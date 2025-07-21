<h1 align="center">🌫️ Particulate Matter Monitoring with SDS018 & STM32</h1>

<p align="center">
  Real-time air quality monitoring using the SDS018 dust sensor and STM32F446RE.
</p>

<hr/>

<h2>📦 Overview</h2>
<ul>
  <li>Measures PM2.5 and PM10 concentrations in real time</li>
  <li>Reads data via UART or PWM</li>
  <li>Displays data over USB serial terminal</li>
  <li>Written in Embedded C using STM32CubeIDE</li>
</ul>

<h2>🧰 Hardware Used</h2>
<table>
  <tr>
    <th>Component</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>SDS018 Sensor</td>
    <td>Laser-based particulate matter detector</td>
  </tr>
  <tr>
    <td>STM32F446RE (Nucleo-64)</td>
    <td>Microcontroller board (ARM Cortex-M4 @ 180 MHz)</td>
  </tr>
  <tr>
    <td>USB-C Cable</td>
    <td>Power + data transfer</td>
  </tr>
</table>

<h3>🔌 Wiring Summary</h3>
<table>
  <tr>
    <th>SDS018 Pin</th>
    <th>Function</th>
    <th>STM32 Pin</th>
  </tr>
  <tr><td>Pin 2</td><td>PWM PM2.5</td><td>PA0</td></tr>
  <tr><td>Pin 3</td><td>5V VCC</td><td>5V</td></tr>
  <tr><td>Pin 4</td><td>PWM PM10</td><td>PA1</td></tr>
  <tr><td>Pin 5</td><td>GND</td><td>GND</td></tr>
  <tr><td>Pin 6</td><td>UART RX</td><td>PA9</td></tr>
  <tr><td>Pin 7</td><td>UART TX</td><td>PA10</td></tr>
</table>

<h2>⚙️ How It Works</h2>
<ul>
  <li><strong>UART:</strong> Reads 10-byte packets, parses PM2.5 & PM10 from raw bytes.</li>
  <li><strong>PWM:</strong> Measures pulse widths using timer input capture.</li>
</ul>

<h2>🚀 Getting Started</h2>
<ol>
  <li>Clone this repository</li>
  <li>Open the project in <strong>STM32CubeIDE</strong></li>
  <li>Connect STM32 via USB and flash the firmware</li>
  <li>Open a serial monitor (e.g. PuTTY, Tera Term) at <code>9600 baud</code></li>
</ol>

<h3>📤 Sample Output</h3>

<pre>
PM2.5 = 14 µg/m³
PM10  = 22 µg/m³
</pre>

<h2>💡 Future Improvements</h2>
<ul>
  <li>Send data to the cloud (e.g., via ESP8266 or ESP32)</li>
  <li>Log long-term air quality data to SD card</li>
  <li>Build a web dashboard for visualization</li>
</ul>


<h2>📄 License</h2>
<p>
  MIT License — feel free to use, modify, and share!
</p>
