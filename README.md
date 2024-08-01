<h1>Robô Modalidade Sumô - Controle Remoto</h1>
<p>
  Um robô sumô é um tipo de robô projetado para participar de competições inspiradas no esporte tradicional japonês de sumô. Essas competições envolvem dois robôs tentando empurrar um ao outro para fora de uma arena circular, chamada dohyo, de maneira semelhante aos lutadores de sumô humanos.
</p>
<p>
  Existem diferentes categorias de robôs sumô, geralmente baseadas em seu peso e tamanho, como micro, mini e mega sumô. Os robôs são frequentemente equipados com sensores, motores e outras tecnologias que permitem a detecção do adversário e estratégias de movimentação para empurrá-lo para fora do dohyo. As competições de robô sumô combinam engenharia, programação e design, desafiando os participantes a criar máquinas autônomas que podem competir de forma eficaz.
</p>
<p>
  Os robôs podem ser controlados remotamente ou ser totalmente autônomos, dependendo das regras da competição. Em competições de robôs sumô autônomos, os robôs dependem exclusivamente de sua programação e sensores para tomar decisões em tempo real durante a luta.
</p>

<h2>Conexão Bluetooth</h2>
<p>
  Para criar um robô controlado remotamente, utilizei a ESP32, um microcontrolador com suporte a Bluetooth. A conexão entre o controle remoto e a ESP32 foi estabelecida utilizando um host de Bluetooth chamado BluePad32, que gerencia eficientemente a comunicação Bluetooth entre os dispositivos.
</p>
<p>
  O funcionamento do robô é baseado nessa conexão. Uma vez estabelecida a comunicação entre o controle remoto e a ESP32, os comandos enviados pelas teclas do controle são transmitidos para a ESP32. Esta, por sua vez, processa esses comandos e executa as operações correspondentes, como movimentar o robô para frente, para trás, virar para os lados ou frear. Dessa forma, o robô responde de maneira precisa e rápida às instruções do controle remoto, permitindo um controle eficaz durante suas operações.
</p>

<h2>Integração</h2>
<p>
  Para programar a ESP32, vamos utilizar a plataforma Arduino IDE. Siga os passos abaixo para instalar o suporte para a ESP32:
  <ol>
    <li>
      <strong>Baixar e instalar a Arduino IDE:</strong>
      <ul>
        <li>
          Se você ainda não tem a Arduino IDE instalada, baixe-a do <a href="https://www.arduino.cc/en/software">site oficial do Arduino</a> e siga as instruções de instalação para o seu sistema operacional.
        </li>
      </ul>
    </li>
    <li>
      <strong>Abrir a Arduino IDE:</strong>
      <ul>
        <li>Após a instalação, abra a Arduino IDE.</li>
      </ul>
    </li>
    <li>
      <strong>Adicionar suporte para a ESP32:</strong>
      <ul>
        <li>Vá para o menu "File" (Arquivo) e selecione "Preferences" (Preferências).</li>
        <li>Na janela que abrir, procure pelo campo "Additional Boards Manager URLs" (URLs Adicionais do Gerenciador de Placas).</li>
        <li>Adicione a seguinte URL: <strong>https://dl.espressif.com/dl/package_esp32_index.json</strong></li>
        <li>Clique em "OK" para salvar as mudanças.</li>
      </ul>
    </li>
    <li>
      <strong>Instalar o pacote da ESP32:</strong>
      <ul>
        <li>Vá para o menu "Tools" (Ferramentas) e selecione "Board" (Placa) e depois "Boards Manager" (Gerenciador de Placas).</li>
        <li>Na janela que abrir, digite "ESP32" na barra de busca.</li>
        <li>Encontre o pacote "esp32" da Espressif Systems e clique em "Install" (Instalar).</li>
      </ul>
    </li>
    <li>
      <strong>Adicionar suporte para Bluepad32:</strong>
      <ul>
        <li>Vá para o menu "File" (Arquivo) e selecione "Preferences" (Preferências).</li>
        <li>Na janela que abrir, procure pelo campo "Additional Boards Manager URLs" (URLs Adicionais do Gerenciador de Placas).</li>
        <li>Adicione a seguinte URL: <strong>https://raw.githubusercontent.com/ricardoquesada/esp32-arduino-lib-builder/master/bluepad32_files/package_esp32_bluepad32_index.json</strong></li>
        <li>Clique em "OK" para salvar as mudanças.</li>
      </ul>
    </li>
    <li>
      <strong>Instalar o pacote da ESP32:</strong>
      <ul>
        <li>Vá para o menu "Tools" (Ferramentas) e selecione "Board" (Placa) e depois "Boards Manager" (Gerenciador de Placas).</li>
        <li>Na janela que abrir, digite "esp32_bluepad32" na barra de busca.</li>
        <li>Encontre o pacote "esp32_bluepad32" da Ricardo Quesada e clique em "Install" (Instalar).</li>
      </ul>
    </li>
    <li>
      <strong>Selecionar a placa ESP32:</strong>
      <ul>
        <li>Após a instalação, vá novamente para o menu "Tools" (Ferramentas), selecione "Board" (Placa), vá em "esp32_bluepad32" e escolha o modelo específico da sua placa ESP32.</li>
      </ul>
    </li>
  </ol>
</p>
<p>
  Depois de completar esses passos, a Arduino IDE estará configurada para programar a ESP32. Agora você está pronto para começar a desenvolver e carregar códigos para a sua placa ESP32.
</p>

<h2>Lista de Materiais</h2>
<table>
  <tr>
    <td>Quantidade</td>
    <td>Componente</td>
  </tr>
  <tr>
    <td>1</td>
    <td>ESP32</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Relé 5V - 4 Canais</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Relé 5V</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Motor Vidro Elétrico</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Bateria 18650</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Bateria Lipo 11.1V</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Case para batereira 18650</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Conetores XT60(macho+fêmea)</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Controle remoto compatível com o Bluepad</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Barra roscada de 8mm</td>
  </tr>
  <tr>
    <td>2</td>
    <td>rolamento 628 2rs</td>
  </tr>
  <tr>
    <td>1kg</td>
    <td>Filamento para impressão 3D</td>
  </tr>
</table>

<h2>Diagrama de Ligação</h2>
<img src="https://github.com/pedro4896/RoboSumo/blob/main/Diagrama_conexao.jpg" height="400px" align="center">

<h2>Créditos</h2>
<ul>
  <li>Ricardo Quesada: https://github.com/ricardoquesada/bluepad32</li>
  <li>Abraao Lacerda: https://www.youtube.com/watch?v=K_rIaBKQcCk</li>
</ul>
