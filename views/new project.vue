<template>
    <div class="contact-form">
      <h1 style="background-color: yellowgreen;">Contact Form</h1>
      <form @submit.prevent="submitForm">
        <label for="Name">Name:</label>
        <input id="Name" v-model="formData.name" required placeholder="Please let me know you name">
        
        <label for="contact">Contact:</label>
        <input id="contact" v-model="formData.contact" type="Contact" required placeholder="Your Contact no">
    
        <label for="message">Message:</label>
        <textarea id="message" v-model="formData.message" rows="4" required placeholder="Drop a message for me"></textarea>
    
        <button type="submit" class="submit-button">Submit</button>
      </form>
    </div>
    
    </template>
    
    <script>
    export default {
    data() {
      return {
        formData: {
          Name: '',
          contact: '',
          message: ''
        }
      };  
    },
    methods: {
      submitForm() {
        console.log('Form Data:', this.formData);
        alert('Form submitted successfully!');
      }
    }
    }
    </script>
    
    
    
<style>
    .contact-form {
      background-color: #f8f8f8;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
      text-align: center;
    }
    
    .contact-form h1 {
      background-color: yellowgreen;
      color: #fff;
      padding: 10px;
      border-radius: 5px;
    }
    
    .contact-form form {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 15px;
    }
    
    .contact-form label {
      font-weight: bold;
    }
    
    .contact-form input[type="text"],
    .contact-form input[type="Contact"],
    .contact-form textarea {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    
    .contact-form textarea {
      resize: vertical;
    }
    
    .contact-form .submit-button {
      background-color: yellowgreen;
      color: #fff;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    
    .contact-form .submit-button:hover {
      background-color: #4CAF50;
    }
    
    /* Responsiveness */
    
    @media screen and (max-width: 600px) {
      .contact-form form {
        width: 80%;
      }
    }
</style> 