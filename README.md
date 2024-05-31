import React, { useState } from 'react';

const DeviceShop = () => {
  const [message, setMessage] = useState('');

  const checkPCPrice = (price) => {
    if (price <= 20000) {
      setMessage('This laptop is 20,000 pesos.');
    } else if (price >= 20000) {
      setMessage('This laptop is 20,000 pesos, this is your change.');
    }
  };

  const checkPhonePrice = (price) => {
    if (price <= 15000) {
      setMessage('This phone is 15,000 pesos.');
    } else if (price >= 15000) {
      setMessage('This phone is 15,000 pesos only, this is your change.');
    }
  };

  const checkiPadPrice = (price) => {
    if (price !== 25000) {
      setMessage('The iPad price must be exactly 25,000 pesos.');
    } else {
      setMessage('The iPad price is correct.');
    }
  };

  return (
    <div>
      <h1>Device Shop</h1>
      <div>
        <h2>Check PC Price</h2>
        <button onClick={() => checkPCPrice(20000)}>Check PC</button>
      </div>
      <div>
        <h2>Check Phone Price</h2>
        <button onClick={() => checkPhonePrice(15000)}>Check Phone</button>
      </div>
      <div>
        <h2>Check iPad Price</h2>
        <button onClick={() => checkiPadPrice(25000)}>Check iPad</button>
      </div>
      <div>
        <h2>Message</h2>
        <p>{message}</p>
      </div>
    </div>
  );
};

export default DeviceShop;
