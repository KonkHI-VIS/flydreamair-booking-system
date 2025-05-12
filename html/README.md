The html code, display only at the moment
## Backend layout
- when programming the backend layout information will be parsed through a temp json file and can be imported using this code
- this is template code and just displays the information parsed from the information-input.html file.
- you will need to change the variables based on what information will be parsed to your page.
- You will need to change the layout based on the design of your page.

<pre lang=html>
<body>
        <script>
            window.onload = function() {
            const bookingData = JSON.parse(localStorage.getItem("bookingData"));
            if (bookingData) {
                document.getElementById("bookingDetails").innerHTML = `
                    <p><strong>From:</strong> ${bookingData.from}</p>
                    <p><strong>To:</strong> ${bookingData.to}</p>
                    <p><strong>Departure Date:</strong> ${bookingData.departureDate}</p>
                    <p><strong>Return Date:</strong> ${bookingData.returnDate}</p>
                    <p><strong>Passengers:</strong> ${bookingData.passengers}</p>
                `;
            }
        };
        </script>

        <div id="bookingDetails"></div>  
  </body>
  </pre>
