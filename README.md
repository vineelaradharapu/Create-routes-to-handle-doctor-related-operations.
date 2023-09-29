# Create-routes-to-handle-doctor-related-operations
// routes/doctor.js
const express = require('express');
const router = express.Router();
const doctorController = require('../controllers/doctorController');

// Get a list of doctors
router.get('/', doctorController.getDoctors);

// Get doctor details by ID
router.get('/:id', doctorController.getDoctorById);

// Book an appointment with a doctor
router.post('/:id/appointments', doctorController.bookAppointment);

module.exports = router;
