---
title: Registro de la tecnología de asistencia de accesibilidad
description: En este artículo se explica cómo registrar una aplicación de accesibilidad con el centro de accesibilidad. También se explica cómo adaptar la aplicación de accesibilidad para que funcione bien con el escritorio seguro.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704998"
---
# <a name="ease-of-access---assistive-technology-registration"></a>Registro de la tecnología de asistencia de accesibilidad

En este artículo se explica cómo registrar una aplicación de accesibilidad con el centro de accesibilidad. También se explica cómo adaptar la aplicación de accesibilidad para que funcione bien con el escritorio seguro.

El centro de accesibilidad es una aplicación del panel de control para Microsoft Windows que reúne la funcionalidad de accesibilidad y facilidad de uso. Mediante el centro de accesibilidad, los usuarios pueden configurar sus equipos para que se adapten a sus necesidades físicas y cognitivas.

Una función del centro de accesibilidad es ayudar a los usuarios a iniciar aplicaciones de accesibilidad, como narrador, teclado en pantalla y ampliador. Las aplicaciones de terceros registradas también aparecen en el centro de accesibilidad y se pueden iniciar directamente desde allí.

Las aplicaciones de accesibilidad deben funcionar sin problemas con el escritorio seguro. El escritorio seguro es la interfaz de usuario que aparece cuando el equipo está bloqueado (en el inicio de sesión o cuando el usuario ha bloqueado el escritorio) y cuando se solicita al usuario que permita una acción potencialmente insegura. Por motivos de seguridad, Windows impone límites en el software de terceros que se ejecuta en el escritorio seguro. Si desea que la aplicación de accesibilidad se ejecute en el escritorio seguro, debe registrar la aplicación con el centro de accesibilidad.

## <a name="registering-with-the-ease-of-access-center"></a>Registro con el centro de accesibilidad

Las aplicaciones de accesibilidad se registran con el centro de facilidad de acceso mediante la creación de una o varias claves del registro cuando se instala la aplicación. En la tabla siguiente se muestra la información contenida en las claves del registro.



| Nombre                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Obligatorio/Opcional | Idioma      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| Nombre de la aplicación            | El nombre de la aplicación, que se encuentra en un archivo de recursos. Este valor del registro contiene una cadena con un formato especificado. Puede tratarse de una versión localizada del nombre de la aplicación, si la aplicación está localizada en idiomas distintos del inglés. El nombre aparece en el centro de accesibilidad.<br/>                                                                                                                                                                                                                                                                                       | Mandatory          | Traducida     |
| ATExe                       | Nombre del archivo ejecutable de la aplicación o de la imagen. Windows usa este valor para determinar si se está ejecutando la aplicación de accesibilidad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | Mandatory          | No localizado |
| CopySettingsToLockedDesktop | Valor **DWORD** que indica si se debe copiar la configuración de la aplicación de accesibilidad en el escritorio bloqueado.<br/> Si este valor es 1, la aplicación puede escribir la configuración en una ubicación del registro de usuario y Windows copia la configuración en la misma ubicación del registro de usuario para el escritorio bloqueado. Esto permite que la aplicación conserve su estado del escritorio "normal" en el escritorio bloqueado.<br/>                                                                                                                                                             | Opcionales           | No localizado |
| Descripción                 | Breve descripción de la aplicación, desde un archivo de recursos. Este valor del registro contiene una cadena con un formato especificado. Puede tratarse de una versión localizada de la descripción si la aplicación está localizada en idiomas distintos del inglés. La longitud de esta cadena debe ser inferior a 512 caracteres.<br/> La descripción aparece en el centro de accesibilidad para proporcionar información adicional sobre la aplicación de accesibilidad al usuario.<br/> Este valor también se puede usar para notificar al usuario que la aplicación no se utiliza en el escritorio seguro.<br/>      | Mandatory          | Traducida     |
| Perfil                     | Una pequeña parte de XML que especifica los alojamientos que proporciona la aplicación. Garantiza que la aplicación aparece en la categoría correcto en el centro de accesibilidad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  | Mandatory          | No localizado |
| PassiveAutoStartBehavior    | <p>Valor **DWORD** que indica si está habilitado el comportamiento de inicio automático heredado.</p><p>El valor predeterminado es 0, que indica que un en requiere un comportamiento de inicio automático heredado. Esto hace que el valor "iniciar después del inicio de sesión" en se proteja en la configuración rápida (OOBE) y el panel de control (vea **Panel de control-> facilidad de acceso > centro de accesibilidad-> cambiar la configuración de inicio de sesión**) e inicia automáticamente la en después de UAC y de la pantalla de bloqueo.</p><p>Un valor de 1 indica que en debe usar el nuevo comportamiento de inicio automático en el que la opción "iniciar después del inicio de sesión" de la no está activada en la configuración rápida (OOBE) y el panel de control, y en se inicia automáticamente una vez por sesión de usuario (en el inicio de sesión) solo si está activada la opción "iniciar después del inicio de sesión".</p>                                                                                                                                                                                                                                                                                                                                                                                                  | Opcionales          | No localizado |
| SecureDesktopAccommodation  | El nombre de una aplicación de accesibilidad alternativa que se ejecutará en el escritorio seguro en lugar de esta aplicación. La alternativa puede ser una aplicación diferente, una versión diferente de la misma aplicación, una de las aplicaciones de accesibilidad que se incluye en Windows o "none" si no desea ejecutar ninguna aplicación de accesibilidad en el escritorio seguro. <br/>                                                                                                                                                                                                               | Opcionales           | No localizado |
| Perfil simple              | Un valor que describe cómo clasificar la aplicación en una o dos palabras: lector de pantalla, lupa o teclado en pantalla, por ejemplo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Mandatory          | No localizado |
| Variable startexe ProcessStartInfo                    | Ruta de acceso completa del archivo ejecutable. Este valor se utiliza para iniciar la aplicación de accesibilidad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Mandatory          | No localizado |
| StartParams                 | Argumentos de la línea de comandos. Estos valores se usan junto con variable startexe ProcessStartInfo para iniciar la aplicación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Opcionales           | No localizado |
| TerminateOnDesktopSwitch    | Valor **DWORD** que especifica el modo en que la aplicación de accesibilidad responde a las transiciones hacia o desde el escritorio seguro.<br/> Si este valor no existe o es 1, Windows finaliza y reinicia la aplicación en cada transición hacia o desde el escritorio seguro. Este es el comportamiento predeterminado.<br/> Si este valor es 0, Windows no finaliza la aplicación de accesibilidad en una transición del escritorio. La aplicación continúa ejecutándose en el escritorio anterior y Windows inicia una nueva instancia en el escritorio nuevo si aún no se está ejecutando una instancia.<br/> | Opcionales           | No localizado |


 

### <a name="localization"></a>Localización

Los valores del registro de nombre y descripción de la aplicación deben ser localizables para admitir la interfaz de usuario multilingüe (MUI).

Estas cadenas tienen el formato siguiente, donde los corchetes angulares indican los elementos necesarios y los corchetes, lo que significa un elemento opcional.

*@ <ResDllPath \\ ResDLLFilename>,- <resID> \[ ;<comment>\]*

*<ResDllPath \\ ResDLLFilename>* es la ruta de acceso al archivo dll de recursos. La ruta de acceso puede contener variables de entorno.

*<resID>* es el identificador de recurso de la cadena.

el *\[ comentario \]* contiene cualquier comentario opcional.

Este es un ejemplo:


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



Para obtener más información sobre MUI, vea [centro de conocimientos de Windows mui](../intl/about-multilingual-user-interface.md).

### <a name="hci-profile"></a>Perfil de HCI

El perfil de interacción de equipo humano (HCI) es una manera de determinar qué alojamientos debe proporcionar en función de las necesidades del usuario. Las aplicaciones de accesibilidad deben registrar información sobre el tipo de discapacidad que la aplicación ayuda a acomodar.

El valor del registro profile contiene XML que describe el tipo de discapacidad de destino de la aplicación de accesibilidad. Este XML tiene el siguiente formato:


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



Los valores válidos para el atributo de **tipo de alojamiento** son los siguientes:

-   visión leve
-   visión seria
-   cognitiva leve
-   cognitivo grave
-   destreza leve
-   destreza grave
-   audición leve
-   audiencia grave
-   voz leve
-   voz seria

> [!Note]  
> Estos valores distinguen entre mayúsculas y minúsculas.

 

Si una aplicación de accesibilidad admite varias adaptaciones, el valor del registro de perfil debe incluir un atributo de **tipo de alojamiento** para cada alojamiento.

### <a name="ease-of-access-registry-details"></a>Detalles del registro de accesibilidad

Para registrar la aplicación de accesibilidad, debe crear una clave para la aplicación en la siguiente ubicación del registro y rellenarla con pares nombre-valor.

**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS\\**

Asigne un nombre a la clave del registro de la aplicación con el siguiente formato:

*"CompanyName \_ ProductName \_ v \# "*

Por ejemplo, "Contoso \_ Magnifier \_ v 2.0".

Para agregar valores de registro, el programa de instalación debe ejecutarse con privilegios elevados.

### <a name="secure-desktop-accommodation"></a>Alojamiento de escritorio seguro

La clave del registro **SecureDesktopAccommodation** le permite especificar el modo en que la aplicación de accesibilidad responde al escritorio seguro. De forma predeterminada, el centro de accesibilidad inicia la aplicación en el escritorio seguro si ya se estaba ejecutando en el escritorio normal, o si está configurado para ejecutarse en el escritorio de inicio de sesión. Mediante el uso de la clave **SecureDesktopAccommodation** , puede:

-   Especifique una versión alternativa de la aplicación para usarla en el escritorio seguro. Por ejemplo, podría tener una versión alternativa que deshabilita características no seguras o está optimizada para usar menos memoria e iniciarse más rápido.

    Para especificar la versión alternativa, establezca la clave **SecureDesktopAccommodation** en el nombre de la versión alternativa. Por ejemplo, si registró su aplicación en la \_ clave lector de pantalla de Contoso \_ v 1.0, podría registrar la versión alternativa en la pantalla de Contoso \_ ReaderSecure \_ v 1.0. A continuación, establezca la clave **SecureDesktopAccommodation** del \_ lector de pantalla de Contoso \_ v 1.0 en "Contoso \_ Screen ReaderSecure \_ v 1.0".

-   Especifique una aplicación de accesibilidad de Microsoft para usarla en el escritorio seguro en lugar de la aplicación. Para esta opción, establezca **SecureDesktopAccommodation** en el nombre de la aplicación de accesibilidad de Microsoft determinada: "Osk", "magnifierpane" o "narrador".
-   Especifique que la aplicación no debe ejecutarse en el escritorio seguro y que ninguna otra aplicación alternativa. Para esta opción, establezca **SecureDesktopAccommodation** en "none" (recomendado) o el nombre de una aplicación inexistente.

Si la clave del registro **SecureDesktopAccommodation** de la aplicación de accesibilidad especifica que una aplicación de accesibilidad de Microsoft se ejecute en el escritorio seguro en lugar de la aplicación, Windows notifica al usuario de este al realizar la transición al escritorio seguro. Para notificar al usuario, Windows muestra la cadena especificada en la clave del registro de descripción de la aplicación. Por ejemplo, si la aplicación ScreenReader Deluxe 1,0 usa Microsoft Narrator en el escritorio seguro, incluiría una cadena de descripción como, "el narrador de Microsoft se usará en el bloque, el inicio de sesión y otros escritorios seguros en lugar de ScreenReader Deluxe 1,0".

Si la clave **SecureDesktopAccommodation** de la aplicación se establece en "none", use la clave **Description** para indicar al usuario que la aplicación no está disponible en el escritorio seguro y no se proporciona ninguna alternativa.

Windows muestra el texto de descripción en las ubicaciones correspondientes del centro de accesibilidad.

### <a name="running-at-installation-and-on-the-logon-desktop"></a>Ejecutar durante la instalación y en el escritorio de inicio de sesión

Si anexa el nombre de clave registrado de la aplicación de accesibilidad a la cadena en la siguiente ubicación del registro, Windows iniciará la aplicación inmediatamente después de instalarla. Además, Windows ejecutará automáticamente la aplicación cada vez que el escritorio de inicio de sesión esté activo.

**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ Configuration**

La clave de configuración es una cadena delimitada por comas. Para agregar la aplicación, anexe una cadena que sea la misma que la clave del registro de la aplicación en HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ .

### <a name="running-in-a-job"></a>Ejecutar en un trabajo

Si la clave del registro **TerminateOnDesktopSwitch** no está presente o se establece en un valor distinto de cero, Windows ejecuta la aplicación en el contexto de un trabajo, finalizando y reiniciando la aplicación con cada transición del escritorio. La ejecución en un trabajo garantiza que solo una instancia de la aplicación se ejecuta en un momento determinado y libera a la aplicación de tener que supervisar el estado del escritorio. Las desventajas de ejecutar en un trabajo incluyen:

-   La aplicación incurre en un costo de inicio con cada transición de escritorio.
-   La aplicación solo se puede iniciar a través del centro de accesibilidad.
-   La aplicación debe guardar continuamente su configuración porque una transición de escritorio puede terminar en cualquier momento.

Si la clave **TerminateOnDesktopSwitch** existe y está establecida en 0, Windows no ejecuta la aplicación de accesibilidad en un trabajo. Esto tiene las ventajas siguientes:

-   No hay costos de inicio asociados a las transiciones de escritorio.
-   La aplicación se puede iniciar fuera del centro de accesibilidad.

Las desventajas de no ejecutar en un trabajo incluyen:

-   Dado que la aplicación no se reinicia en las transiciones del escritorio, debe detectar cuándo está inactivo el escritorio actual y responder de forma adecuada. Por ejemplo, la aplicación debe ceder el control del hardware para que la versión de escritorio seguro de la aplicación pueda usarla, y la aplicación debe entrar en modo de suspensión para evitar el uso de los recursos del procesador.
-   Si la aplicación se puede iniciar a través del menú Inicio, el explorador de Windows o la línea de comandos, se debe informar al centro de accesibilidad. Para obtener más información, consulte **tecla del logotipo de Windows + U**.
-   Dado que se pueden ejecutar varias copias de la aplicación simultáneamente en distintos equipos de escritorio, la aplicación debe estar escrita para admitir varias copias en ejecución.

### <a name="windows-logo-key--u"></a>Tecla del logotipo de Windows + U

Si la aplicación de accesibilidad está configurada para ejecutarse en un trabajo, el código de inicio de la aplicación debe incluir una llamada a la función [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) para determinar si la aplicación se está iniciando en un trabajo. Si es así, la aplicación debe iniciar el centro de accesibilidad y, a continuación, salir. En el ejemplo siguiente se muestra cómo llamar a **IsProcessInJob**.


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



Si la aplicación de accesibilidad está configurada para ejecutarse fuera de un trabajo, debe notificar al centro de accesibilidad que la aplicación se está iniciando y continuar de la forma habitual.

Independientemente de cómo se configure la aplicación, si proporciona una manera de salir de la aplicación, como un botón Cerrar, la aplicación debe notificar al centro de accesibilidad que se está cerrando.

Una aplicación notifica al centro de accesibilidad mediante el establecimiento de una clave del registro temporal y, después, la inserción de la combinación de teclas del logotipo de Windows + U en el flujo de entrada.

La aplicación debe crear la clave temporal en la siguiente ubicación.

**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**

La clave temporal debe tener el mismo nombre que el nombre de la aplicación registrada, como " \_ lector de pantalla de Contoso \_ v 1.0". El valor de la clave es una **DWORD** establecida en 0x0003 cuando se inicia o 0x0002 cuando la aplicación se está cerrando.


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a>Tecla del logotipo de Windows + subir volumen

Cuando el usuario inicia la aplicación de accesibilidad presionando la tecla del logotipo de Windows + combinación de teclas del volumen (por ejemplo, en un dispositivo de tableta gráfica), el centro de accesibilidad pasa el siguiente argumento de línea de comandos a la aplicación:

**/hardwarebuttonlaunch**

La aplicación puede usar este argumento para determinar si se va a iniciar con normalidad o para ajustar el comportamiento en consecuencia.

### <a name="transferring-secure-desktop-settings"></a>Transferencia de la configuración de escritorio seguro

Si su aplicación de accesibilidad es compatible con el escritorio seguro, puede usar el registro para copiar la configuración cuando la aplicación pase al escritorio seguro. La copia de la configuración permite que la transición al escritorio seguro sea más fluida para el usuario.

Para copiar la configuración, establezca la clave del registro CopySettingsToLockedDesktop de la aplicación en 1 y almacene la configuración en la siguiente ubicación del registro.

**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATConfig\\<AT Key Name>**

El centro de accesibilidad supervisa esta ubicación del registro mientras la aplicación se está ejecutando. Cuando se produce una transición al escritorio seguro, el centro de accesibilidad copia la configuración en la misma ubicación del subárbol HKCU de escritorio seguro. A continuación, la aplicación puede leer la configuración y reanudar su estado.

La aplicación de accesibilidad debe escribir su configuración a intervalos regulares o cada vez que cambien los valores. La escritura de la configuración en la salida de la aplicación no funcionará. Si la aplicación se ejecuta en un trabajo, se termina en la transición fuera del escritorio seguro, antes de que el código de salida tenga la oportunidad de ejecutarse. Si la aplicación no se está ejecutando en un trabajo, la aplicación no se termina en la transición fuera del escritorio seguro.

### <a name="caution"></a>Precaución

Dado que las claves del registro que se describen aquí están escritas en modo de usuario, no son seguras. Si la aplicación de accesibilidad lee el contenido de estas claves, debe comprobar cuidadosamente los datos y utilizarlos con precaución. En concreto, la aplicación debe realizar una comprobación de los límites de los valores **DWORD** , tener cuidado con las longitudes de cadena, no debe leer los nombres de los archivos DLL del complemento y no debe ejecutar ningún comando que se encuentre en las cadenas.

## <a name="registry-examples"></a>Ejemplos del registro

En el ejemplo siguiente se muestran los posibles valores de registro de un producto ficticio denominado contoso ScreenReader versión 2,0, cuyo nombre localizado se almacena como un recurso.

Los valores de la tabla están bajo la siguiente clave:

**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ contoso \_ Screen Reader \_ v 2.0**



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Tipo</th>
<th>Datos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll,-5020</td>
</tr>
<tr class="even">
<td>Descripción</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll,-5040</td>
</tr>
<tr class="odd">
<td>Perfil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>Variable startexe ProcessStartInfo</td>
<td>REG_SZ</td>
<td>C:\ContosoTools\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>

</tr>
<tr class="odd">
<td>SecureDesktopAccommodation</td>
<td>REG_SZ</td>
<td>Narrador</td>
</tr>
</tbody>
</table>



 

Si la aplicación proporciona un lector de pantalla y un ampliador de pantalla en un solo archivo ejecutable, los valores del componente lector de pantalla pueden tener este aspecto:



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Tipo</th>
<th>Datos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-30</td>
</tr>
<tr class="even">
<td>Descripción</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-32</td>
</tr>
<tr class="odd">
<td>Perfil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>Variable startexe ProcessStartInfo</td>
<td>REG_SZ</td>
<td>C:\Archivos de Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/r</td>
</tr>
</tbody>
</table>



 

Los valores para el componente del ampliador tendrían la siguiente clave:

**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATS \\ contoso \_ Magnifier \_ v 2.0**



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Tipo</th>
<th>Datos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-31</td>
</tr>
<tr class="even">
<td>Descripción</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-42</td>
</tr>
<tr class="odd">
<td>Perfil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>Aumento</td>
</tr>
<tr class="odd">
<td>Variable startexe ProcessStartInfo</td>
<td>REG_SZ</td>
<td>C:\Archivos de Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/m</td>
</tr>
</tbody>
</table>



 

 

