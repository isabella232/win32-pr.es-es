---
description: Este tema contiene información acerca de las API de bajo nivel utilizadas por la infraestructura de cliente de Windows.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Compatibilidad con clientes Low-Level varios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906916"
---
# <a name="miscellaneous-low-level-client-support"></a>Compatibilidad con clientes Low-Level varios

Este tema contiene información acerca de las API de bajo nivel utilizadas por la infraestructura de cliente de Windows.

### <a name="functions"></a>Functions



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></td>
<td>La función _lclose cierra el archivo especificado para que ya no esté disponible para lectura o escritura. Esta función se proporciona por compatibilidad con las versiones de 16 bits de Windows. Las aplicaciones basadas en Win32 deben usar la función CloseHandle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></td>
<td>La función _lopen abre un archivo existente y establece el puntero de archivo al principio del archivo. Esta función se proporciona por compatibilidad con las versiones de 16 bits de Windows. Las aplicaciones basadas en Win32 deben utilizar la función CreateFile. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></td>
<td>La función _lread lee datos del archivo especificado. Esta función se proporciona por compatibilidad con las versiones de 16 bits de Windows. Las aplicaciones basadas en Win32 deben utilizar la función ReadFile. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></td>
<td>Devuelve un valor que indica si se habilitan los códecs de DVD en el dispositivo actual.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></td>
<td>Deshabilita la característica de fantasma de la ventana para el proceso de llamada a la GUI. El fantasma de las ventanas es una característica del administrador de Windows que permite al usuario minimizar, trasladar o cerrar la ventana principal de una aplicación que no responde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></td>
<td>Devuelve una lista de propiedades para todos los códecs multimedia instalados en el sistema que cumplan los requisitos especificados.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></td>
<td>Crea una factoría de comunicaciones para registrar una extensión de medios.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></td>
<td>Crea una instancia de una clase en un paquete de aplicación. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></td>
<td>Obtiene un valor que indica si está habilitado el comportamiento multimedia asociado con el GUID especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></td>
<td>En desuso. Esta función se utiliza para cerrar el identificador especificado. El <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> se sustituye por <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></td>
<td>En desuso. Compila los descriptores de los búferes proporcionados y pasa los datos sin tipo al controlador de dispositivo asociado al identificador de archivo. <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>sustituye a <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></td>
<td>En desuso. Espera hasta que el objeto especificado alcanza un estado de <code>signaled</code> . <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>sustituye a <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></td>
<td>Convierte la cadena de origen ANSI especificada en una cadena Unicode. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></td>
<td>Convierte una cadena de caracteres en un entero.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></td>
<td>Inicializa el búfer proporcionado con una representación de cadena del SID del usuario actual. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></td>
<td>Libera el búfer de cadena asignado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></td>
<td>Libera el búfer de cadena asignado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></td>
<td>Libera el búfer de cadena asignado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> o <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></td>
<td>Inicializa una cadena contada. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></td>
<td>Inicializa una cadena Unicode contada. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></td>
<td>Convierte la cadena de origen Unicode especificada en una cadena ANSI. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></td>
<td>Esta función convierte la cadena de origen Unicode especificada en una cadena OEM. La traducción se realiza con respecto a la página de códigos OEM (OCP). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></td>
<td>Determina el número de bytes necesarios para representar una cadena Unicode como una cadena ANSI.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></td>
<td>La función <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> traduce la cadena Unicode especificada en una nueva cadena de caracteres, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></td>
<td>La función <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> traduce la cadena de origen especificada en una cadena Unicode, mediante la página de códigos UTF-8.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></td>
<td>Especifica una acción o procesamiento para el editor de métodos de entrada (IME) a través de una subfunción especificada.
<blockquote>
[!Note]<br />
Esta función está obsoleta y no debe usarse.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></td>
<td>Habilita o deshabilita temporalmente un IME y, al mismo tiempo, activa o desactiva la visualización de todas las ventanas propiedad del IME.
<blockquote>
[!Note]<br />
Esta función está obsoleta y no debe usarse.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>Estructuras



| Tema                                 | Contenido                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMESTRUCT**](/windows/win32/api/ime/ns-ime-imestruct) | Lo usa [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) para especificar la subfunción que se va a ejecutar en el mensaje IME y sus parámetros. Esta estructura también se usa para recibir los valores devueltos de esas subfunciones.<br/> |
| [**String@**](/windows/desktop/api/Winternl/ns-winternl-string)       | Esta estructura se usa con la función [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) . <br/>                                                                                                              |



 

### <a name="compiler-routines"></a>Rutinas del compilador



| Tema                                                             | Contenido                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_\_\_Rutina de controlador específica de C \_**](--c-specific-handler2.md) | El [**\_ \_ \_ \_ controlador específico de c**](--c-specific-handler2.md) es una rutina auxiliar para el compilador de c.<br/> |
| [\_Rutina alldiv](-win32-alldiv.md)                             | [ \_ alldiv rutina](-win32-alldiv.md) es una rutina auxiliar para el compilador de C.<br/>                     |
| [\_allmul](-win32-allmul.md) | Multiplica dos **LONGLONG** o **ULONGLONG**. |
| [\_aulldiv](-win32-aulldiv.md) | Divide dos enteros **ULONGLONG** . |
| [\_Rutina chkstk](-win32-chkstk.md)                             | [ \_ chkstk rutina](-win32-chkstk.md) es una rutina auxiliar para el compilador de C.<br/>                     |
