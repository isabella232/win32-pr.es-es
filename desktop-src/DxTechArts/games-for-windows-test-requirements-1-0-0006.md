---
title: 'Casos de prueba de Games for Windows: procedimientos recomendados para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8'
description: En este artículo se proporcionan casos de prueba para juegos para Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104bf659e439108bc18cf30dd1bef40a63197e7c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625120"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Juegos para Windows casos de prueba: procedimientos recomendados para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8

En este artículo se proporcionan casos de prueba para juegos para Windows.

## <a name="how-to-use-this-article"></a>Cómo usar este artículo

Hay tres secciones principales de este artículo:

<dl> <dt>

<span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisitos de prueba**
</dt> <dd>

Cada requisito de prueba de este documento tiene cuatro secciones principales: un título y una tabla con tres secciones importantes (columna izquierda, parte superior derecha e inferior derecha).

<dl> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Título
</dt> <dd>

Nombre del caso de prueba.

</dd> <dt>

<span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Cuadro, columna de extremo izquierdo
</dt> <dd>

Nombres de los sistemas operativos a los que se aplica el caso de prueba.

</dd> <dt>

<span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, parte superior derecha
</dt> <dd>

Breve resumen del caso de prueba.

</dd> <dt>

<span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Cuadro, parte inferior derecha
</dt> <dd>

Detalles del caso de prueba real.

</dd> </dl> </dd> <dt>

<span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Script de prueba de ejemplo**
</dt> <dd>

Esta sección es un ejemplo de la secuencia que seguiría una prueba típica si se usan los requisitos de prueba como guía.

</dd> <dt>

<span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Notas de la herramienta de prueba**
</dt> <dd>

Esta sección contiene notas detalladas sobre cada una de las herramientas de prueba usadas para comprobar las condiciones de superación o error en los requisitos de prueba.

</dd> </dl>

## <a name="test-requirements"></a>Requisitos de prueba

### <a name="1-game-requirements"></a>1. Requisitos del juego

### <a name="11-windows-games-explorer"></a>1.1 Windows Games Explorer



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>El juego debe estar visible en el Explorador de juegos en Windows Vista y Windows 7. Cuando se selecciona, el juego también debe mostrar los metadatos correctos. La instalación no debe crear un acceso directo para iniciar el juego en el escritorio, en el menú Inicio o en cualquier otra ubicación. No se deben crear tareas ni métodos abreviados para la eliminación.</td>
</tr>
<tr class="even">

<td><ol>
<li>Después de instalar el juego, abra El Explorador de juegos.</li>
<li>Compruebe que el icono del juego se muestra en el Explorador de juegos.</li>
<li>Haga clic con el botón derecho en el icono y pruebe cada tarea de soporte técnico de & definida por la aplicación.</li>
<li>Haga clic en el icono y compruebe que los metadatos (publicador, desarrollador, género, fecha de lanzamiento, versión) en la parte inferior se muestran y son correctos.</li>
<li>Compruebe que el icono del juego muestra Windows índice de experiencia (WEI) en El Explorador de juegos.</li>
<li>Compruebe que los hipervínculos de juegos para metadatos funcionan correctamente en El Explorador de juegos. (Si los hipervínculos no se muestran, se trata de un posible signo de que el archivo exe no está firmado; vea <a href="#23-sign-files">la sección 2.3).</a></li>
<li>Compruebe que el juego muestra una clasificación de control parental precisa en Games Explorer. (Si dice no clasificado, compruebe que se trata de un juego no clasificado; de lo contrario, es un indicador de que el archivo exe no está firmado; vea la sección <a href="#23-sign-files">2.3).</a></li>
<li>Compruebe que el juego no coloca accesos directos de inicio en el escritorio del usuario.</li>
<li>Haga clic en Inicio -> Todos los programas.</li>
<li>Compruebe que el juego no coloca accesos directos de inicio en el menú Inicio.</li>
<li>Compruebe que el juego no coloca los accesos directos de desinstalación en el menú Inicio fuera de Panel de control.</li>
<li>Si el juego se distribuye digitalmente, compruebe que el proveedor de servicios aparece en Windows Games Explorer.</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a>1.2 Windows seguridad de familia y controles parentales



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>El juego debe ejecutarse en el contexto de &quot; un usuario &quot; estándar. Los controles parentales deben poder bloquear el juego. Compruebe que GDF tiene nombres EXE.</td>
</tr>
<tr class="even">

<td><ol>
<li>Cree una cuenta de usuario estándar en Windows Vista o Windows 7 denominada Toby. Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</li>
<li>Como Julia, desde la cuenta de administrador, configure los controles parentales para el juego. Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby
<ol>
<li>Compruebe que el juego se inicia desde el icono del Explorador de juegos.</li>
<li>Compruebe que el juego muestra la clasificación de control parental precisa debajo del título del juego en el cuadro de diálogo Controles parentales Panel de control.</li>
<li>Antes de aplicar los controles parentales, compruebe que el juego no solicita credenciales de administrador al iniciarse.</li>
<li>Establezca Controles parentales en &quot; En &quot; .</li>
<li>En la sección Windows Configuración, haga clic en Juegos.</li>
<li>Haga clic en Aceptar (la configuración ahora debe ser &quot; AO / todos los &quot; juegos).</li>
<li>Compruebe que el juego se ejecuta con esta configuración como User Jane.</li>
<li>Cierre sesión como Julia e inicie sesión como Toby.</li>
<li>Compruebe que el juego se ejecuta con esta configuración como User Toby.</li>
<li>Cierre sesión como Toby e inicie sesión como Julia.</li>
<li>Vuelva a la pantalla anterior y seleccione &quot; Establecer clasificaciones de &quot; juegos.</li>
<li><p>Seleccione una clasificación inferior a la clasificación de ESRB del juego.</p>
<blockquote>
[!Note]<br />
Si el juego no está clasificado, omita este paso y pase a la siguiente parte de esta prueba. Puede que sea necesario elegir un sistema de clasificación diferente para encontrar una clasificación de juego, en función de la configuración regional del idioma de la SKU que se está probando.
</blockquote>
<p><br/></p></li>
<li>Cierre sesión como Julia e inicie sesión como Toby.</li>
<li>Compruebe que el juego no se inicia para El usuario Toby cuando es bloqueado por el usuario Julia.</li>
<li>Cierre sesión como Toby e inicie sesión como Julia.</li>
<li>Si se ha cambiado anteriormente, restaure la configuración de ESRB.</li>
<li>Si no hay ninguna configuración de ESRB, seleccione Bloquear o Permitir juegos específicos &quot; y seleccione el juego por &quot; nombre.</li>
<li>Cierre sesión como Julia e inicie sesión como Toby.</li>
<li>Compruebe que el juego no se inicia para User Toby cuando el usuario Jane bloquea EXE/Name.</li>
<li>Cierre sesión como Toby y vuelva a iniciarla como Julia.</li>
<li>Como Julia, abra Controles de usuario -> restricciones de aplicación.</li>
<li>Haga clic en Toby solo puede usar los programas que se permiten y haga clic en &quot; &quot; Aceptar (es decir, no permitir exes).</li>
<li>Vaya a Controles de usuario | Controles de juegos y permitir el juego específico mediante la clasificación de ESRB.</li>
<li>Cierre sesión como Julia e inicie sesión como Toby e intente jugar al juego.</li>
<li>Compruebe que el juego NO está bloqueado y que Toby puede reproducirlo cuando no se establece allow &quot; &quot; exes.</li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a>1.3 Windows juegos guardados enriquecidos de Vista

Este requisito se ha retirado.

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 Xbox 360 controlador común para Windows \[ condicional\]



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos que admiten controladores gamepad deben admitir el Mando Xbox 360 para Windows mediante la API XInput. Todas las referencias a botones y desencadenadores de controlador comunes deben usar Xbox 360 nombres.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inicie el juego.</li>
<li>Vaya a las opciones del controlador. **</li>
<li>Compruebe que el juego reconoce Mando Xbox 360 para Windows como un dispositivo de entrada.</li>
<li>Jugar al juego y comprobar que el juego y el sistema de menús se pueden controlar con Mando Xbox 360 para Windows.</li>
<li>Compruebe que el Mando Xbox 360 para Windows se comporta según los estándares aceptados. (B para atrás, A para aceptar, Iniciar para en el menú del juego, pausar o aceptar, etc.)</li>
<li>Compruebe que el juego hace referencia a los botones y desencadenadores del controlador Xbox 360 nombres.</li>
</ol>
<br/>
<blockquote>
[!Note]<br />
Si el juego no admite un controlador de juego o solo admite teclado o mouse, omita este caso de prueba.
</blockquote>
<br/> ** Configuración del controlador podría encontrarse fuera del juego. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a>1.5 Varias relaciones de aspecto y resoluciones



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>El juego debe admitir al menos las siguientes relaciones de aspecto y resoluciones de pantalla asociadas: <br/>
<ul>
<li>4:3 &quot; normal &quot; (800 600 o 1024 768)</li>
<li>16:9 &quot; widescreen &quot; (1280 720)</li>
<li>16:10 &quot; widescreen &quot; (1152 720, 1680 1050 o 800 480)</li>
</ul></td>
</tr>
<tr class="even">

<td>Busque las opciones de vídeo del juego (puede que esté fuera de juego).<br/>
<blockquote>
[!Note]<br />
Las siguientes pruebas deben realizarse en un monitor de pantalla ancha.
</blockquote>
<br/>
<ol>
<li>En la sección de resolución de vídeo, seleccione 800 600 o 1024 768.</li>
<li>Compruebe que el juego se ejecuta con una resolución de relación de aspecto 4:3.</li>
<li>En la sección resolución de vídeo, seleccione 1280 720.</li>
<li>Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:9.</li>
<li>En la sección de resolución de vídeo, seleccione 1680 1050, 800 480 o 1152 720.</li>
<li>Compruebe que el juego se ejecuta en una resolución de relación de aspecto de 16:10.</li>
<li>Compruebe que el juego no extiende la imagen y, a su vez, presenta un área de vista más amplia.</li>
<li>Compruebe que el juego solicita al usuario cuando se realiza un cambio en la resolución.</li>
<li>Si el usuario no acepta en 15 segundos, compruebe que la pantalla se revierta a la configuración anterior.</li>
<li>Compruebe que el juego no agrega barras negras a la izquierda y derecha del área de juego del juego. (En este caso, verá que el área de juego sigue en una relación de 4:3 en el centro de la pantalla).</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a>1.6 Windows Media Center

Este requisito se ha retirado.

### <a name="17-direct3d-conditional-requirement"></a>1.7 Requisito condicional de \[ Direct3D\]



| SO                                                                    | Requisito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> Windows XP<br/> | Si el juego usa Direct3D, la versión mínima admitida debe ser Direct3D 9 y Direct3D debe ser el valor predeterminado para cualquier opción de configuración de pantalla.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> <dd> Inicie el juego. En las opciones de vídeo, compruebe si hay opciones de representación, D3D o OpenGL. Si lo hay, compruebe que las opciones de representación del juego tienen como valor predeterminado Direct3D. Si no puede comprobar que D3D9 es la versión de DirectX que se usa, continúe con La prueba automatizada. <br/> </dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> <dd> Usar herramienta: Depends.exe <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a>1.8 Habilitar reconocimiento de valores altos de PPP



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Los juegos y sus instaladores deben ejecutarse correctamente sin problemas visuales cuando el escalado de PPP está habilitado.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> <dd>
<ol>
<li>Establezca el sistema en PPP 150 %: <br/> Windows Vista: Panel de control personalización, ajuste del tamaño de fuente (PPP), PPP personalizado. Establezca en 150 %.<br/> Windows 7: Panel de control: Mostrar, Establecer en Mayor - 150 %.<br/></li>
<li>Ejecute el proceso de instalación y el juego para comprobar que no hay ningún problema con pantallas recortadas o cuadros de diálogo.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> <dd> Compruebe que el <dpiAware>elemento true</dpiAware> está contenido en el manifiesto incrustado.<br/> Usar herramienta: Mt.exe <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a>2. Seguridad y compatibilidad

### <a name="21-follow-user-account-control-guidelines"></a>2.1 Siga las instrucciones de control de cuentas de usuario



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Cada archivo ejecutable (.EXE extensión) incluido con una aplicación debe tener un manifiesto incrustado que defina su nivel de ejecución:
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
En el caso de los juegos y instaladores de juegos, uiAccess siempre debe establecerse en &quot; &quot; false.
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Compruebe que los archivos ejecutables del juego contienen manifiestos.</li>
<li>Compruebe que el manifiesto del archivo ejecutable del juego solicitadoExecutionLevel &quot; es AsInvoker. &quot;</li>
</ol>
Usar herramienta: Mt.exe <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a>2.2 Compatibilidad con versiones x64 de Windows



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Para mantener la compatibilidad con las versiones x64 de Windows: <br/>
<ul>
<li>Los títulos y los instaladores de títulos no deben contener ningún código de 16 bits ni depender de ningún componente de 16 bits.</li>
<li>Si el juego depende de los controladores en modo kernel para el funcionamiento, las versiones x64 de estos controladores deben estar disponibles. La configuración del juego debe detectar e instalar los controladores y componentes adecuados para las ediciones de 64 bits de Windows.</li>
</ul>
<blockquote>
[!Note]<br />
La compatibilidad con la edición de 64 bits de Windows XP Professional es opcional.
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td>Prueba manual<br/>
<ol>
<li>Ejecute el juego en ediciones de 64 bits de Windows. Compruebe que el proceso de instalación del juego se ejecuta normalmente en ediciones de 64 bits de Windows Vista o Windows 7.</li>
<li>Compruebe que el juego no encuentra un error como resultado de archivos ejecutables de 16 bits en ediciones de 64 bits de Windows Vista o Windows 7. El error mencionará la aplicación de 16 bits en la ventana de error.</li>
<li>Si el juego tiene un ejecutable nativo de 64 bits, úselo también.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a>2.3 Archivos de firma



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Todos los archivos de código ejecutable (por ejemplo, .exe y .dll) deben estar firmados con un certificado Authenticode. <br/> Si usa el instalador Windows, los archivos de paquete del instalador (.msi archivos) deben estar firmados. <br/></td>
</tr>
<tr class="even">

<td>Prueba manual<br/>
<ol>
<li>Vaya al directorio del juego.</li>
<li>Busque todos los archivos .exe y .dll archivos.</li>
<li>Haga clic con el botón derecho en Propiedades en cada archivo.</li>
<li>Compruebe que los archivos ejecutables del juego contienen una firma digital.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a>2.4 Controladores de firma



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Cualquier controlador en modo kernel instalado por el juego debe estar firmado con un certificado Authenticode válido públicamente. <br/> Cualquier controlador de dispositivo de hardware en modo kernel instalado por el juego debe tener una firma de Microsoft obtenida a través del programa Windows Hardware Quality Labs (WHQL) o firma de confiabilidad de controladores (DRS). <br/></td>
</tr>
<tr class="even">

<td>Prueba manual<br/>
<ol>
<li>Instale el juego.</li>
<li>Compruebe que el proceso de instalación del juego no muestra diálogos de controladores sin signo.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a>2.5 Realizar correctamente la comprobación de versiones



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos no deben dejar de ejecutarse en sistemas operativos futuros, como indican los cambios en el número de versión de Windows, a menos que el Contrato de licencia del usuario final prohíba el uso en sistemas operativos futuros. Si se supone que se producirá un error en el juego, debe hacerlo correctamente mostrando un mensaje al usuario.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> <dd>
<ol>
<li>Instale el juego en Windows XP, en ediciones de 32 bits de Windows Vista y Windows 7, y en ediciones de 64 bits de Windows Vista y Windows 7.</li>
<li>Compruebe que el proceso de instalación del juego no encuentra un error con respecto a la versión del sistema operativo.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> <dd> Usar herramienta: Application Verifier<br/>
<ol>
<li>Inicie Application Verifier.</li>
<li>Habilite la prueba Compatibility:HighVersionLie después de seleccionar el INSTALL.EXE.</li>
<li>Instale el juego y asegúrese de que no bloquea la instalación en función de la versión del sistema operativo.</li>
<li>Habilite la prueba Compatibility:HighVersionLie después de seleccionar el GAME.EXE.</li>
<li>Ejecute el juego y asegúrese de que no bloquea la ejecución en función de la versión del sistema operativo.</li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a>2.6 Compatibilidad con sesiones de usuario simultáneas



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos deben admitir escenarios Windows multitarea estándar.</td>
</tr>
<tr class="even">

<td>Cree una cuenta de usuario estándar en Windows Vista o Windows 7 denominada Toby. Start -> Control Panel -> Add or Remove User Accounts -> Create New Account <br/>
<ol>
<li>Inicie el juego como User Jane.</li>
<li>ALT+TAB de vuelta al escritorio.</li>
<li>Compruebe que el juego esté correctamente alt+TABs en el Windows escritorio.</li>
<li>Haga clic en Inicio > [flecha situada a la derecha de Bloquear] -> Cambiar usuario.</li>
<li>Inicie sesión como User Toby.</li>
<li>Compruebe que el juego se inicia como User Toby mientras sigue ejecutándose como User Jane.</li>
<li>Compruebe que el juego no encuentra errores para User Toby o User Jane durante el proceso de cambio de usuario.</li>
<li>Si puede iniciar otra sesión de juego, compruebe que no puede escuchar audio de la sesión de juego original.</li>
<li>Cierre el juego y vuelva al usuario y al juego originales.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a>2.7 Compatibilidad con nombres largos



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Si un juego admite guardar archivos, debe ser capaz de guardar archivos que tengan nombres largos y rutas de acceso. El juego debe controlar correctamente los caracteres especiales del sistema de archivos, como \ / : * ? &quot; < o > en los campos de entrada del usuario usados para crear rutas de acceso o nombres de archivo.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inicie el juego.</li>
<li>Inicie un nuevo juego.</li>
<li>Guarde el juego. Durante el proceso de guardado, compruebe que el juego se guarda con el nombre guardado: Mi primer juego guardado.</li>
<li>Vuelva al menú principal.</li>
<li>Intente cargar el juego recién guardado.</li>
<li>Compruebe que el juego no encuentra errores al controlar caracteres del sistema de archivos no admitidos, como \ / : * ? &quot; < o > si el juego lo permite, asigne un nombre al juego guardado.</li>
<li>Si el usuario puede dar nombre a su perfil o carácter o guardar juegos, compruebe que el juego no encuentra errores al usar también nombres de archivo largos aquí.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a>3. Instalación

### <a name="31-easy-install"></a>3.1 Instalación sencilla



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos con una instalación tradicional deben proporcionar una ruta de acceso simplificada en su interfaz de usuario de configuración.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inserte el disco del juego.</li>
<li>Compruebe que el juego no muestra más de un End-User licencia (CLUF).</li>
<li>Si el juego admite una opción de instalación personalizada o avanzada, compruebe que esta opción es accesible durante el proceso de instalación.</li>
<li>Compruebe que la opción Instalación predeterminada omite todas las selecciones de entrada del usuario para el proceso de instalación (selección de carpeta de instalación, selección de componentes, entre otras).</li>
<li>Compruebe que el proceso de instalación del juego no solicita la configuración del componente del sistema operativo (configuración de DirectX, entornos de ejecución de Visual C, y así sucesivamente).</li>
<li>Compruebe que el proceso de instalación del juego no solicita la interacción del firewall.</li>
<li>Compruebe que el juego se ejecuta automáticamente o que hay un menú del iniciador al final del proceso de instalación.</li>
<li>Compruebe que el proceso de desinstalación del juego quita todos los archivos de componentes del sistema operativo instalados y no redistribuidos y borra toda la configuración. No es necesario limpiar toda la configuración y los datos por usuario (por ejemplo, juegos guardados).</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a>3.2 Compatibilidad con el control de cuentas de usuario para la instalación



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>El instalador del juego no debe asumir que se ejecuta en el mismo contexto que el usuario. Por lo tanto, los juegos deben realizar tareas por usuario en la primera ejecución por separado de la instalación.</td>
</tr>
<tr class="even">

<td><ol>
<li>Compruebe que puede instalar el juego como User Jane. (Esto requerirá derechos elevados durante el proceso de instalación o instalación).</li>
<li>Compruebe que el proceso de instalación del juego solicita al usuario Julia que eleve a través de credenciales de administrador. (El mensaje para elevar aparecerá cuando el usuario intente instalar).</li>
<li>Opte por Ejecutar automáticamente el juego al final de la instalación, si aún no lo hace, o iniciarlo desde el menú que aparece.</li>
<li>Una vez dentro del juego, cree un nuevo perfil, jugar y guardar un juego.</li>
<li>Salga del juego.</li>
<li>Reinicie el juego y compruebe que la cuenta user jane puede acceder a los perfiles de usuario y a los juegos guardados.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a>3.3 Instalar en carpetas correctas



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos deben instalarse en la carpeta Archivos de programa de forma predeterminada. Los datos de usuario deben escribirse en la primera ejecución y no durante la instalación.</td>
</tr>
<tr class="even">

<td><ol>
<li>Instale el juego con el tipo de instalación Predeterminado.</li>
<li>Compruebe que el juego se instaló en Archivos de programa.</li>
</ol>
<blockquote>
[!Note]<br />
Si se produce un error en esta prueba, compruebe que el juego está pensado para instalarse para Todos los usuarios. Si es así, se trata de un error.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a>3.4 Instalar Windows recursos correctamente



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Las aplicaciones no deben intentar instalar archivos ni claves del Registro que estén protegidas por Windows Resource Protection (WRP).</td>
</tr>
<tr class="even">

<td><ul>
<li>Compruebe que no aparecen Windows de diálogo WRP de Resource Protection durante el proceso de instalación.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a>3.5 Evitar reinicios durante la instalación



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>El instalador del juego no debe suponer que la instalación de componentes de Windows desde paquetes de redistribución requiere un reinicio, a menos que el reinicio se indique mediante un resultado devuelto o por la documentación de Microsoft.</td>
</tr>
<tr class="even">

<td><ol>
<li>Instale el juego.</li>
<li>Compruebe que el juego no requiere que el sistema se reinicie después de la instalación.</li>
</ol>
<blockquote>
[!Note]<br />
Si una actualización del sistema de Microsoft REDIST requiere un reinicio, haga lo siguiente: Complete la instalación del juego, desinstale el juego y vuelva a instalarlo una segunda vez. El proceso de instalación del juego no debe requerir un reinicio en esta segunda instalación.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a>3.6 Usar el control de versiones de archivos correctamente



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>El programa de instalación del juego debe comprobar correctamente que están instaladas las versiones de archivo más recientes. La instalación de un juego nunca debe volver a los archivos que no se producen o que comparten las aplicaciones que no se producen.</td>
</tr>
<tr class="even">

<td><ol>
<li>Antes de instalar el juego, cree una instantánea previa a la instalación de System32.<br/>
<ol>
<li>Crear un directorio denominado G4Wtest.</li>
<li>Abre una ventana de comandos (Start -> Run -> cmd).</li>
<li>Vaya a c:\windows\system32.</li>
<li>Escriba dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</li>
</ol></li>
<li>Cree una instantánea posterior a la instalación de System32. <br/>
<ol>
<li>Abre una ventana de comandos (Start -> Run -> cmd).</li>
<li>Vaya a c:\windows\system32.</li>
<li>Escriba dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</li>
<li>Compruebe que el juego no revierte ninguna versión de archivo de archivos que el juego no produjo (... de los archivos enumerados en los dos documentos comparando pregame.txt con postgame.txt).</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a>3.7 Compatibilidad con el requisito condicional de ejecución \[ automática\]



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>En el caso de los juegos distribuidos en CD, DVD u otros medios extraíbles que admiten la ejecución automática, cuando el disco se inserta por primera vez, la aplicación debe ejecutar automáticamente o pedir al usuario que instale el juego. <br/>
<blockquote>
[!Note]<br />
Los programas de ejecución automática escritos para su uso en versiones de Windows anteriores a Windows Vista no deben usar el entorno de ejecución de .NET, ya que esta tecnología no se incluye con Windows XP o versiones anteriores de Windows.
</blockquote>
<br/> Para obtener más instrucciones, consulte <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun (Requisitos técnicos 3.7, Ejecución automática de soporte técnico). <br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Inserte el disco o el medio del juego.</li>
<li>Compruebe que el cuadro de diálogo instalar o ejecutar aparece automáticamente.</li>
<li>Windows Vista o Windows 7: Compruebe que el propio programa de ejecución automática del juego no pide al usuario Julia que eleve el nivel a través de credenciales de administrador.</li>
<li>Compruebe que el ejecutable De ejecución automática no necesita componentes REDIST estándar, como .NET 3.5, bibliotecas de C Run-Time, y así sucesivamente.</li>
<li>Compruebe que volver a insertar el disco en la unidad después de la instalación no hace que la instalación se vuelva a iniciar automáticamente.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a>4. Confiabilidad

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 Eliminar reinicios innecesarios



| SO                                              | Requisito                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> | Todos los instaladores de aplicaciones deben aprovechar las API de Restart Manager para evitar reinicios del sistema (consulte el [requisito 3.5).](#35-avoid-reboots-during-installation) |



 

### <a name="42-eliminate-application-verifier-failures"></a>4.2 Eliminar Application Verifier errores



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>El juego no debe generar errores en ejecución en Microsoft Application Verifier (AppVerifier), versión 4.0 o posterior, en las siguientes pruebas: <br/>
<ul>
<li>Aspectos básicos: identificadores, montones, bloqueos, memoria, TLS</li>
<li>Varios: DangerousAPIs, DirtyStacks</li>
</ul></td>
</tr>
<tr class="even">

<td>Usar herramienta: AppVerifier 4.0 (o posterior)<br/>
<ol>
<li>Instale AppVerifier.</li>
<li>Inicie AppVerifier y seleccione Archivo -> Agregar aplicación.</li>
<li>Busque el archivo ejecutable del juego, selecciónelo y haga clic en &quot; el botón &quot; Abrir.</li>
<li>En la &quot; sección &quot; Aplicaciones, seleccione el archivo ejecutable del juego.</li>
<li>En la sección Pruebas, seleccione las pruebas enumeradas anteriormente en las categorías Aspectos básicos y Varios &quot; &quot; (desactive ThreadPool y &quot; &quot; &quot; &quot; TimeRollOver) y asegúrese de que todas las demás pruebas no estén seleccionadas.</li>
<li>Inicie el juego.</li>
<li>Compruebe que el juego no genera errores cuando se ejecuta en Application Verifier.</li>
</ol>
<blockquote>
[!Note]<br />
Algunas pruebas requieren que un depurador se ejecute completamente. Esto puede requerir una versión de lanzamiento sin protección del archivo ejecutable del juego, ya que la tecnología anti-cheat/antisecuencia puede interferir con AppVerifer.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a>4.3 Compatibilidad Informe de errores de Windows



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos solo deben controlar las excepciones conocidas y esperadas, Informe de errores de Windows no deben deshabilitarse. Si se inserta un error (como una infracción de acceso) en un juego, debe permitir que Informe de errores de Windows informe del bloqueo.</td>
</tr>
<tr class="even">

<td>Herramienta de uso: subprocesos <br/>
<ul>
<li>Si la aplicación se bloquea durante las pruebas, compruebe que el juego Informe de errores de Windows correctamente y recopila datos de bloqueo.</li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Todos los archivos ejecutables (por ejemplo, .exe o .dll archivos) deben contener un nombre de producto, un nombre de empresa y una versión de archivo precisos.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Prueba manual:</dt> <dd>
<ol>
<li>Haga clic con el botón derecho en los archivos ejecutables del juego tanto en los medios de instalación como en los instalados en el disco duro del equipo.</li>
<li>Seleccione Propiedades.</li>
<li>Windows XP: haga clic en <strong>la pestaña</strong> Versión. Compruebe que los campos Nombre del producto, Nombre de la empresa y Versión de archivo están correctamente rellenados.</li>
<li>Windows Vista o Windows 7: haga clic en la <strong>pestaña</strong> Detalles. Compruebe que los campos Nombre del producto y Versión del archivo están correctamente rellenados. El nombre de la empresa no está visible en la Windows vista o Windows 7 propiedades.</li>
</ol>
</dd> <dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Prueba automatizada:</dt> <dd>
<ul>
<li>Use Microsoft Games for Windows Test Tool; vea <a href="#64-microsoft-games-for-windows-test-tool">la sección 6.4.</a></li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>La salida normal del juego no debe dar lugar a un error de excepción desconocido.</td>
</tr>
<tr class="even">

<td><ul>
<li>Después de jugar al juego para una sesión de juegos normal, compruebe que el juego no genera errores al salir.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a>5. Script de prueba de ejemplo

Este es un ejemplo de un paso de prueba típico con los requisitos de prueba anteriores como guía.

### <a name="51-tools"></a>5.1 Tools

-   Edición de 32 bits de Windows Vista SP1 o Windows 7 en una CPU amd
-   Edición de 32 bits de Windows Vista SP1 o Windows 7 en una CPU Intel
-   Edición de 64 bits de Windows Vista SP1 o Windows 7 en una CPU AMD
-   Edición de 64 bits de Windows Vista SP1 o Windows 7 en una CPU Intel
-   Edición de 32 bits Windows XP SP2 en una CPU AMD
-   Edición de 32 bits Windows XP SP2 en una CPU Intel
-   Monitor de pantalla ancha que admite 1680 1050
-   Mando Xbox 360 para Windows

### <a name="52-pre-install"></a>5.2 Preinstalación

1.  Windows Vista y Windows 7: Crear dos usuarios estándar: Jane y Toby
2.  Windows Vista y Windows 7: Asegurarse de que el control de cuentas de usuario está habilitado
3.  Creación de una instantánea previa a la instalación de System32

    1.  Crear un directorio llamado G4Wtest
    2.  Abrir una ventana de comandos (Start -> Run -> cmd)
    3.  Vaya a c: \\ windows \\ system32
    4.  Escriba dir /o:-g /o:-d >> c: \\ G4Wtest \\pregame.txt

4.  Windows Vista y Windows 7: establecido en 150 % PPP \[ 1,8\]
5.  Continuar con [la instalación](#3-installation)

### <a name="53-install"></a>5.3 Instalación

1.  Iniciar sesión como User Jane
2.  Inserte el disco del juego en la unidad de CD/DVD y compruebe que el cuadro de diálogo instalar/ejecutar aparece automáticamente \[ en la versión 3.7.\]
3.  Compruebe que el proceso de instalación del juego solicita al usuario Julia que eleve las credenciales \[ de administrador 3.2.\]
4.  Compruebe que el propio programa de ejecución automática del juego no pide al usuario Jane que eleve a través de las credenciales \[ de administrador 3.7.\]
5.  Compruebe que el juego no muestra más de un End-User licencia (CLUF) \[ 3.1\]
6.  Compruebe que el juego muestra las opciones de instalación Predeterminada, Fácil y \[ Personalizada/Avanzada 3.1\]
7.  Compruebe que la opción de instalación Predeterminada/Fácil omite todas las selecciones de entrada del usuario para el proceso de instalación (selección de la carpeta de instalación, selección de componentes, y así sucesivamente). \[ 3.1\]
8.  Compruebe que el proceso de instalación del juego no solicita la configuración del componente del sistema operativo (instalación de DirectX, bibliotecas de Run-Time C, y así sucesivamente). \[ 3.1\]
9.  Compruebe que el proceso de instalación del juego no solicita la interacción del firewall \[ 3.1\]
10. Compruebe que el proceso de instalación del juego no encuentra un error con respecto a la versión \[ 2.5 \] \[ 4.2 del sistema operativo.\]
11. Compruebe que el proceso de instalación del juego no muestra los cuadros de diálogo de controladores sin signo \[ 2.4.\]
12. Compruebe que no Windows diálogos de Resource Protection (WRP) durante el proceso de instalación \[ 3.4\]
13. Compruebe que volver a insertar el disco en la unidad después de la instalación no hace que la instalación se vuelva a iniciar automáticamente.
14. Compruebe que el juego no requiere que el sistema se reinicie después de la \[ instalación 3.5.\]
15. Compruebe que puede instalar el juego como usuario Jane \[ 3.2.\]
16. Compruebe que el juego se ejecuta automáticamente o que hay un menú del iniciador al final del proceso de instalación \[ 3.1.\]
17. Si el juego se ejecuta automáticamente después de la instalación, vaya directamente a [Runtime (Tiempo de ejecución).](#55-runtime)
18. Si el juego dejó un menú de inicio o no se pudo desinstalar, consulte la sección [Posterior a la instalación.](#54-post-install)

### <a name="54-post-install"></a>5.4 Posterior a la instalación

1.  Compruebe que el juego no coloca accesos directos de inicio en el escritorio del usuario \[ 1.1.\]
2.  Compruebe que el juego no coloca accesos directos de inicio en el menú \[ Inicio 1.1.\]
3.  Compruebe que el icono del juego se muestra en Windows Games Explorer \[ 1.1\]
4.  Compruebe que los metadatos (publicador, desarrollador, género, fecha de lanzamiento, versión) en la parte inferior se muestran y es correcto \[ 1.1.\]
5.  Compruebe que el icono del juego muestra Windows experience index (WEI) en Windows Games Explorer \[ 1.1\]
6.  Compruebe que los hipervínculos de juegos para metadatos funcionan correctamente en Windows Games Explorer \[ 1.1\]
7.  Compruebe que el juego muestra una clasificación de control parental precisa en Windows Games Explorer \[ 1.1\]
8.  Creación de una instantánea posterior a la instalación de System32

    1.  Abrir una ventana de comandos (Start -> Run -> cmd)
    2.  Vaya a c: \\ sistema \\ de Windows32
    3.  Escriba dir /o:-g /o:-d >> c: \\ G4Wtest \\postgame.txt
    4.  Compruebe que el juego no revierte ninguna versión de archivo de los archivos enumerados en los dos documentos comparando pregame.txt con postgame.txt \[ 3.6\]

9.  Continúe [con](#55-runtime) runtime

### <a name="55-runtime"></a>5.5 Runtime

1.  RUNTIME 1: si el menú de inicio está presente, inicie el juego desde allí. Si el juego se ejecutó automáticamente o se inició desde el menú del iniciador del juego después de la instalación, realice lo siguiente: Si no es así, vaya a RUNTIME 2:

    1.  Crear un perfil (si el juego lo permite)
    2.  Inicio de un nuevo juego
    3.  Guardar el juego
    4.  Salir del juego
    5.  Inicio del juego desde Games Explorer
    6.  Compruebe que el juego se inicia desde el icono 1.2 del Explorador de \[ juegos.\]
    7.  Compruebe que el juego no solicita credenciales de administrador al iniciar \[ la versión 1.2.\]
    8.  Compruebe que la cuenta 3.2 de User Jane puede acceder a los perfiles de usuario y Guardar \[ juegos.\]
    9.  Continúe con RUNTIME 3

2.  RUNTIME 2: si el juego no se ha ejecutado automáticamente ni ha mostrado un lanzamiento desde el menú del iniciador del juego, se trata de un error de \[ 3.1; sin embargo, las pruebas pueden continuar \] normalmente:

    1.  Inicio del juego desde Games Explorer
    2.  Compruebe que el juego se inicia desde el icono 1.2 del Explorador de \[ juegos.\]
    3.  Compruebe que el juego no solicita credenciales de administrador al iniciar \[ la versión 1.2.\]
    4.  Continúe con RUNTIME 3

3.  RUNTIME 3: si el juego admite un panel de juego, compruebe que el juego reconoce Mando Xbox 360 para Windows como un dispositivo de entrada \[ 1.4.\]

    1.  Si es necesario, habilite el controlador a través del menú de opciones.
    2.  Compruebe que el juego hace referencia a los botones y desencadenadores del controlador Xbox 360 nombres.
    3.  Compruebe que el juego y el sistema de menús se pueden controlar con el Mando Xbox 360 para Windows
    4.  Compruebe que el Mando Xbox 360 para Windows se comporta según los estándares aceptados.

4.  Establezca el vídeo en \[ 1.5 \] :

    1.  Compruebe que el juego se ejecuta con una resolución de relación de aspecto 4:3 (800 600 o 1024 768)
    2.  Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:9 (1280 720)
    3.  Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:10 (1680 1050, 800 480 o 1152 720).
    4.  Compruebe que el juego solicita al usuario cuándo se realiza un cambio en la resolución.
    5.  Compruebe que la pantalla vuelve a la configuración anterior si no acepta en 15 segundos.
    6.  Compruebe que el juego no extiende la imagen y, a su vez, presenta un área de vista más amplia.
    7.  Compruebe que el juego no agrega barras negras a la izquierda y derecha del área de juego.

5.  Si está disponible en la configuración del vídeo, compruebe que las opciones de representación del juego tienen como valor predeterminado Direct3D \[ 1.7; de lo contrario, continúe \] con [Pruebas automatizadas.](#58-automated-tests)
6.  Si se le solicita o si la opción está disponible, cree un perfil de usuario. Comprobar que el juego no encuentra errores al usar nombres de archivo \[ largos 2.7\]
7.  Iniciar un juego nuevo, crear un juego guardado y comprobar que el juego no encuentra errores al controlar los caracteres del sistema de archivos \[ no admitidos 2.7\]
8.  Compruebe que el juego esté correctamente alt+TABs en Windows escritorio \[ 2.6\]

    1.  Cambiar usuarios con el juego en ejecución haciendo clic en Iniciar -> Cambiar usuario
    2.  Iniciar sesión como Toby
    3.  Compruebe que el juego se inicia como User Toby mientras sigue ejecutándose como User Jane \[ 2.6.\]
    4.  Compruebe que el juego no encuentra errores para User Toby o User Jane durante el proceso de cambio de usuario \[ 2.6.\]
    5.  Compruebe que no puede escuchar audio de la sesión de juego original \[ 2.6.\]
    6.  Salir del juego
    7.  Cerrar sesión en Toby
    8.  Volver al usuario original donde se ejecuta el juego
    9.  ALT+TAB de nuevo en el juego

9.  Salir del juego
10. Vaya a [Post-Runtime](#56-post-runtime)

### <a name="56-post-runtime"></a>5.6 Post-Runtime

1.  Compruebe que el juego no genera errores al salir \[ de la versión 4.3.\]
2.  Compruebe que el juego está instalado en Archivos de \[ programa 3.3.\]
3.  Continuar con los [controles parentales](/windows)

### <a name="57-parental-controls"></a>5.7 Controles parentales

1.  Abrir controles parentales en Panel de control
2.  Compruebe que el juego muestra la clasificación de control parental precisa debajo del título del juego en Control parental Panel de control \[ 1.2\]
3.  Consulte Caso de \[ prueba 1.2 \] para ver las pruebas siguientes:

    1.  Después de establecer Controles parentales en "On", compruebe que el juego se ejecuta con esta configuración como User Jane \[ 1.2.\]
    2.  Cerrar sesión e iniciar sesión como Toby
    3.  Compruebe que el juego se ejecuta con esta configuración como User Toby \[ 1.2.\]
    4.  Cierre la sesión e inicie sesión como Julia.
    5.  En la sección Control parental, bloquee al usuario Toby para que no vea juegos de un nivel superior de ESRB desde el juego que acaba de instalar.

        Ejemplo: si el juego tiene la clasificación E, estabbúla para que Toby solo pueda jugar juegos que tienen la clasificación C.

    6.  Compruebe que el juego se ejecuta con esta configuración como User Jane \[ 1.2\]
    7.  Cierre la sesión e inicie sesión como usuario toby
    8.  Compruebe que el juego no se inicia en El usuario Toby cuando la aplicación ESRB está bloqueada por la usuario Jane \[ 1.2.\]
    9.  Cierre la sesión como usuario Toby y vuelva a iniciarla como usuario Jane.
    10. Si se ha cambiado anteriormente, restaure la configuración de ESRB.
    11. Si no hay ninguna configuración de ESRB, seleccione "Bloquear o permitir juegos específicos" y seleccione el juego por nombre.
    12. Cierre sesión como Julia y en Toby
    13. Compruebe que el juego no se inicia en User Toby cuando la aplicación EXE/Name está bloqueada por la usuario Jane \[ 1.2.\]
    14. Cierre sesión como Toby y vuelva a iniciarla como Julia.
    15. Como Julia, abra Controles de usuario -> restricciones de aplicación
    16. Haga clic en "Toby solo puede usar los programas que se permiten" y, a continuación, haga clic en Aceptar (es decir, no permitir exes)
    17. Haga clic en la casilla Desactivar todo y, a continuación, haga clic en Aceptar.
    18. Vaya a Controles de usuario \| Controles de juegos y permita el juego específico mediante la clasificación de ESRB.
    19. Cierre sesión como Julia e inicie sesión como Toby e intente jugar al juego.
    20. Compruebe que el juego NO está bloqueado y que Toby puede reproducirlo cuando "no permitir ningún archivo exe" está establecido \[ en 1.2.\]
    21. Cierre la sesión como usuario Toby y vuelva a iniciarla como usuario Jane.
    22. Vaya a Controles parentales en Panel de control quitar las restricciones.
    23. Compruebe que ambos usuarios ahora pueden jugar al juego.

4.  Continuar con las [pruebas automatizadas](#58-automated-tests)

### <a name="58-automated-tests"></a>5.8 Pruebas automatizadas

1.  Comprobación de que el juego no genera errores cuando se ejecuta en Application Verifier: consulte la documentación de la herramienta de prueba de marca \[ 4.2.\]
2.  Compruebe que los archivos ejecutables del juego contienen manifiestos; consulte la documentación de la herramienta de prueba de personalidad \[ 2.1.\]
3.  Compruebe que el manifiesto del archivo ejecutable del juego solicitadoExecutionLevel es "AsInvoker". Consulte la documentación de la herramienta de prueba de personalidad \[ 2.1.\]
4.  Continuar con [otras pruebas](#59-other-tests)

### <a name="59-other-tests"></a>5.9 Otras pruebas

1.  Compruebe que los archivos ejecutables del juego contienen una firma digital \[ 2.3.\]
2.  Compruebe que el proceso de instalación del juego se ejecuta normalmente en ediciones de 64 bits de Windows Vista o Windows 7 \[ 2.3\]
3.  Compruebe que el juego no encuentra un error como resultado de ejecutables de 16 bits en ediciones de 64 bits de Windows Vista o Windows 7 \[ 2.3\]
4.  Forzar el bloqueo de la aplicación durante las pruebas y comprobar que el juego Informe de errores de Windows correctamente y recopila datos de bloqueo \[ 4.3\]
5.  Asegúrese de que los resúmenes de archivo \[ son correctos 4.3\]

    1.  Haga clic en Start -> Computer (Inicio > equipo).
    2.  Vaya al directorio del juego.
    3.  En la ventana de búsqueda, \* escriba.dll
    4.  Para cada archivo: haga clic con el botón derecho en el archivo y haga clic en Propiedades.

        -   En Windows XP: haga clic en la pestaña Versión. Compruebe que los campos Nombre del producto, Nombre de la compañía y Versión de archivo están correctamente rellenados. \[4.3\]
        -   En Windows Vista y Windows 7: haga clic en la pestaña Detalles. Compruebe que los campos Nombre del producto y Versión de archivo están correctamente rellenados. El nombre de la empresa no está visible en Windows Vista o Windows 7 propiedades \[ de la página 4.3\]

    5.  Repita esta comprobación para los .exe archivos

6.  Inicie el juego.

    1.  Presione CTRL+ALT+SUPR.
    2.  Haga clic en la flecha "Opciones de apagado".
    3.  Haga clic en Reiniciar.
    4.  Comprobar que el juego no bloquea el apagado \[ 3.1\]

7.  Continuar a [Desinstalar](#510-uninstall)

### <a name="510-uninstall"></a>5.10 Desinstalar

-   Compruebe que el proceso de desinstalación del juego quita todos los archivos de componentes del sistema operativo instalados y no redistribuidos y borra toda la configuración \[ 3.1.\]

    -   Compruebe en Windows Vista o Windows 7 que Panel de control es la única manera de quitar el programa \[ 1.1\]

## <a name="test-tool-notes"></a>Notas de la herramienta de prueba

Estas son notas de cada una de las herramientas de prueba enumeradas en los requisitos de prueba anteriores.

### <a name="61-appverifier-40-or-higher"></a>6.1 Appverifier 4.0 (o superior)

**Caso de prueba: 2.5, 4.2**

> [!Note]  
> Algunas aplicaciones no se pueden ejecutar con AppVerifier en ejecución, debido a la protección de copia. Esto se puede resolver mediante la ejecución con una versión de lanzamiento no protegida del archivo ejecutable del juego.

 

1.  Instalación de AppVerifier 4.0 (o superior) en un equipo que ejecuta Windows XP
2.  Inicie AppVerifier y haga clic en Archivo -> Agregar aplicación
3.  Busque el archivo ejecutable del juego, selecciónelo y haga clic en Abrir.
4.  En la sección "Aplicaciones", seleccione el archivo ejecutable del juego.
5.  Seleccione las siguientes pruebas en la sección "Aspectos básicos":

    -   Asas
    -   Montones
    -   Bloqueos
    -   Memoria
    -   TLS

6.  Seleccione las siguientes pruebas en la sección "Varios":

    -   DangerousAPIs
    -   DirtyStacks

7.  Asegúrese de que no estén seleccionadas todas las demás pruebas.
8.  Iniciar el juego
9.  Juego
10. Cerrar el juego
11. En AppVerifier, seleccione Ver -> registros.
12. En la sección "Aplicaciones", seleccione el archivo de .exe aplicación.
13. En la sección "Registros", seleccione el archivo de registro y observe el recuento de errores. Si no hay errores, finalice las pruebas de AppVerifier. Si hay errores, haga clic en el botón Ver.
14. Busque gravedad="Error" en el documento (CTRL+F)
15. Creación de errores basados en la parte LayerName= del error

### <a name="62-manifest-test---mtexe"></a>6.2 Prueba de manifiesto: mt.exe

**Caso de prueba: 1.8, 2.1**

Esta herramienta se ejecuta desde un símbolo del sistema donde MT.exe se encuentra.

Ejemplo:

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  Haga clic en Start -> Run -> type cmd y haga clic en el botón Aceptar.
2.  Ejecute la mt.exe para generar un archivo .manifest para cada archivo .exe que se instala con el juego.
3.  Abra el archivo .manifest generado.
4.  Asegúrese de que .exe archivo contiene lo siguiente (solicitado:

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> El nivel de ejecución solicitado debe estar presente para cada archivo y pppAware debe estar presente para al menos el archivo ejecutable del juego.

 

### <a name="63-thread-hijacker---threadhijackerexe"></a>6.3 Subprocesos de la conversación: threadhijacker.exe

Esta herramienta se ejecuta desde un símbolo del sistema donde threadhijacker.exe se encuentra.

Ejemplo:

``` syntax
threadhijacker.exe /process:str
```

Donde str es el nombre \_ de \_program.exe

1.  En el Administrador de tareas, haga clic en la pestaña Procesos y busque el nombre del archivo ejecutable del juego.
2.  Abrir un símbolo del sistema en modo de administración
3.  Vaya al directorio donde threadhijacker.exe está
4.  Tipo: **threadhijacker.exe /process:** str, donde str es el nombre del ejecutable al que desea alcanzar

### <a name="64-microsoft-games-for-windows-test-tool"></a>6.4 Microsoft Games for Windows Test Tool

Esta herramienta se encuentra en el SDK de DirectX. Una vez instalado el SDK en un equipo, se puede colocar e instalar el instalador de la herramienta de pruebas de Games for Windows en el equipo de prueba.

Busque el instalador de Microsoft Games for Windows Test Tool en el equipo de desarrollo donde está instalado el SDK de DirectX. De forma predeterminada, se coloca en la siguiente ubicación:

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  Copie el instalador (MicrosoftGFWTestTool.msi o setup.exe) en el equipo de prueba.
2.  Ejecute al programa de instalación.
3.  Inicie Microsoft Games for Windows Test Tool.
4.  En el **campo Project lista,** reemplace **Create New Project** por el nombre del título y haga clic en Create New **(Crear nuevo).**

    Espere a que se complete la línea base.

5.  Rellene cualquier información que pueda tener en la sección **Información del** juego y haga clic en Actualizar información **del juego.**
6.  Haga clic en **la pestaña Casos de** prueba.
7.  A partir de la parte superior, continúe con los casos de prueba y haga clic **en Pasar** o **Producir** error según corresponda.

    Consulte "Escribir un error", más adelante en esta sección, para obtener más información sobre cómo incluir un error en el informe.

8.  Vuelva a la **pestaña Proyectos** después de revisar el informe (comprobando las pestañas **Informe** y **Edición de** errores).
9.  Haga clic **en Compilar informe.**

    Se abrirá una ventana cuando finalice la compilación del informe. Aquí encontrará un nombre de archivo .ZIP *nombre de proyectoreport.zip.* \_ Este archivo contiene todos los registros y resultados recopilados durante la fase de prueba.

### <a name="writing-a-bug"></a>Escribir un error

Hay dos maneras de escribir un informe de errores:  puede pasar por los casos de  prueba y hacer clic en Error cuando el título produce un error en un caso de prueba, o puede hacer clic en la pestaña Edición de errores y agregar manualmente un informe de errores.

### <a name="clicking-fail-on-a-test-case"></a>Hacer clic en Error en un caso de prueba

1.  Al hacer clic en **Error** en un caso de prueba, **la** lista desplegable Tipo de problema se establecerá automáticamente en el tipo de caso de prueba.
2.  Agregue una breve descripción al **campo Título** que describa brevemente el problema.
3.  Agregue una descripción detallada del problema al **campo Comportamiento** observado.
4.  Según corresponda, agregue lo que se esperaba (en lugar de una descripción del problema) al **campo Comportamiento esperado.**
5.  Agregue una descripción detallada de cómo reproducir el problema en el **campo Pasos de** reproducción.
6.  Cuando haya terminado, haga clic en **el botón** Guardar.

### <a name="manually-adding-a-bug"></a>Agregar manualmente un error

Este proceso es el mismo que al hacer clic en **Error,** a excepción de la lista desplegable rellenada automáticamente. En este caso, seleccione el tipo de error de TCR adecuado o seleccione **\* \* Non-TR Issue \* \*** for bugs that fall outside of the TR range but should still be reported (Problema no TR para errores que se encuentran fuera del intervalo TR pero que deben seguir siendo notificados).

## <a name="resources"></a>Recursos

<dl> <dt>

<span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Juegos para Windows: Requisitos técnicos
</dt> <dd>

[Requisitos técnicos de Games for Windows: Procedimientos recomendados para juegos en Windows XP, Windows Vista y Windows 7](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK
</dt> <dd>

[Windows Sdk](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Directrices de control de cuentas de usuario
</dt> <dd>

[Windows Requisitos de desarrollo de aplicaciones de Vista para la compatibilidad con el control de cuentas de usuario](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

</dd> <dt>

<span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Información del instalador
</dt> <dd>

[Windows Installer](../msi/windows-installer-portal.md)

</dd> <dt>

<span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Portal para desarrolladores 
</dt> <dd>

[Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Portal para desarrolladores
</dt> <dd>

[Centro para desarrolladores de DirectX](/previous-versions/windows/apps/hh452744(v=win.10))

</dd> <dt>

<span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog de Games for Windows SDK y DirectX
</dt> <dd>

[Juegos para Windows y el SDK de DirectX](https://walbourn.github.io/)

</dd> <dt>

<span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artículos adicionales de DirectX
</dt> <dd>

[Artículos técnicos de DirectX](./dx9-technical-articles.md)

</dd> </dl>

 

