---
description: Este tema contiene información sobre las API de bajo nivel que usa la infraestructura Windows cliente.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Compatibilidad con Low-Level varios clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffc5d32588089d3300ef59af17fe7ce2a0d0e99
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470182"
---
# <a name="miscellaneous-low-level-client-support"></a>Compatibilidad con Low-Level varios clientes

Este tema contiene información sobre las API de bajo nivel que usa la infraestructura Windows cliente.

### <a name="functions"></a>Functions




| Tema | Contenido | 
|-------|----------|
| <a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a> | La _lclose cierre el archivo especificado para que ya no esté disponible para lectura o escritura. Esta función se proporciona por compatibilidad con versiones de 16 bits de Windows. Las aplicaciones basadas en Win32 deben usar la función CloseHandle.<br /> | 
| <a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a> | La _lopen abre un archivo existente y establece el puntero de archivo al principio del archivo. Esta función se proporciona por compatibilidad con versiones de 16 bits de Windows. Las aplicaciones basadas en Win32 deben usar la función CreateFile. <br /> | 
| <a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a> | La _lread lee datos del archivo especificado. Esta función se proporciona por compatibilidad con versiones de 16 bits de Windows. Las aplicaciones basadas en Win32 deben usar la función ReadFile. <br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a> | Devuelve un valor que indica si los códecs de DVD están habilitados en el dispositivo actual.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a> | Deshabilita la característica de creación de fantasmas de ventana para el proceso de GUI de llamada. El fantasma de ventana es una característica Windows Manager que permite al usuario minimizar, mover o cerrar la ventana principal de una aplicación que no responde.<br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a> | Devuelve una lista de propiedades para todos los códecs multimedia instalados en el sistema que cumplen los requisitos especificados.<br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a> | Crea un generador de comunicaciones para registrar una extensión multimedia.<br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>Creación de una instancia deComponentFromPackage</strong></a> | Crea una instancia de una clase en un paquete de aplicación. <br /> | 
| <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a> | Obtiene un valor que indica si el comportamiento de los medios asociado al GUID especificado está habilitado.<br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> | En desuso. Esta función se usa para cerrar el identificador especificado. <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> se sustituye por <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle.</a><br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> | En desuso. Compila descriptores para los búferes proporcionados y pasa los datos sin tipo al controlador de dispositivo asociado al identificador de archivo. <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> es reemplazado por <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl.</a><br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> | En desuso. Espera hasta que el objeto especificado alcanza un estado de <code>signaled</code> . <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> se sustituye por <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject.</a><br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> | Convierte la cadena de origen ANSI especificada en una cadena Unicode. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a> | Convierte una cadena de caracteres en un entero.<br /> | 
| <a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a> | Inicializa el búfer proporcionado con una representación de cadena del SID para el usuario actual. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a> | Libera el búfer de cadena asignado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString.</strong></a><br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a> | Libera el búfer de cadena asignado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString.</strong></a><br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a> | Libera el búfer de cadena asignado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> o <a href="https://msdn.microsoft.com/library/ms803011.aspx">por RtlUpcaseUnicodeString.</a><br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a> | Inicializa una cadena con recuento. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a> | Inicializa una cadena Unicode con recuento. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a> | Convierte la cadena de origen Unicode especificada en una cadena ANSI. <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a> | Esta función convierte la cadena de origen Unicode especificada en una cadena OEM. La traducción se realiza con respecto a la página de códigos oem (OCP). <br /> | 
| <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a> | Determina cuántos bytes se necesitan para representar una cadena Unicode como una cadena ANSI.<br /> | 
| <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> | La <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>función RtlUnicodeToUTF8N</strong></a> convierte la cadena Unicode especificada en una nueva cadena de caracteres, mediante la página de códigos Formato de transformación Unicode de 8 bits (UTF-8).<br /> | 
| <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> | La <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>función RtlUTF8ToUnicodeN</strong></a> convierte la cadena de origen especificada en una cadena Unicode, mediante la página de códigos UTF-8.<br /> | 
| <a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a> | Especifica una acción o procesamiento para el Editor de métodos de entrada (IME) a través de una subfunción especificada.<blockquote>[!Note]<br />Esta función está obsoleta y no se debe usar.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a> | Habilita o deshabilita temporalmente un IME y, al mismo tiempo, activa o desactiva la presentación de todas las ventanas que pertenecen al IME.<blockquote>[!Note]<br />Esta función está obsoleta y no se debe usar.</blockquote><br /><br /> | 




 

### <a name="structures"></a>Estructuras



| Tema                                 | Contenido                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMESTRUCT**](/windows/win32/api/ime/ns-ime-imestruct) | Lo usa [**SendIMEMessageEx para**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) especificar la subfunción que se va a ejecutar en el mensaje IME y sus parámetros. Esta estructura también se usa para recibir valores devueltos de esas subfunciones.<br/> |
| [**CADENA**](/windows/desktop/api/Winternl/ns-winternl-string)       | Esta estructura se usa con la [**función RtlUnicodeStringToOemString.**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) <br/>                                                                                                              |



 

### <a name="compiler-routines"></a>Rutinas del compilador



| Tema                                                             | Contenido                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_\_Rutina \_ de controlador específico de C \_**](--c-specific-handler2.md) | [**\_ \_ El \_ controlador específico \_ de C**](--c-specific-handler2.md) es una rutina auxiliar para el compilador de C.<br/> |
| [\_alldiv (rutina)](-win32-alldiv.md)                             | [ \_ alldiv Routine es](-win32-alldiv.md) una rutina auxiliar para el compilador de C.<br/>                     |
| [\_allmul](-win32-allmul.md) | Multiplica dos **LONGLONG** o **ULONGLONG.** |
| [\_aulldiv](-win32-aulldiv.md) | Divide dos **enteros ULONGLONG.** |
| [\_chkstk (rutina)](-win32-chkstk.md)                             | [ \_ Chkstk Routine es](-win32-chkstk.md) una rutina auxiliar para el compilador de C.<br/>                     |
