---
title: 'Casos de prueba de Games for Windows: procedimientos recomendados para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8'
description: En este artículo se proporcionan casos de prueba para juegos para Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae26274f199f070ce605227fa19796716df9fbaf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078076"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Juegos para casos de prueba de Windows: prácticas recomendadas para juegos en Windows XP, Windows Vista, Windows 7 y Windows 8

En este artículo se proporcionan casos de prueba para juegos para Windows.

## <a name="how-to-use-this-article"></a>Cómo usar este artículo

Hay tres secciones principales en este artículo:

<dl> <dt>

<span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisitos de pruebas**
</dt> <dd>

Cada requisito de prueba de este documento tiene cuatro secciones principales: un título y una tabla con tres secciones destacadas (columna izquierda, superior derecha, inferior derecha).

<dl> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titulo
</dt> <dd>

Nombre del caso de prueba.

</dd> <dt>

<span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Cuadro, columna izquierda
</dt> <dd>

Nombres de los sistemas operativos a los que se aplica el caso de prueba.

</dd> <dt>

<span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Cuadro, parte superior derecha
</dt> <dd>

Breve resumen del caso de prueba.

</dd> <dt>

<span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Cuadro, parte inferior derecha
</dt> <dd>

Detalles del caso de prueba real.

</dd> </dl> </dd> <dt>

<span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Script de prueba de ejemplo**
</dt> <dd>

Esta sección es un ejemplo de la secuencia que seguiría un paso de prueba típico si usara los requisitos de prueba como guía.

</dd> <dt>

<span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Notas de la herramienta de prueba**
</dt> <dd>

Esta sección contiene notas detalladas sobre cada una de las herramientas de prueba que se usan para comprobar las condiciones superadas o erróneas en los requisitos de pruebas.

</dd> </dl>

## <a name="test-requirements"></a>Requisitos de pruebas

### <a name="1-game-requirements"></a>1. requisitos del juego

### <a name="11-windows-games-explorer"></a>Explorador de juegos de Windows 1,1



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>El juego debe estar visible en el explorador de juegos de Windows Vista y Windows 7. Cuando se selecciona, el juego también debe mostrar los metadatos correctos. La instalación no debe crear un acceso directo para iniciar el juego en el escritorio, en el menú Inicio o en cualquier otra ubicación. No se deben crear tareas ni accesos directos para quitarlos.</td>
</tr>
<tr class="even">

<td><ol>
<li>Después de instalar el juego, abra el explorador de juegos.</li>
<li>Compruebe que el icono de juego se muestra en el explorador de juegos.</li>
<li>Haga clic con el botón secundario en el icono y pruebe cada tarea de soporte & de reproducción definida por la aplicación.</li>
<li>Haga clic en el icono y compruebe que los metadatos (publicador, desarrollador, género, fecha de lanzamiento, versión) de la parte inferior se muestran y son correctos.</li>
<li>Compruebe que el icono de juego muestra información del índice de experiencia de Windows (WEI) en el explorador de juegos.</li>
<li>Compruebe que los hipervínculos de juego para metadatos funcionan correctamente en el explorador de juegos. (Si no se muestran los hipervínculos, es posible que el archivo exe no esté firmado; vea la <a href="#23-sign-files">sección 2,3</a>).</li>
<li>Compruebe que el juego muestra la clasificación de control parental exacta en el explorador de juegos. (Si dice sin clasificación, compruebe que se trata de un juego sin clasificación; de lo contrario, es un indicador de que el archivo exe no está firmado; vea la <a href="#23-sign-files">sección 2,3</a>).</li>
<li>Compruebe que el juego no coloca accesos directos de inicio en el escritorio del usuario.</li>
<li>Haga clic en Inicio-> todos los programas.</li>
<li>Compruebe que el juego no coloca accesos directos de inicio en el menú Inicio.</li>
<li>Compruebe que el juego no coloca los accesos directos de desinstalación en el menú Inicio fuera del panel de control.</li>
<li>Si el juego está distribuido digitalmente, compruebe que el proveedor de servicios aparece en el explorador de juegos de Windows.</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a>1,2 protección de la familia de Windows/control parental



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>El juego debe ejecutarse en el contexto de un &quot; usuario estándar &quot; . Los controles parentales deben ser capaces de bloquear el juego. Compruebe que GDF tiene nombres de EXE.</td>
</tr>
<tr class="even">

<td><ol>
<li>Cree una cuenta de usuario estándar en Windows Vista o Windows 7 denominada Toby. Inicio > panel de control-> agregar o quitar cuentas de usuario-> crear una cuenta nueva</li>
<li>Como Julia, desde la cuenta de administrador configura controles parentales para el juego. Inicio-> panel de control-> configurar controles parentales para cualquier usuario > Toby
<ol>
<li>Compruebe que el juego se inicia desde el icono del explorador de juegos.</li>
<li>Compruebe que el juego muestra la clasificación de control parental exacta debajo del título del juego en el panel de control de controles parentales.</li>
<li>Antes de aplicar controles parentales, compruebe que el juego no solicita credenciales de administrador al iniciarse.</li>
<li>Establezca controles parentales en &quot; activado &quot; .</li>
<li>En la sección configuración de Windows, haga clic en juegos.</li>
<li>Haga clic en Aceptar (el valor debe ser ahora &quot; AO/todos los juegos &quot; ).</li>
<li>Compruebe que el juego se ejecuta con esta configuración como User Jane.</li>
<li>Cierre la sesión como Julia e inicie sesión como Toby.</li>
<li>Compruebe que el juego se ejecuta con esta configuración como User Toby.</li>
<li>Cierre la sesión como Toby e inicie sesión como Julia.</li>
<li>Vuelva a la pantalla anterior y seleccione &quot; establecer clasificaciones de &quot; juegos.</li>
<li><p>Seleccione una clasificación inferior a la clasificación de ESRB del juego.</p>
<blockquote>
[!Note]<br />
Si el juego no está clasificado, omita este paso y vaya a la siguiente parte de esta prueba. Puede que sea necesario elegir otro sistema de clasificación para encontrar una clasificación de juego, en función de la configuración regional de idioma de la SKU que se está probando.
</blockquote>
<p><br/></p></li>
<li>Cierre la sesión como Julia e inicie sesión como Toby.</li>
<li>Compruebe que el juego no se inicia para el usuario Toby cuando ESRB está bloqueado por el usuario Jane.</li>
<li>Cierre la sesión como Toby e inicie sesión como Julia.</li>
<li>Si ha cambiado previamente, restaure la configuración de ESRB.</li>
<li>Si no hay ninguna configuración de ESRB, seleccione &quot; bloquear o permitir juegos específicos &quot; y seleccione el juego por nombre.</li>
<li>Cierre la sesión como Julia e inicie sesión como Toby.</li>
<li>Compruebe que el juego no se inicia para el usuario Toby cuando el usuario Julia bloquea el archivo EXE/Name.</li>
<li>Cierre la sesión como Toby y vuelva a iniciarla como Julia.</li>
<li>Como Julia, abra controles de usuario-> restricciones de la aplicación.</li>
<li>Haga clic en &quot; Toby solo puede usar los programas que se permiten &quot; y hacer clic en Aceptar (es decir, no permitir ningún exe).</li>
<li>Vaya a controles de usuario | Controla los juegos y permite el juego específico con la Clasificación ESRB.</li>
<li>Cierre la sesión como Julia e inicie sesión como Toby e intente jugar al juego.</li>
<li>Compruebe que el juego no está bloqueado y que Toby puede reproducirlo cuando &quot; no &quot; se ha establecido permitir ningún exe.</li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a>1,3 juegos guardados enriquecidos de Windows Vista

Este requisito se ha retirado.

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 Xbox 360 Common Controller for Windows \[ requisito condicional\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos que admiten controladores de controlador para juegos deben admitir la controladora Xbox 360 para Windows mediante la API de XInput. Todas las referencias a los botones y desencadenadores de controlador comunes deben usar los nombres de Xbox 360.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inicie el juego.</li>
<li>Vaya a las opciones del controlador. **</li>
<li>Compruebe que el juego reconoce el controlador Xbox 360 para Windows como dispositivo de entrada.</li>
<li>Juega el juego y comprueba que el juego y el sistema de menús se pueden controlar con el controlador Xbox 360 para Windows.</li>
<li>Compruebe que la controladora Xbox 360 para Windows se comporta de acuerdo con los estándares aceptados. (B para atrás, para aceptar, iniciar para en el menú juego/pausar o aceptar, etc.)</li>
<li>Compruebe que el juego hace referencia a los botones del controlador y a los desencadenadores mediante los nombres de Xbox 360.</li>
</ol>
<br/>
<blockquote>
[!Note]<br />
Si el juego no es compatible con un dispositivo de juego o solo es compatible con el teclado o el mouse, omita este caso de prueba.
</blockquote>
<br/> * * La configuración del controlador podría encontrarse fuera del juego. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a>1,5 varias relaciones y resoluciones de aspecto



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>El juego debe admitir al menos las siguientes proporciones de aspecto y las resoluciones de pantalla asociadas: <br/>
<ul>
<li>4:3 &quot; normal &quot; (800 600 o 1024 768)</li>
<li>&quot;pantalla panorámica 16:9 &quot; (1280 720)</li>
<li>16:10 &quot; pantalla panorámica &quot; (1152 720, 1680 1050 o 800 480)</li>
</ul></td>
</tr>
<tr class="even">

<td>Busque las opciones de vídeo del juego (esto puede estar fuera del juego).<br/>
<blockquote>
[!Note]<br />
Las siguientes pruebas deben realizarse en un monitor de pantalla panorámica.
</blockquote>
<br/>
<ol>
<li>En la sección resolución de vídeo, seleccione 800 600 o 1024 768.</li>
<li>Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 4:3.</li>
<li>En la sección resolución de vídeo, seleccione 1280 720.</li>
<li>Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:9.</li>
<li>En la sección resolución de vídeo, seleccione 1680 1050, 800 480 o 1152 720.</li>
<li>Compruebe que el juego se ejecuta con una resolución de relación de aspecto de 16:10.</li>
<li>Compruebe que el juego no estire la imagen y, a su vez, presente un área más amplia de la vista.</li>
<li>Compruebe que el juego solicita al usuario cuando se realiza un cambio en la resolución.</li>
<li>Si el usuario no acepta en 15 segundos, compruebe que la pantalla revierte a la configuración anterior.</li>
<li>Compruebe que el juego no agrega barras negras a la izquierda y a la derecha del área de juego. (En este caso, verá que el área de juego sigue teniendo una relación 4:3 en el centro de la pantalla).</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a>1,6 Windows Media Center

Este requisito se ha retirado.

### <a name="17-direct3d-conditional-requirement"></a>1,7 \[ requisito condicional de Direct3D\]



|                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> Windows XP<br/> | Si el juego usa Direct3D, la versión mínima admitida debe ser Direct3D 9 y Direct3D debe ser el valor predeterminado de cualquier opción de configuración de pantalla.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|                                                                     | <dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> <dd> Inicie el juego. En las opciones de vídeo, compruebe si hay opciones de representación, D3D y/o OpenGL. Si es así, compruebe que las opciones de representación de juego tienen como valor predeterminado Direct3D. Si no puede comprobar que D3D9 es la versión de DirectX que se está usando, continúe con la prueba automatizada. <br/> </dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> <dd> Herramienta de uso: Depends.exe <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a>1,8 habilitar reconocimiento de PPP alto



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Los juegos y sus instaladores deben ejecutarse correctamente sin problemas visuales cuando está habilitado el escalado de PPP.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> <dd>
<ol>
<li>Establezca el sistema en PPP 150%: <br/> Windows Vista: panel de control: personalización, ajustar tamaño de fuente (PPP), PPP personalizado. Establézcalo en 150%.<br/> Windows 7: panel de control: mostrar, establecer en un valor mayor que 150%.<br/></li>
<li>Ejecute el proceso de instalación y el juego para comprobar que no hay problemas con pantallas o cuadros de diálogo recortados.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> <dd> Compruebe que el elemento <dpiAware>true</dpiAware> está incluido en el manifiesto incrustado.<br/> Herramienta de uso: Mt.exe <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a>2. seguridad y compatibilidad

### <a name="21-follow-user-account-control-guidelines"></a>2,1 Siga las directrices de control de cuentas de usuario



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Todos los archivos ejecutables (. La extensión EXE) que se incluye con una aplicación debe tener un manifiesto incrustado que defina su nivel de ejecución:
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
En el caso de los juegos y los instaladores de juegos, uiAccess siempre debe establecerse en &quot; false &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Compruebe que los archivos ejecutables del juego contienen manifiestos.</li>
<li>Compruebe que el archivo ejecutable del juego requestedExecutionLevel es &quot; asInvoker &quot; .</li>
</ol>
Herramienta de uso: Mt.exe <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a>2,2 compatibilidad con versiones x64 de Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Para mantener la compatibilidad con las versiones x64 de Windows: <br/>
<ul>
<li>Los instaladores de títulos y títulos no deben contener código de 16 bits ni confiar en ningún componente de 16 bits.</li>
<li>Si el juego depende de los controladores en modo kernel para su funcionamiento, las versiones x64 de estos controladores deben estar disponibles. La configuración del juego debe detectar e instalar los controladores y componentes adecuados para las ediciones de 64 bits de Windows.</li>
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
<li>Ejecute el juego en las ediciones de 64 bits de Windows. Compruebe que el proceso de instalación del juego se ejecuta normalmente en las ediciones de 64 bits de Windows Vista o Windows 7.</li>
<li>Compruebe que el juego no encuentra un error como resultado de los ejecutables de 16 bits en las ediciones de 64 bits de Windows Vista o Windows 7. El error hará mención a la aplicación de 16 bits en la ventana de error.</li>
<li>Si el juego tiene un archivo ejecutable nativo de 64 bits, úselo también.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a>Archivos de firma de 2,3



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Todos los archivos de código ejecutable (por ejemplo, las extensiones. exe y. dll) deben estar firmados con un certificado Authenticode. <br/> Si está utilizando Windows Installer, los archivos de paquete del instalador (archivos. msi) deben estar firmados. <br/></td>
</tr>
<tr class="even">

<td>Prueba manual<br/>
<ol>
<li>Navegue hasta el directorio del juego.</li>
<li>Busque todos los archivos. exe y. dll.</li>
<li>Haga clic con el botón secundario en propiedades en cada archivo.</li>
<li>Compruebe que los archivos ejecutables del juego contienen una firma digital.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a>Controladores de firma de 2,4



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Cualquier controlador en modo kernel instalado por el juego debe estar firmado con un certificado Authenticode válido públicamente. <br/> Cualquier controlador de dispositivo de hardware en modo de kernel instalado por el juego debe tener una firma de Microsoft obtenida a través del programa de calidad de hardware de Windows (WHQL) o la firma de confiabilidad de controlador (DRS). <br/></td>
</tr>
<tr class="even">

<td>Prueba manual<br/>
<ol>
<li>Instale el juego.</li>
<li>Compruebe que el proceso de instalación del juego no muestra cuadros de diálogo de controladores sin firmar.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a>2,5 realizar la comprobación de versiones correctamente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos no deben ejecutarse en sistemas operativos futuros, tal como se indica en los cambios en el número de versión de Windows, a menos que el contrato de licencia para el usuario final prohíba su uso en sistemas operativos futuros. Si se supone que el juego produce un error, debe hacerlo correctamente mostrando un mensaje al usuario.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> <dd>
<ol>
<li>Instale el juego en Windows XP, en las ediciones de 32 bits de Windows Vista y Windows 7, y en las ediciones de 64 bits de Windows Vista y Windows 7.</li>
<li>Compruebe que el proceso de instalación del juego no encuentra un error relacionado con la versión del sistema operativo.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Prueba automatizada</dt> <dd> Herramienta de uso: comprobador de aplicaciones<br/>
<ol>
<li>Inicie comprobador de aplicaciones.</li>
<li>Habilite la prueba Compatibility: HighVersionLie después de seleccionar el INSTALL.EXE.</li>
<li>Instale el juego y asegúrese de que no bloquee la instalación en función de la versión del sistema operativo.</li>
<li>Habilite la prueba Compatibility: HighVersionLie después de seleccionar el GAME.EXE.</li>
<li>Ejecute el juego y asegúrese de que no bloquee la ejecución en función de la versión del sistema operativo.</li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a>2,6 compatibilidad con sesiones de usuario simultáneas



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos deben admitir escenarios estándar de multitarea de Windows.</td>
</tr>
<tr class="even">

<td>Cree una cuenta de usuario estándar en Windows Vista o Windows 7 denominada Toby. Inicio > panel de control-> agregar o quitar cuentas de usuario-> crear una cuenta nueva <br/>
<ol>
<li>Inicie el juego como User Jane.</li>
<li>Presione ALT + TAB para volver al escritorio.</li>
<li>Compruebe que el juego está correctamente ALT + tabulaciones en el escritorio de Windows.</li>
<li>Haga clic en Inicio-> [flecha a la derecha de bloquear]-> cambiar de usuario.</li>
<li>Inicie sesión como usuario Toby.</li>
<li>Compruebe que el juego se inicia como User Toby mientras sigue ejecutándose como User Jane.</li>
<li>Compruebe que el juego no encuentra errores para el usuario Toby o el usuario Julia durante el proceso de cambio de usuario.</li>
<li>Si puede iniciar otra sesión de juego, compruebe que no puede oír el audio de la sesión de juego original.</li>
<li>Cierre el juego y vuelva al usuario y el juego originales.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a>2,7 compatibilidad con nombres largos



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Si un juego admite el guardado de archivos, debe poder guardar archivos que tengan nombres y rutas de acceso largos. El juego debe administrar correctamente caracteres especiales del sistema de archivos, como \/: *? &quot; < o > en los campos de entrada del usuario que se usan para crear nombres de archivo o rutas de acceso.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inicie el juego.</li>
<li>Inicie un nuevo juego.</li>
<li>Guarde el juego. Durante el proceso de almacenamiento, compruebe que el juego se guarda con el nombre guardar: mi primer juego guardar.</li>
<li>Vuelva al menú principal.</li>
<li>Intente cargar el juego recién guardado.</li>
<li>Compruebe que el juego no encuentra errores al controlar caracteres del sistema de archivos no admitidos, como \/: *? &quot; < o > si el juego lo permite, asigne un nombre al juego guardado.</li>
<li>Si el usuario puede asignar un nombre a su perfil o a caracteres o guardar juegos, compruebe que el juego no detecta errores al usar nombres de archivo largos aquí también.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a>3. instalación

### <a name="31-easy-install"></a>Instalación sencilla de 3,1



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos con una instalación tradicional deben proporcionar una ruta de acceso simplificada en la interfaz de usuario del programa de instalación.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inserte el disco del juego.</li>
<li>Compruebe que el juego no muestra más de un End-User contrato de licencia (CLUF).</li>
<li>Si el juego admite una opción de instalación personalizada o avanzada, compruebe que esta opción es accesible durante el proceso de instalación.</li>
<li>Compruebe que la opción de instalación predeterminada omite todas las selecciones de entrada del usuario para el proceso de instalación (selección de carpeta de instalación, selección de componentes, etc.).</li>
<li>Compruebe que el proceso de instalación del juego no solicita la instalación de los componentes del sistema operativo (instalación de DirectX, tiempos de ejecución de Visual C, etc.).</li>
<li>Compruebe que el proceso de instalación del juego no solicita interacción con el firewall.</li>
<li>Compruebe que el juego se ejecuta automáticamente o que hay un menú del iniciador al final del proceso de instalación.</li>
<li>Compruebe que el proceso de desinstalación de juegos quita todos los archivos de componentes del sistema operativo instalados y no redistribuidos y borra todas las opciones de configuración. No es necesario limpiar todos los datos y la configuración de cada usuario (por ejemplo, los juegos guardados).</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a>3,2 compatibilidad con el control de cuentas de usuario para la instalación



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>El instalador del juego no debe asumir que se esté ejecutando en el mismo contexto que el usuario. Por tanto, los juegos deben realizar tareas por usuario en la primera ejecución de forma independiente de la instalación.</td>
</tr>
<tr class="even">

<td><ol>
<li>Compruebe que puede instalar el juego como User Jane. (Esto requerirá derechos elevados durante el proceso de instalación y configuración).</li>
<li>Compruebe que el proceso de instalación de juegos solicita al usuario Jane que eleve a través de las credenciales de administrador. (El mensaje de elevación se mostrará cuando el usuario intente instalar).</li>
<li>Optar por la ejecución automática del juego al final de la instalación, si aún no lo hace, o iniciarlo desde el menú que aparece.</li>
<li>Una vez en el juego, cree un nuevo perfil, juegue y guarde un juego.</li>
<li>Salga del juego.</li>
<li>Reinicie el juego y compruebe que la cuenta de usuario Jane puede tener acceso a los perfiles de usuario y a los juegos guardados.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a>3,3 instalar en carpetas correctas



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>De forma predeterminada, los juegos se deben instalar en la carpeta archivos de programa. Los datos de usuario se deben escribir en la primera ejecución y no durante la instalación.</td>
</tr>
<tr class="even">

<td><ol>
<li>Instale el juego con el tipo de instalación predeterminado.</li>
<li>Compruebe que el juego se ha instalado en los archivos de programa.</li>
</ol>
<blockquote>
[!Note]<br />
Si se produce un error en esta prueba, compruebe que el juego esté diseñado para instalarse para todos los usuarios. Si es así, se trata de un error.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a>3,4 instalar los recursos de Windows correctamente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Las aplicaciones no deben intentar instalar archivos o claves del registro protegidas por Protección de recursos de Windows (WRP).</td>
</tr>
<tr class="even">

<td><ul>
<li>Compruebe que no aparece ningún cuadro de diálogo de Protección de recursos de Windows WRP durante el proceso de instalación.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a>3,5 evitar reinicios durante la instalación



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>El instalador de juegos no debe suponer que la instalación de los componentes de Windows de los paquetes de redistribución requiere un reinicio, a menos que el reinicio se indique mediante un resultado devuelto o la documentación de Microsoft.</td>
</tr>
<tr class="even">

<td><ol>
<li>Instale el juego.</li>
<li>Compruebe que el juego no requiere que el sistema se reinicie después de la instalación.</li>
</ol>
<blockquote>
[!Note]<br />
Si una actualización de Microsoft System Update Redist requiere un reinicio, realice lo siguiente: complete la instalación del juego, desinstale el juego y vuelva a instalar el juego una segunda vez. El proceso de instalación del juego no debe requerir un reinicio en esta segunda instalación.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a>3,6 usar el control de versiones de archivos correctamente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>El programa de instalación del juego debe comprobar correctamente para asegurarse de que las versiones más recientes del archivo estén instaladas. La instalación de un juego nunca debe retrasar los archivos que no genere o que compartan las aplicaciones que no genere.</td>
</tr>
<tr class="even">

<td><ol>
<li>Antes de instalar el juego, cree una instantánea previa a la instalación de system32.<br/>
<ol>
<li>Cree un directorio denominado G4Wtest.</li>
<li>Abra una ventana de comandos (Inicio > ejecutar > cmd).</li>
<li>Vaya a c:\windows\system32.</li>
<li>Escriba dir/o:-g/o:-d >> c:\G4Wtest\pregame.txt.</li>
</ol></li>
<li>Cree una instantánea posterior a la instalación de system32. <br/>
<ol>
<li>Abra una ventana de comandos (Inicio > ejecutar > cmd).</li>
<li>Vaya a c:\windows\system32.</li>
<li>Escriba dir/o:-g/o:-d >> c:\G4Wtest\postgame.txt.</li>
<li>Compruebe que el juego no reproduce las versiones de archivo de los archivos que el juego no produjo (... de los archivos enumerados en los dos documentos comparando pregame.txt con postgame.txt).</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a>3,7 compatibilidad con el requisito condicional de ejecución automática \[\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>En el caso de los juegos distribuidos en CD, DVD u otros medios extraíbles que admitan la ejecución automática, cuando se inserte el disco por primera vez, la aplicación debe ejecutarse automáticamente o solicitar al usuario que instale el juego. <br/>
<blockquote>
[!Note]<br />
Los programas de ejecución automática que se escribieron para usarse en versiones de Windows anteriores a Windows Vista no deben usar el tiempo de ejecución de .NET, ya que esta tecnología no se incluye con Windows XP o versiones anteriores de Windows.
</blockquote>
<br/> Para obtener más información, consulte <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">juegos para Windows requisitos técnicos</a> 3,7, compatibilidad con la ejecución automática. <br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Inserte el disco de juego o el medio.</li>
<li>Compruebe que el cuadro de diálogo instalar/ejecutar aparece automáticamente.</li>
<li>Windows Vista o Windows 7: Compruebe que el programa de ejecución automática del juego no solicita al usuario Jane que eleve a través de las credenciales de administrador.</li>
<li>Compruebe que el ejecutable de ejecución automática no necesita componentes de distribución no integrados, como .NET 3,5, C Run-Time bibliotecas, etc.</li>
<li>Compruebe que al volver a insertar el disco en la unidad después de la instalación no se inicia automáticamente la instalación.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a>4. confiabilidad

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 eliminación de los reinicios innecesarios



|                                               |                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> | Todos los instaladores de aplicaciones deben aprovechar las API del administrador de reinicio para evitar reinicios del sistema (consulte el [requisito 3,5](#35-avoid-reboots-during-installation)). |



 

### <a name="42-eliminate-application-verifier-failures"></a>4,2 eliminación de errores de comprobador de aplicaciones



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>El juego no debe generar ningún error que se ejecute en Microsoft comprobador de aplicaciones (AppVerifier), versión 4,0 o posterior, en las siguientes pruebas: <br/>
<ul>
<li>Aspectos básicos: identificadores, montones, bloqueos, memoria, TLS</li>
<li>Varios: DangerousAPIs, DirtyStacks</li>
</ul></td>
</tr>
<tr class="even">

<td>Herramienta de uso: AppVerifier 4,0 (o posterior)<br/>
<ol>
<li>Instale AppVerifier.</li>
<li>Inicie AppVerifier y seleccione Archivo-> agregar aplicación.</li>
<li>Busque el archivo ejecutable del juego, selecciónelo y haga clic en el &quot; &quot; botón abrir.</li>
<li>En la &quot; &quot; sección aplicaciones, seleccione el archivo ejecutable del juego.</li>
<li>En la &quot; sección de pruebas &quot; , seleccione las pruebas indicadas anteriormente en las categorías &quot; conceptos básicos &quot; y &quot; varios &quot; (desactive ThreadPool y TimeRollOver) y asegúrese de que las demás pruebas no estén seleccionadas.</li>
<li>Inicie el juego.</li>
<li>Compruebe que el juego no genera errores cuando se ejecuta en comprobador de aplicaciones.</li>
</ol>
<blockquote>
[!Note]<br />
Algunas pruebas requieren que se ejecute completamente el depurador. Esto puede requerir una versión de lanzamiento no protegida del archivo ejecutable del juego, ya que la tecnología antitrampa/antipiratería puede interferir con el AppVerifer.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a>4,3 compatibilidad Informe de errores de Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Los juegos deben controlar solo las excepciones conocidas y esperadas, y Informe de errores de Windows no deben deshabilitarse. Si se inserta un error (por ejemplo, una infracción de acceso) en un juego, debe permitir que Informe de errores de Windows informe del bloqueo.</td>
</tr>
<tr class="even">

<td>Herramienta de uso: secuestrador de subprocesos <br/>
<ul>
<li>Si la aplicación se bloquea mientras se prueba, compruebe que el juego se muestre Informe de errores de Windows correctamente y recopile datos de bloqueo.</li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Todos los archivos ejecutables (por ejemplo, archivos. exe o. dll) deben contener un nombre de producto exacto, el nombre de la compañía y la versión del archivo.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Prueba manual:</dt> <dd>
<ol>
<li>Haga clic con el botón secundario en los archivos ejecutables del juego en el medio de instalación y en los instalados en el disco duro del equipo.</li>
<li>Seleccione Propiedades.</li>
<li>Windows XP: haga clic en la pestaña <strong>versión</strong> . Compruebe que los campos nombre de producto, nombre de la compañía y versión del archivo estén rellenados correctamente.</li>
<li>Windows Vista o Windows 7: haga clic en la pestaña <strong>detalles</strong> . Compruebe que los campos nombre del producto y versión del archivo estén rellenados correctamente. El nombre de la compañía no es visible en la página de propiedades de Windows Vista o Windows 7.</li>
</ol>
</dd> <dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Prueba automatizada:</dt> <dd>
<ul>
<li>Usar la herramienta Microsoft Games for Windows Test; Vea la <a href="#64-microsoft-games-for-windows-test-tool">sección 6,4</a>.</li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>La salida normal del juego no debe producir un error de excepción desconocido.</td>
</tr>
<tr class="even">

<td><ul>
<li>Después de reproducir el juego para una sesión de juego normal, compruebe que el juego no genera errores al salir.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a>5. script de prueba de ejemplo

Este es un ejemplo de un paso de prueba típico que usa los requisitos de prueba anteriores como guía.

### <a name="51-tools"></a>5,1 herramientas

-   edición de 32 bits de Windows Vista SP1 y/o Windows 7 en una CPU AMD
-   edición de 32 bits de Windows Vista SP1 y/o Windows 7 en una CPU de Intel
-   edición de 64 bits de Windows Vista SP1 y/o Windows 7 en una CPU AMD
-   edición de 64 bits de Windows Vista SP1 y/o Windows 7 en una CPU de Intel
-   edición de 32 bits de Windows XP SP2 en una CPU AMD
-   edición de 32 bits de Windows XP SP2 en una CPU de Intel
-   Monitor de pantalla ancha compatible con 1680 1050
-   Controladora Xbox 360 para Windows

### <a name="52-pre-install"></a>5,2 preinstalación

1.  Windows Vista y Windows 7: crear dos usuarios estándar: Julia y Toby
2.  Windows Vista y Windows 7: comprobación de que el control de cuentas de usuario está habilitado
3.  Crear una instantánea previa a la instalación de system32

    1.  Cree un directorio denominado G4Wtest
    2.  Abrir una ventana de comandos (Inicio > ejecutar > cmd)
    3.  Vaya a c: \\ Windows \\ system32
    4.  Escriba dir/o:-g/o:-d >> c: \\ G4Wtest \\pregame.txt

4.  Windows Vista y Windows 7: establezca en 150% DPI \[ 1,8\]
5.  Continuar con la [instalación](#3-installation)

### <a name="53-install"></a>instalación de 5,3

1.  Iniciar sesión como usuario Julia
2.  Inserte el disco del juego en la unidad de CD/DVD, compruebe que el cuadro de diálogo instalar/ejecutar aparece automáticamente \[ 3,7\]
3.  Compruebe que el proceso de instalación de juego solicita al usuario Julia que eleve las credenciales de administrador \[ 3,2\]
4.  Compruebe que el programa de ejecución automática del juego no solicita al usuario Jane que eleve a través de las credenciales de administrador \[ 3,7\]
5.  Compruebe que el juego no muestra más de un End-User contrato de licencia (EULA) \[ 3,1\]
6.  Compruebe que el juego muestra opciones de instalación predeterminadas, sencillas y personalizadas y avanzadas \[ 3,1\]
7.  Compruebe que la opción de instalación predeterminada o fácil omite todas las selecciones de entrada del usuario para el proceso de instalación (selección de carpeta de instalación, selección de componentes, etc.) \[ . 3,1\]
8.  Compruebe que el proceso de instalación del juego no solicita la instalación de los componentes del sistema operativo (instalación de DirectX, bibliotecas de C Run-Time, etc.) \[ 3,1\]
9.  Compruebe que el proceso de instalación del juego no solicita la interacción con el Firewall \[ 3,1\]
10. Compruebe que el proceso de instalación del juego no encuentra un error relacionado con la versión del sistema operativo \[ 2,5 \] \[ 4,2\]
11. Compruebe que el proceso de instalación del juego no muestra cuadros de diálogo de controladores sin firmar \[ 2,4\]
12. Compruebe que no aparece ningún cuadro de diálogo de Protección de recursos de Windows (WRP) durante el proceso de instalación \[ 3,4\]
13. Compruebe que la reinserción del disco en la unidad después de la instalación no hace que la instalación se inicie automáticamente de nuevo.
14. Comprobar que el juego no requiere que el sistema se reinicie después de la instalación \[ 3,5\]
15. Compruebe que puede instalar el juego como usuario Jane \[ 3,2\]
16. Compruebe que el juego se ejecuta automáticamente o que hay un menú del iniciador al final del proceso de instalación \[ 3,1\]
17. Si el juego se ejecuta automáticamente después de la instalación, vaya al [tiempo de ejecución](#55-runtime) .
18. Si el juego dejó un menú de inicio o no se pudo desinstalar, consulte la sección [posterior a la instalación](#54-post-install) .

### <a name="54-post-install"></a>5,4 posterior a la instalación

1.  Compruebe que el juego no coloca accesos directos de inicio en el escritorio de usuario \[ 1,1\]
2.  Compruebe que el juego no coloca accesos directos de inicio en el menú Inicio \[ 1,1\]
3.  Comprobar que el icono de juego aparece en el explorador de juegos de Windows \[ 1,1\]
4.  Compruebe que los metadatos (publicador, desarrollador, género, fecha de lanzamiento, versión) de la parte inferior se muestran y son correctos \[ 1,1\]
5.  Compruebe que el icono de juego muestra información de Windows Experience index (WEI) en el explorador de juegos de Windows \[ 1,1\]
6.  Comprobar que los hipervínculos de juego para metadatos funcionan correctamente en el explorador de juegos de Windows \[ 1,1\]
7.  Compruebe que el juego muestra la clasificación de control parental exacta en el explorador de juegos de Windows \[ 1,1\]
8.  Crear una instantánea posterior a la instalación de system32

    1.  Abrir una ventana de comandos (Inicio > ejecutar > cmd)
    2.  Vaya a c: \\ Windows \\ system32
    3.  Escriba dir/o:-g/o:-d >> c: \\ G4Wtest \\postgame.txt
    4.  Compruebe que el juego no retrase las versiones de archivo de los archivos enumerados en los dos documentos comparando pregame.txt con postgame.txt \[ 3,6\]

9.  Continuar en [tiempo de ejecución](#55-runtime)

### <a name="55-runtime"></a>tiempo de ejecución de 5,5

1.  Tiempo de ejecución 1: Si el menú Inicio está presente, inicie el juego desde allí. Si el juego se ejecutó automáticamente o se inició desde el menú del selector de juegos después de la instalación, realice lo siguiente: Si no es así, vaya al tiempo de ejecución 2:

    1.  Crear un perfil (si el juego lo permite)
    2.  Iniciar un nuevo juego
    3.  Guardar el juego
    4.  Salir del juego
    5.  Iniciar el juego desde el explorador de juegos
    6.  Compruebe que el juego se inicia desde el icono del explorador de juegos \[ 1,2\]
    7.  Compruebe que el juego no solicita credenciales de administrador en el inicio \[ 1,2\]
    8.  Compruebe que se puede tener acceso a los perfiles de usuario y guardar los juegos mediante la cuenta de usuario Jane \[ 3,2\]
    9.  Continuar en tiempo de ejecución 3

2.  Tiempo de ejecución 2: Si el juego no se ejecutó automáticamente o muestra un inicio en el menú del selector de juegos, se trata de un error de \[ 3,1 \] ; sin embargo, las pruebas pueden continuar normalmente:

    1.  Iniciar el juego desde el explorador de juegos
    2.  Compruebe que el juego se inicia desde el icono del explorador de juegos \[ 1,2\]
    3.  Compruebe que el juego no solicita credenciales de administrador en el inicio \[ 1,2\]
    4.  Continuar en tiempo de ejecución 3

3.  Tiempo de ejecución 3: Si el juego es compatible con un panel de juego, compruebe que el juego reconoce la controladora Xbox 360 para Windows como dispositivo de entrada \[ 1,4\]

    1.  Si es necesario, habilite el controlador a través del menú opciones.
    2.  Comprobar que el juego hace referencia a los botones del controlador y a los desencadenadores mediante los nombres de Xbox 360
    3.  Comprobar que el juego y el sistema de menús se pueden controlar con la controladora Xbox 360 para Windows
    4.  Compruebe que la controladora Xbox 360 para Windows se comporta de acuerdo con los estándares aceptados.

4.  Establezca el vídeo en \[ 1,5 \] :

    1.  Compruebe que el juego se ejecuta con una resolución de relación de aspecto 4:3 (800 600 o 1024 768).
    2.  Compruebe que el juego se ejecuta con una resolución de relación de aspecto 16:9 (1280 720).
    3.  Compruebe que el juego se ejecuta con una resolución de relación de aspecto 16:10 (1680 1050, 800 480 o 1152 720)
    4.  Comprobar que el juego solicita al usuario cuando se realiza un cambio en la resolución
    5.  Compruebe que la pantalla revierte a la configuración anterior si no acepta en 15 segundos.
    6.  Compruebe que el juego no estire la imagen y, a su vez, presente un área más amplia de la vista
    7.  Comprobar que el juego no agrega barras negras a la izquierda y a la derecha del área de juego

5.  Si está disponible en la configuración de vídeo, compruebe que las opciones de representación de juego tienen como valor predeterminado Direct3D \[ 1,7 \] ; de lo contrario, continúe con las [pruebas automatizadas](#58-automated-tests) .
6.  Si se le solicita o si la opción está disponible, cree un perfil de usuario. Compruebe que el juego no encuentra errores al usar nombres de archivo largos \[ 2,7\]
7.  Inicie un nuevo juego, cree un juego y compruebe que el juego no encuentre errores al controlar los caracteres del sistema de archivos no admitidos \[ 2,7\]
8.  Compruebe que el juego está correctamente ALT + pestañas en el escritorio de Windows \[ 2,6\]

    1.  Cambiar a los usuarios con el juego en ejecución haciendo clic en Inicio-> cambiar usuario
    2.  Iniciar sesión como Toby
    3.  Comprobar que el juego se inicia como usuario Toby mientras se sigue ejecutando como usuario Jane \[ 2,6\]
    4.  Compruebe que el juego no encuentra errores para el usuario Toby o el usuario Julia durante el proceso de cambio de usuario \[ 2,6\]
    5.  Compruebe que no puede oír el audio de la sesión de juego original \[ 2,6\]
    6.  Salir del juego
    7.  Cerrar sesión Toby
    8.  Vuelva al usuario original en el que se está ejecutando el juego
    9.  Presione ALT + TAB para volver al juego

9.  Salir del juego
10. Continuar en [el tiempo de ejecución](#56-post-runtime)

### <a name="56-post-runtime"></a>5,6 posterior al tiempo de ejecución

1.  Compruebe que el juego no genera errores al salir \[ 4,3\]
2.  Comprobar que el juego está instalado en los archivos de programa \[ 3,3\]
3.  Continuar con el [control parental](/windows)

### <a name="57-parental-controls"></a>Controles parentales de 5,7

1.  Abrir controles parentales en el panel de control
2.  Compruebe que el juego muestra la clasificación de control parental exacta debajo del título del juego en el panel de control de controles parentales \[ 1,2\]
3.  Vea el caso \[ de prueba 1,2 \] para las siguientes pruebas:

    1.  Después de establecer el control parental en "ON", compruebe que el juego se ejecuta con esta configuración como usuario Jane \[ 1,2\]
    2.  Cerrar sesión e iniciar sesión como Toby
    3.  Compruebe que el juego se ejecuta con esta configuración como usuario Toby \[ 1,2\]
    4.  Cerrar sesión e iniciar sesión como Julia
    5.  En la sección Control parental, bloquee la Toby del usuario para ver los juegos de un ESRB de nivel superior y superior del juego que acaba de instalar.

        Ejemplo: Si el juego tiene la clasificación E, establézcalo de modo que Toby solo pueda jugar a juegos con la clasificación C

    6.  Compruebe que el juego se ejecuta con esta configuración como usuario Jane \[ 1,2\]
    7.  Cerrar sesión e iniciar sesión como usuario Toby
    8.  Compruebe que el juego no se inicia en el usuario Toby cuando ESRB está bloqueado por el usuario Jane \[ 1,2\]
    9.  Cerrar sesión como usuario Toby y volver a iniciar como usuario Julia
    10. Si ha cambiado previamente, restaure la configuración de ESRB
    11. Si no hay ninguna configuración de ESRB, seleccione "bloquear o permitir juegos específicos" y seleccione el juego por nombre.
    12. Cierre la sesión como Jane y on como Toby
    13. Compruebe que el juego no se inicia en el usuario Toby cuando el usuario Jane 1,2 bloquea el archivo EXE/Name. \[\]
    14. Cierre la sesión como Toby y vuelva a iniciarla como Julia
    15. Como Julia, abra controles de usuario-> restricciones de la aplicación
    16. Haga clic en "Toby solo puede usar los programas que se permiten" y, a continuación, haga clic en Aceptar (es decir, no permitir ningún exe)
    17. Haga clic en el cuadro desactive todo y, a continuación, haga clic en Aceptar.
    18. Vaya a controles de usuario \| juegos controles y permita el juego específico con la Clasificación ESRB
    19. Cierre la sesión como Julia e inicie sesión como Toby e intente jugar al juego
    20. Compruebe que el juego no esté bloqueado y que Toby pueda reproducirlo cuando "no permitir ningún exe" esté establecido en \[ 1,2\]
    21. Cerrar sesión como usuario Toby y volver a iniciar como usuario Julia
    22. Vaya a controles parentales en el panel de control y quite las restricciones
    23. Comprobar que los dos usuarios ya pueden jugar al juego

4.  Continuar con las [pruebas automatizadas](#58-automated-tests)

### <a name="58-automated-tests"></a>5,8 pruebas automatizadas

1.  Compruebe que el juego no genera errores cuando se ejecuta en comprobador de aplicaciones; vea la documentación de la herramienta de pruebas de personalización de marca \[ 4,2\]
2.  Compruebe que los archivos ejecutables del juego contienen manifiestos; vea la documentación de la herramienta de pruebas de personalización de marca \[ 2,1\]
3.  Compruebe que el archivo ejecutable del juego requestedExecutionLevel es "AsInvoker"; vea la documentación de la herramienta de prueba de marca \[ 2,1\]
4.  Continuar con [otras pruebas](#59-other-tests)

### <a name="59-other-tests"></a>5,9 otras pruebas

1.  Compruebe que los archivos ejecutables del juego contienen una firma digital \[ 2,3\]
2.  Comprobar que el proceso de instalación de juego se ejecuta normalmente en las ediciones de 64 bits de Windows Vista y/o Windows 7 \[ 2,3\]
3.  Compruebe que el juego no encuentra un error como resultado de los ejecutables de 16 bits en las ediciones de 64 bits de Windows Vista y/o Windows 7 \[ 2,3\]
4.  Forzar la aplicación para que se bloquee durante las pruebas y comprobar que el juego se muestra Informe de errores de Windows correctamente y recopila los datos de bloqueo \[ 4,3\]
5.  Asegúrese de que los resúmenes de archivo sean correctos \[ 4,3\]

    1.  Haga clic en Inicio-> equipo
    2.  Navegue hasta el directorio del juego
    3.  En la ventana Buscar, escriba \* . dll
    4.  Para cada archivo: haga clic con el botón derecho en el archivo y haga clic en propiedades.

        -   En Windows XP: haga clic en la pestaña versión. Compruebe que los campos nombre de producto, nombre de la compañía y versión del archivo estén rellenados correctamente. \[4.3\]
        -   En Windows Vista y Windows 7: haga clic en la pestaña detalles. Compruebe que los campos nombre del producto y versión del archivo estén rellenados correctamente. El nombre de la compañía no es visible en la página de propiedades de Windows Vista o Windows 7 \[ 4,3\]

    5.  Repetir esta comprobación para los archivos. exe

6.  Inicie el juego.

    1.  Presione CTRL + ALT + SUPR
    2.  Haga clic en la flecha "opciones de apagado"
    3.  Haga clic en reiniciar
    4.  Compruebe que el juego no bloquee el cierre \[ 3,1\]

7.  Continuar con la [desinstalación](#510-uninstall)

### <a name="510-uninstall"></a>5,10 desinstalación

-   Compruebe que el proceso de desinstalación de juegos quita todos los archivos de componentes del sistema operativo instalados y no redistribuidos y borra todas las opciones de configuración \[ 3,1\]

    -   Comprobar en Windows Vista o Windows 7 que el panel de control es la única manera de quitar el programa \[ 1,1\]

## <a name="test-tool-notes"></a>Notas de la herramienta de prueba

Estas son las notas para cada una de las herramientas de prueba que se enumeran en los requisitos de pruebas anteriores.

### <a name="61-appverifier-40-or-higher"></a>6,1 AppVerifier 4,0 (o superior)

**Caso de prueba: 2,5, 4,2**

> [!Note]  
> Algunas aplicaciones no se ejecutan con AppVerifier ejecutándose debido a la protección contra copia. Esto se puede resolver ejecutando con una versión de lanzamiento sin protección del ejecutable del juego.

 

1.  Instalación de AppVerifier 4,0 (o posterior) en un equipo que ejecuta Windows XP
2.  Inicie AppVerifier y haga clic en archivo-> agregar aplicación
3.  Busque el archivo ejecutable del juego, selecciónelo y haga clic en abrir.
4.  En la sección "aplicaciones", seleccione el archivo ejecutable del juego
5.  Seleccione las siguientes pruebas en la sección "aspectos básicos":

    -   Asas
    -   Montones
    -   Bloqueos
    -   Memory
    -   TLS

6.  Seleccione las siguientes pruebas en la sección "varios":

    -   DangerousAPIs
    -   DirtyStacks

7.  Asegúrese de que todas las demás pruebas no estén seleccionadas
8.  Iniciar el juego
9.  Juego
10. Cierre el juego
11. En AppVerifier, seleccione Ver registros de >
12. En la sección "aplicaciones", seleccione el archivo app. exe.
13. En la sección "registros", seleccione el archivo de registro y observe el recuento de errores. Si no hay ningún error, finalice las pruebas de AppVerifier. Si hay errores, haga clic en el botón ver
14. Buscar el documento (CTRL + F) para Severity = "error
15. Crear errores basados en la parte LayerName = del error

### <a name="62-manifest-test---mtexe"></a>Prueba del manifiesto 6,2: mt.exe

**Caso de prueba: 1,8, 2,1**

Esta herramienta se ejecuta desde un símbolo del sistema donde se encuentra MT.exe.

Ejemplo:

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  Haga clic en Inicio > ejecutar > escriba cmd y haga clic en el botón Aceptar.
2.  Ejecute la herramienta de mt.exe para generar un archivo. manifest para cada archivo. exe que se instala con el juego
3.  Abra el archivo. manifest generado.
4.  Asegúrese de que cada archivo. exe contiene lo siguiente (solicitado:

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
> El nivel de ejecución solicitado debe estar presente para cada archivo y dpiAware debe estar presente al menos en el archivo ejecutable del juego s.

 

### <a name="63-thread-hijacker---threadhijackerexe"></a>6,3 secuestrador de subprocesos: threadhijacker.exe

Esta herramienta se ejecuta desde un símbolo del sistema donde se encuentra threadhijacker.exe.

Ejemplo:

``` syntax
threadhijacker.exe /process:str
```

Donde str es el nombre \_ de \_program.exe

1.  Abra el administrador de tareas, haga clic en la pestaña procesos y busque el nombre del ejecutable del juego.
2.  Abra un símbolo del sistema en modo de administrador.
3.  Navegue al directorio donde threadhijacker.exe es
4.  Escriba: **threadhijacker.exe/Process:** Str, donde str es el nombre del ejecutable que desea alcanzar.

### <a name="64-microsoft-games-for-windows-test-tool"></a>6,4 Microsoft Games for Windows Test Tool

Esta herramienta se encuentra en el SDK de DirectX. Una vez que el SDK está instalado en un equipo, el instalador de la herramienta de prueba games for Windows se puede colocar en el equipo de pruebas e instalar.

Busque el instalador de Microsoft Games for Windows Test Tool en el equipo de desarrollo en el que está instalado el SDK de DirectX. De forma predeterminada, se coloca en la siguiente ubicación:

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  Copie el instalador (MicrosoftGFWTestTool.msi/setup.exe) en el equipo de pruebas.
2.  Ejecute al programa de instalación.
3.  Inicie la herramienta Microsoft Games for Windows Test.
4.  En el campo **lista de proyectos** , reemplace **crear nuevo proyecto** por el nombre del título y haga clic en **crear nuevo**.

    Espere a que se complete la línea base.

5.  Rellene la información que pueda tener en la sección **información del juego** y haga clic en **Actualizar información de juego**.
6.  Haga clic en la pestaña **casos de prueba** .
7.  A partir de la parte superior, continúe a través de los casos de prueba y haga clic en **correcto** o en **error** según corresponda.

    Vea "escribir un error" más adelante en esta sección para obtener más información sobre cómo incluir un error en el informe.

8.  Vuelva a la pestaña **proyectos** después de revisar el informe (activando las pestañas de **edición** de **informes** y errores).
9.  Haga clic en **compilar Informe**.

    Se abrirá una ventana cuando el informe termine de compilarse. Aquí encontrará un. Nombres de archivo ZIP *ProjectName* \_report.zip. Este archivo contiene todos los registros y resultados recopilados durante la prueba superada.

### <a name="writing-a-bug"></a>Escribir un error

Hay dos maneras de escribir un informe de errores: puede pasar por los casos de prueba y hacer clic en **error** si el título no es un caso de prueba, o puede hacer clic en la pestaña **Editar error** y agregar manualmente un informe de errores.

### <a name="clicking-fail-on-a-test-case"></a>Hacer clic en error en un caso de prueba

1.  Al hacer clic en **error** en un caso de prueba, la lista desplegable **tipo de problema** se establecerá automáticamente en el tipo de caso de prueba.
2.  Agregue una descripción breve al campo de **título** que describa brevemente el problema.
3.  Agregue una descripción detallada del problema al campo **comportamiento observado** .
4.  Según corresponda, agregue lo que se esperaba (en lugar de una descripción del problema) al campo **comportamiento esperado** .
5.  Agregue una descripción detallada de cómo reproducir el problema en el campo **reproducción-pasos** .
6.  Cuando haya terminado, haga clic en el botón **Guardar** .

### <a name="manually-adding-a-bug"></a>Agregar manualmente un error

Este proceso es el mismo que cuando se hace clic en **FAIL**, con la excepción de la lista desplegable de rellenado automático. En este caso, seleccione el tipo de error de TCR adecuado o seleccione un **\* \* problema \* \* que no sea TR** para los errores que se encuentren fuera del intervalo TR, pero que todavía se deben informar.

## <a name="resources"></a>Recursos

<dl> <dt>

<span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Juegos para Windows: requisitos técnicos
</dt> <dd>

[Juegos para requisitos técnicos de Windows: prácticas recomendadas para juegos en Windows XP, Windows Vista y Windows 7](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK
</dt> <dd>

[SDK de Windows](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Directrices de control de cuentas de usuario
</dt> <dd>

[Requisitos de desarrollo de aplicaciones de Windows Vista para la compatibilidad de control de cuentas de usuario](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

</dd> <dt>

<span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Información de Windows Installer
</dt> <dd>

[Windows Installer](../msi/windows-installer-portal.md)

</dd> <dt>

<span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portal para desarrolladores de WinQual 
</dt> <dd>

[Servicios en línea de calidad de Windows (WinQual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>Portal para desarrolladores de DirectX
</dt> <dd>

[Centro para desarrolladores de DirectX](/previous-versions/windows/apps/hh452744(v=win.10))

</dd> <dt>

<span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog de juegos para Windows y DirectX SDK
</dt> <dd>

[Juegos para Windows y el SDK de DirectX](https://walbourn.github.io/)

</dd> <dt>

<span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artículos adicionales de DirectX
</dt> <dd>

[Artículos técnicos de DirectX](./dx9-technical-articles.md)

</dd> </dl>

 

