 <script>
        const apikey = "48d2dcebc4932fae7d60914b44487b11";
        const apiurl = "https://api.openweathermap.org/data/2.5/weather?units=metric&q=Bangalore";
    
        async function checkWeather() {
            const response = await fetch(apiurl + `&appid=${apikey}`);
            var data = await response.json();
            console.log(data);
            document.querySelector(".city").innerHTML=data.name;
            document.querySelector(".temp").innerHTML=Math.round(data.main.temp) + "°c";
            document.querySelector(".humidity").innerHTML=data.main.humidity + "%";
            document.querySelector(".wind").innerHTML=data.wind.speed +km/h
        }
        checkWeather();
    </script>

