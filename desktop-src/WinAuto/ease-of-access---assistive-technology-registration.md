---
title: Accesibilidad de tecnología de asistencia
description: En este artículo se explica cómo registrar una aplicación de accesibilidad con el Centro de accesibilidad. También se explica cómo adaptar la aplicación de accesibilidad para que funcione bien con el escritorio seguro.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 9a87fadac85906dfd07fd4c568185125039207d9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885204"
---
# <a name="ease-of-access---assistive-technology-registration"></a>Accesibilidad de tecnología de asistencia

En este artículo se explica cómo registrar una aplicación de accesibilidad con el Centro de accesibilidad. También se explica cómo adaptar la aplicación de accesibilidad para que funcione bien con el escritorio seguro.

El Centro de accesibilidad es una aplicación Panel de control para Microsoft Windows reúne funcionalidad para la accesibilidad y facilidad de uso. Mediante el uso de Centro de accesibilidad, los usuarios pueden configurar sus equipos para satisfacer sus necesidades físicas y cognitivas.

Una función de la Centro de accesibilidad es ayudar a los usuarios a iniciar aplicaciones de accesibilidad, como Narrador, Teclado en pantalla y Lupa. Las aplicaciones de terceros registradas también aparecen en la Centro de accesibilidad y se pueden iniciar directamente desde allí.

Las aplicaciones de accesibilidad deben funcionar sin problemas con el escritorio seguro. El escritorio seguro es la interfaz de usuario que aparece cuando el equipo está bloqueado (al iniciar sesión o cuando el usuario ha bloqueado el escritorio) y cuando se le pide al usuario que permita una acción potencialmente no segura. Por motivos de seguridad, Windows limita el software de terceros que se ejecuta en el escritorio seguro. Si desea que la aplicación de accesibilidad se ejecute en el escritorio seguro, debe registrar la aplicación con el Centro de accesibilidad.

## <a name="registering-with-the-ease-of-access-center"></a>Registro con el Centro de accesibilidad

Las aplicaciones de accesibilidad se registran con Centro de accesibilidad mediante la creación de una o varias claves del Registro cuando se instala la aplicación. En la tabla siguiente se muestra la información contenida en las claves del Registro.



| Nombre                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Obligatorio/Opcional | Lenguaje      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| Nombre de la aplicación            | Nombre de la aplicación, que se encuentra en un archivo de recursos. Este valor del Registro contiene una cadena en un formato especificado. Podría ser una versión localizada del nombre de la aplicación, si la aplicación se localiza en idiomas distintos del inglés. El nombre aparece en la Centro de accesibilidad.<br/>                                                                                                                                                                                                                                                                                       | Mandatory          | Localizada     |
| ATExe                       | Nombre del archivo ejecutable de la aplicación o la imagen. Windows este valor para determinar si la aplicación de accesibilidad se está ejecutando.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | Mandatory          | No localizado |
| CopySettingsToLockedDesktop | Valor **DWORD** que indica si se debe copiar la configuración de la aplicación de accesibilidad en el escritorio bloqueado.<br/> Si este valor es 1, la aplicación puede escribir la configuración en una ubicación del registro de usuarios y Windows copia la configuración en la misma ubicación del registro de usuario para el escritorio bloqueado. Esto permite que la aplicación conserve su estado desde el escritorio "normal" al escritorio bloqueado.<br/>                                                                                                                                                             | Opcionales           | No localizado |
| Descripción                 | Breve descripción de la aplicación, de un archivo de recursos. Este valor del Registro contiene una cadena en un formato especificado. Podría ser una versión localizada de la descripción, si la aplicación se localiza en idiomas distintos del inglés. La longitud de esta cadena debe ser inferior a 512 caracteres.<br/> La descripción aparece en la Centro de accesibilidad para proporcionar información adicional sobre la aplicación de accesibilidad al usuario.<br/> Este valor también se puede usar para notificar al usuario que la aplicación no se usa en el escritorio seguro.<br/>      | Mandatory          | Localizada     |
| Perfil                     | Fragmento corto de XML que especifica los artículos que proporciona la aplicación. Garantiza que la aplicación aparece en la categoría correcta de la Centro de accesibilidad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  | Mandatory          | No localizado |
| PassiveAutoStartBehavior    | <p>Valor **DWORD** que indica si el comportamiento de inicio automático heredado está habilitado.</p><p>El valor predeterminado es 0, lo que indica que un AT requiere un comportamiento de inicio automático heredado. Esto hace que la configuración "Iniciar después del inicio de sesión" de ese AT se aprotebe en la configuración rápida (OOBE) y Panel de control (consulte **Panel de control -> Accesibilidad -> Centro de accesibilidad -> Cambiar** configuración de inicio de sesión) e inicia automáticamente el AT después de UAC y la pantalla de bloqueo.</p><p>Un valor de 1 indica que AT debe usar el nuevo comportamiento de inicio automático en el que la configuración "Iniciar después del inicio de sesión" para ese AT no está activada en la experiencia de configuración predeterminada (OOBE) y Panel de control, y AT se inicia automáticamente una vez por sesión de usuario (en el inicio de sesión) solo si la opción "iniciar después de iniciar sesión" está activada.</p>                                                                                                                                                                                                                                                                                                                                                                                                  | Opcionales          | No localizado |
| SecureDesktopAccommodation  | Nombre de una aplicación de accesibilidad alternativa que se ejecutará en el escritorio seguro en lugar de esta aplicación. La alternativa puede ser una aplicación diferente, una versión diferente de la misma aplicación, una de las aplicaciones de accesibilidad que se incluyen en Windows o "none" si no desea ejecutar ninguna aplicación de accesibilidad en el escritorio seguro. <br/>                                                                                                                                                                                                               | Opcionales           | No localizado |
| Perfil simple              | Valor que describe cómo clasificar la aplicación en una palabra o dos: lector de pantalla, lupa o teclado en pantalla, por ejemplo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Mandatory          | No localizado |
| StartExe                    | Ruta de acceso completa del ejecutable. Este valor se usa para iniciar la aplicación de accesibilidad.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Mandatory          | No localizado |
| StartParams                 | Argumentos de la línea de comandos. Estos valores se usan junto con StartExe para iniciar la aplicación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Opcionales           | No localizado |
| TerminateOnDesktopSwitch    | Valor **DWORD** que especifica cómo responde la aplicación de accesibilidad a las transiciones hacia o desde el escritorio seguro.<br/> Si este valor no existe o es 1, Windows finaliza y reinicia la aplicación en cada transición hacia o desde el escritorio seguro. Este es el comportamiento predeterminado.<br/> Si este valor es 0, Windows la aplicación de accesibilidad en una transición de escritorio. La aplicación continúa ejecutándose en el escritorio anterior y Windows inicia una nueva instancia en el nuevo escritorio si una instancia aún no se está ejecutando allí.<br/> | Opcionales           | No localizado |


 

### <a name="localization"></a>Localización

Los valores del Registro de Nombre de aplicación y Descripción deben ser localizables para admitir Interfaz de usuario multilingüe (LDAP).

Estas cadenas tienen el siguiente formato, donde los corchetes angulares significan los elementos necesarios y los corchetes significan un elemento opcional.

*@<ResDllPath \\ ResDLLFilename>,- &lt; resID &gt; \[ ; &lt; Comentario&gt;\]*

*<ResDllPath \\ ResDLLFilename>* es la ruta de acceso al archivo DLL del recurso. La ruta de acceso puede contener variables de entorno.

*&lt; resID &gt; es* el identificador de recurso de la cadena.

*\[ comment \]* contiene cualquier comentario opcional.

Este es un ejemplo:


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



Para obtener más información acerca de LAN, [vea Windows centro de conocimiento de WINDOWS.](../intl/about-multilingual-user-interface.md)

### <a name="hci-profile"></a>Perfil de HCI

El perfil de Interacción con equipos humanos (HCI) es una manera de determinar qué servicios proporcionar en función de las necesidades del usuario. Las aplicaciones de accesibilidad deben registrar información sobre el tipo de discapacidad que la aplicación ayuda a dar cabida.

El valor del Registro de perfil contiene XML que describe el tipo de discapacidad que tiene como destino la aplicación de accesibilidad. Este XML tiene el formato siguiente:


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



Los valores válidos para **el atributo Tipo de alojamiento** son los siguientes:

-   visión de visión
-   visión grave
-   cognitive
-   cognitiva grave
-   asínura
-   gravedad
-   audiencia
-   audiencia grave
-   voz de voz
-   voz grave

> [!Note]  
> Estos valores distinguen entre mayúsculas y minúsculas.

 

Si una aplicación de accesibilidad admite varios alojamientos, el valor del Registro de perfil debe incluir un atributo **de tipo De** alojamiento para cada alojamiento.

### <a name="ease-of-access-registry-details"></a>Accesibilidad detalles del Registro

Para registrar la aplicación de accesibilidad, debe crear una clave para la aplicación en la siguiente ubicación del Registro y rellenarla con pares nombre-valor.

**HKLM \\ SOFTWARE Microsoft Windows NT \\ \\ \\ CurrentVersion \\ Accessibility \\ ATs\\**

Asigne un nombre a la clave del Registro de la aplicación con el formato siguiente:

*"CompanyName \_ ProductName \_ v \# "*

Por ejemplo, "Contoso \_ Lupa \_ v2.0".

Para agregar valores del Registro, el programa de instalación debe ejecutarse con privilegios elevados.

### <a name="secure-desktop-accommodation"></a>Proteger los alojamientos de escritorio

La **clave del Registro SecureDesktopAccommodation** le permite especificar cómo responde la aplicación de accesibilidad al escritorio seguro. De forma predeterminada, el Centro de accesibilidad inicia la aplicación en el escritorio seguro si ya se estaba ejecutando en el escritorio normal o si está configurada para ejecutarse en el escritorio de inicio de sesión. Con la **clave SecureDesktopAccommodation,** puede hacer lo siguiente:

-   Especifique una versión alternativa de la aplicación para usarla en el escritorio seguro. Por ejemplo, puede tener una versión alternativa que deshabilite las características no seguras o que esté optimizada para usar menos memoria e iniciarse más rápido.

    Para especificar la versión alternativa, establezca la clave **SecureDesktopAccommodation** en el nombre de la versión alternativa. Por ejemplo, si registró la aplicación en la clave Contoso Screen Reader v1.0, podría registrar la versión alternativa en \_ \_ Contoso Screen \_ ReaderSecure \_ v1.0. A continuación, establezca la clave **SecureDesktopAccommodation** de Contoso \_ Screen Reader \_ v1.0 en "Contoso \_ Screen ReaderSecure \_ v1.0".

-   Especifique una aplicación de accesibilidad de Microsoft para usarla en el escritorio seguro en lugar de la aplicación. Para esta opción, establezca **SecureDesktopAccommodation** en el nombre de la aplicación de accesibilidad de Microsoft concreta: "osk", "lupa" o "Narrador".
-   Especifique que la aplicación no se debe ejecutar en el escritorio seguro y que ninguna aplicación alternativa. Para esta opción, establezca **SecureDesktopAccommodation** en "none" (recomendado) o el nombre de una aplicación inexistente.

Si la clave del Registro **SecureDesktopAccommodation** de la aplicación de accesibilidad especifica una aplicación de accesibilidad de Microsoft para ejecutarse en el escritorio seguro en lugar de la aplicación, Windows lo notifica al usuario al realizar la transición al escritorio seguro. Para notificar al usuario, Windows la cadena especificada en la clave del Registro Description de la aplicación. Por ejemplo, si la aplicación ScreenReader Deluxe 1.0 usa Microsoft Narrator en el escritorio seguro, incluiría una cadena de descripción, como "Microsoft Narrator se usará en los escritorios bloqueados, de inicio de sesión y de otros escritorios seguros en lugar de ScreenReader Scripts 1.0".

Si la clave **SecureDesktopAccommodation** de la aplicación está establecida en "none", use la clave **Description** para decir al usuario que la aplicación no está disponible en el escritorio seguro y no se proporciona ninguna alternativa.

Windows muestra el texto Descripción en las ubicaciones pertinentes del Centro de accesibilidad.

### <a name="running-at-installation-and-on-the-logon-desktop"></a>Ejecución durante la instalación y en el escritorio de inicio de sesión

Si anexa el nombre de clave registrada de la aplicación de accesibilidad a la cadena en la siguiente ubicación del Registro, Windows iniciará la aplicación inmediatamente después de instalarla. Además, Windows ejecutará automáticamente la aplicación cada vez que el escritorio de inicio de sesión esté activo.

**HKCU \\ Software Microsoft Windows nt \\ \\ \\ CurrentVersion \\ Accessibility \\ Configuration**

La clave de configuración es una cadena delimitada por comas. Para agregar la aplicación, anexe una cadena que sea la misma que la clave del Registro de la aplicación en HKLM \\ SOFTWARE Microsoft Windows NT \\ \\ \\ CurrentVersion \\ Accessibility \\ ATs \\ .

### <a name="running-in-a-job"></a>Ejecución en un trabajo

Si la clave del Registro **TerminateOnDesktopSwitch** no está presente o está establecida en distinto de cero, Windows ejecuta la aplicación en el contexto de un trabajo, finalizando y reiniciando la aplicación con cada transición de escritorio. La ejecución en un trabajo garantiza que solo se ejecute una única instancia de la aplicación en un momento determinado y libera a la aplicación de tener que supervisar el estado del escritorio. Las desventajas de la ejecución en un trabajo incluyen:

-   La aplicación incurre en un costo de inicio con cada transición de escritorio.
-   La aplicación solo se puede iniciar a través del Centro de accesibilidad.
-   La aplicación debe guardar continuamente su configuración porque se puede finalizar en cualquier momento mediante una transición de escritorio.

Si la **clave TerminateOnDesktopSwitch** existe y está establecida en 0, Windows ejecuta la aplicación de accesibilidad en un trabajo. Esto tiene las ventajas siguientes:

-   No hay costos de inicio asociados a las transiciones de escritorio.
-   La aplicación se puede iniciar fuera del Centro de accesibilidad.

Las desventajas de no ejecutarse en un trabajo incluyen:

-   Dado que la aplicación no se reinicia en las transiciones de escritorio, debe detectar cuándo está inactivo el escritorio actual y responder correctamente. Por ejemplo, la aplicación debe dejar el control del hardware para que la versión de escritorio segura de la aplicación pueda usarla y la aplicación debe entrar en modo de suspensión para evitar el uso de recursos de procesador.
-   Si la aplicación se puede iniciar a través de menú Inicio, Windows Explorer o la línea de comandos, es necesario informar al Centro de accesibilidad la aplicación. Para obtener más información, **vea Windows Logo key + U**.
-   Dado que varias copias de la aplicación se pueden ejecutar simultáneamente en distintos escritorios, la aplicación debe escribirse para admitir varias copias en ejecución.

### <a name="windows-logo-key--u"></a>Windows Tecla logotipo + U

Si la aplicación de accesibilidad está configurada para ejecutarse en un trabajo, el código de inicio de la aplicación debe incluir una llamada a la función [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) para determinar si la aplicación se inicia en un trabajo. Si es así, la aplicación debe iniciar el Centro de accesibilidad y, a continuación, salir. En el ejemplo siguiente se muestra cómo llamar **a IsProcessInJob.**


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



Si la aplicación de accesibilidad está configurada para ejecutarse fuera de un trabajo, debe notificar al Centro de accesibilidad que la aplicación se está iniciando y continuar con normalidad.

Independientemente de cómo esté configurada la aplicación, si proporciona una manera de salir desde dentro de la aplicación, como un botón Cerrar, la aplicación debe notificar al Centro de accesibilidad que está saliendo.

Una aplicación notifica al Centro de accesibilidad estableciendo una clave temporal del Registro y, a continuación, insertando la combinación Windows tecla Logotipo + tecla U en el flujo de entrada.

La aplicación debe crear la clave temporal en la siguiente ubicación.

**HKCU \\ Software Microsoft Windows NT \\ \\ \\ CurrentVersion \\ AccessibilityTemp**

La clave temporal debe tener el mismo nombre que el nombre de la aplicación registrada, como "Contoso \_ Screen Reader \_ v1.0". El valor de la clave es un **DWORD** establecido en 0x0003 se inicia o 0x0002 cuando se cierra la aplicación.


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



### <a name="windows-logo-key--volume-up"></a>Windows Tecla logotipo + Subir volumen

Cuando el usuario inicia la aplicación de accesibilidad presionando la combinación de teclas Logotipo y Subir volumen de Windows (por ejemplo, en un dispositivo de tableta), el Centro de accesibilidad pasa el siguiente argumento de línea de comandos a la aplicación:

**/hardwarebuttonlaunch**

La aplicación puede usar este argumento para determinar si se debe iniciar con normalidad o ajustar el comportamiento en consecuencia.

### <a name="transferring-secure-desktop-settings"></a>Transferencia de la configuración de escritorio seguro

Si la aplicación de accesibilidad admite el escritorio seguro, puede usar el Registro para copiar la configuración cuando la aplicación pasa al escritorio seguro. La copia de la configuración ayuda a que la transición al escritorio seguro sea más sencilla para el usuario.

Para copiar la configuración, establezca la clave del Registro CopySettingsToLockedDesktop de la aplicación en 1 y almacene la configuración en la siguiente ubicación del Registro.

**HKCU \\ Software Microsoft Windows NT \\ \\ \\ CurrentVersion \\ Accessibility \\ ATConfig\\<AT Key Name>**

El Centro de accesibilidad supervisa esta ubicación del Registro mientras se ejecuta la aplicación. Cuando se produce una transición al escritorio seguro, el Centro de accesibilidad copia la configuración en la misma ubicación en el subárbol HKCU del escritorio seguro. A continuación, la aplicación puede leer la configuración y reanudar su estado.

La aplicación de accesibilidad debe escribir su configuración a intervalos regulares o siempre que cambien los valores. La escritura de la configuración al salir de la aplicación no funcionará. Si la aplicación se ejecuta en un trabajo, se termina en la transición fuera del escritorio seguro, antes de que el código de salida tenga la oportunidad de ejecutarse. Si la aplicación no se ejecuta en un trabajo, la aplicación no finaliza en la transición fuera del escritorio seguro.

### <a name="caution"></a>Precaución

Dado que las claves del Registro descritas aquí se escriben en modo de usuario, no son seguras. Si la aplicación de accesibilidad lee el contenido de estas claves, debe comprobar cuidadosamente los datos y usarlos con precaución. En concreto, la aplicación debe realizar una comprobación de límites en los valores **DWORD,** tener cuidado con las longitudes de cadena, no debe leer nombres dll de complemento y no debe ejecutar ningún comando que se encuentra en cadenas.

## <a name="registry-examples"></a>Ejemplos del Registro

En el ejemplo siguiente se muestran los posibles valores del Registro para un producto ficticio denominado Contoso ScreenReader versión 2.0, cuyo nombre localizado se almacena como un recurso.

Los valores de la tabla están bajo la clave siguiente:

**HKLM \\ SOFTWARE Microsoft Windows NT \\ \\ \\ CurrentVersion \\ Accessibility \\ ATs Contoso Screen Reader \\ \_ \_ v2.0**



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>@%SystemRoot%\system32\ContosoRes.dll,-5020</td>
</tr>
<tr class="even">
<td>Descripción</td>
<td>REG_SZ</td>
<td>@%SystemRoot%\system32\ContosoRes.dll,-5040</td>
</tr>
<tr class="odd">
<td>Perfil</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&lt;HCIModel&gt;
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
&lt;/HCIModel&gt;</code></pre></td>
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
<td>StartExe</td>
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



 

Si la aplicación proporciona un lector de pantalla y una lupa de pantalla en un único ejecutable, los valores del componente de lector de pantalla podrían tener este aspecto:



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&lt;HCIModel&gt;
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
&lt;/HCIModel&gt;</code></pre></td>
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
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\Programa Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/r</td>
</tr>
</tbody>
</table>



 

Los valores del componente lupa estarían en la clave siguiente:

**HKLM \\ SOFTWARE Microsoft Windows NT \\ \\ \\ CurrentVersion \\ Contosoibility \\ ATs Contoso \\ \_ Luer \_ v2.0**



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&lt;HCIModel&gt;
   <Accommodation type=&quot;mild vision&quot; />
&lt;/HCIModel&gt;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>Ampliación</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>c:\Program Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/m</td>
</tr>
</tbody>
</table>



 

 

