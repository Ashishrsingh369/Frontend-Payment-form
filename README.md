# Frontend-Payment-form
Javascript with React used to create secure payment form
import React, { useState } from 'react';

function PaymentForm() {
    const [amount, setAmount] = useState('');

    const handleSubmit = (e) => {
        e.preventDefault();
        console.log(`Processing payment of $${amount}`);
        // Integrate with backend API
    };

    return (
        <form onSubmit={handleSubmit}>
            <input
                type="number"
                value={amount}
                onChange={(e) => setAmount(e.target.value)}
                placeholder="Enter amount"
            />
            <button type="submit">Pay Now</button>
        </form>
    );
}

export default PaymentForm;
