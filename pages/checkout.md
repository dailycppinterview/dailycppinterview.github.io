---
layout: page
title: Hi...
permalink: /checkout/
---
... my name is Sandor. I work as a C++ developer, but I'm also enthusiastic about Python. Before I became a software developer, I was on the dark side. No, I have never been a manager, I meant operations.

I was a DBA in one of the most process-oriented corporations (according to NY Times), but I wanted more freedom and creativity. The more time I've spent on coding, the more I realized how much fun it is and how much I love high-quality code - and how far I am from it!

When I'm not on the road with my family, or not baking something in the kitchen, I read and write. I write mostly about the books I read, the importance of Stoic philosophy, and of course, C++.

Thanks for visiting my blog and if you like it, sign up for [my newsletter](http://eepurl.com/gvcv1j)!

<!-- Load Stripe.js on your website. -->
<script src="https://js.stripe.com/v3"></script>

<!-- Create a button that your customers click to complete their purchase. Customize the styling to suit your branding. -->
<button
  style="background-color:#6772E5;color:#FFF;padding:8px 12px;border:0;border-radius:4px;font-size:1em"
  id="checkout-button-price_1HJIzBDCVI1zPppGCpvadRBD"
  role="link"
  type="button"
>
  Checkout
</button>

<div id="error-message"></div>

<script>
(function() {
  var stripe = Stripe('pk_live_51HIwudDCVI1zPppGIIyhEcQJabeWldO7mHfb1fSS9Ihv770q9g0wOMs99eBE8t7ONoLs6ZlTxLyr1p300bLE4wNY0059JlKaTk');

  var checkoutButton = document.getElementById('checkout-button-price_1HJIzBDCVI1zPppGCpvadRBD');
  checkoutButton.addEventListener('click', function () {
    // When the customer clicks on the button, redirect
    // them to Checkout.
    stripe.redirectToCheckout({
      lineItems: [{price: 'price_1HJIzBDCVI1zPppGCpvadRBD', quantity: 1}],
      mode: 'subscription',
      // Do not rely on the redirect to the successUrl for fulfilling
      // purchases, customers may not always reach the success_url after
      // a successful payment.
      // Instead use one of the strategies described in
      // https://stripe.com/docs/payments/checkout/fulfillment
      successUrl: 'http://www.dailycppinterview.com/success',
      cancelUrl: 'http://www.dailycppinterview.com/canceled',
    })
    .then(function (result) {
      if (result.error) {
        // If `redirectToCheckout` fails due to a browser or network
        // error, display the localized error message to your customer.
        var displayError = document.getElementById('error-message');
        displayError.textContent = result.error.message;
      }
    });
  });
})();
</script>