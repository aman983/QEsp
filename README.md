# QEsp
Simulating a Quanutum Computer on Esp32

# What you will need
<ol><li>Esp32</li>
  <li>SSD1306 Display module</li>
  <li>Jumper wires</li>
  <li>Bread board</li></ol>

# How to get started!
<ol>
  <li>
    <b>Install Thonny python IDE</b> 
    <ol><li>For Linux <pre><code>sudo apt-get install thonny</code></pre></li>
    <li>For Windows/Mac Download setup from --> <a href="https://thonny.org/">Here</a></li>
    </ol> 
  </li>
  
  <br><li>
    <b>Install micro python on Esp32</b> 
    <ol><li>Refer this Video  <a href="https://www.youtube.com/watch?v=lvmNLuHj25o">Here</a> </li>
    </ol> 
  </li>

  <br><li>
    <b>Install libraries for QEsp</b> 
    <ol><li>Click on tools -> manage packages</li>
   <p align="center">
  <img src="Resources/1.png" width="950" title="Circuit Diagram"
</p>
      
 <li>Search for ssd 1306 library. Download micropython-ssd1306 library.</li>
  <p align="center">
  <img src="Resources/3.png" width="950" title="Circuit Diagram"
</p>
  <li>A lib folder will be created containing ssd1306.py </li>
    
  <p align="center">
  <img src="Resources/4.png" width="950" title="Circuit Diagram"
</p>
    
    
  <li>open the QEsp.py from the repository in Thonny and press <code>Ctrl+Shift+s</code> on keyboard</li>
  <p align="center">
  <img src="Resources/6.png" width="950" title="Circuit Diagram"
</p>
    
  <li>click save on Micropython Device</li>
  <p align="center">
  <img src="Resources/7.png" width="950" title="Circuit Diagram"
</p>
  
  <li>Go in the lib folder</li>
  <p align="center">
  <img src="Resources/8.png" width="950" title="Circuit Diagram"
</p>
  <li>save in the lib folder as QEsp.py</li>
  <p align="center">
  <img src="Resources/9.png" width="950" title="Circuit Diagram"
</p>
    
  <li>Your lib folder should look like this </li>
  <p align="center">
  <img src="Resources/10.png" width="950" title="Circuit Diagram"
</p>
    
  <li>Run an example sketch form the repo (Before running the code make the circuit given below)</li>
  <p align="center">
  <img src="Resources/12.png" width="950" title="Circuit Diagram"
</p>
    
    
  </ol> 
  </li>
  
  
   
 <br> <li><b>Circuit connections</b> <ol>
    <li>Pin 21 to SDA</li>
    <li>Pin 22 to SCL</li>
    <li>3.3v to VCC</li>
    <li>GND to GND</li>
    </ol> 
  </li>
  
   <p align="center">
  <img src="QEsp circuit.png" width="550" title="Circuit Diagram"
</p>

      
  
  
  <li>
    <b>How to simulate on QEsp</b> 
    <ol><li>create a circuit <code>qc = QuantumCircuit(Number_of_qubits)</code></li>
    <br><li>Apply Quantum Gates to the Circuit 
  <ul><li>Pauli-X Gate : <code>qc.x(Index_of_Qubit)</code></li>
  <li>Hadamard Gate : <code>qc.h(Index_of_Qubit)</code></li> 
  <li>Pauli-Z : <code>qc.z(Index_of_Qubit)</code></li> 
  <li>Rotation Gate : <code>qc.r(Angle_in_radians,Index_of_Qubit)</code></li> 
  <li>Controll-X Gate : <code>qc.cx(Controll_Index,Target_Index)</code></li>
  <li>Controll-Z Gate : <code>qc.cz(Controll_Index,Target_Index)</code></li>
  <li>Controll-R Gate : <code>qc.cr(Controll_Index,Target_Index)</code></li> 
  <li>Controll-Controll-X Gate : <code>qc.ccx(Controll_Index1,Controll_Index2,Target_Index)</code></li></ul>
  </li></br>
    <li>To measure Qubits : <code>qc.execute()</code></li>
    <li>Prints a single unitary matrix : <code>qc.unitary()</code></li>
    <li>Prints the current quantum state of the circuit : <code>qc.state</code></li>
    <li>Prints the probability of the states : <code>qc.prob()</code></li>
    </ol> 
  </li>
  
</ol>

  
  <em>*Currently You can simulate upto 5 Qubits on QEsp.</em> 
