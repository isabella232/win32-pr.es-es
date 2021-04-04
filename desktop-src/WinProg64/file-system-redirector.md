---
title: Redirector del sistema de archivos
description: El \\ directorio WINDIR system32 está reservado para las aplicaciones de 64 bits en Windows de 64 bits.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- 'redirector del sistema de archivos: programación de Windows de 64 bits'
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, redirector del sistema de archivos
- WOW64 64 bits programación de Windows, redirector del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561d03c8da51bd37a2d97746296bc74e24e43154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078082"
---
# <a name="file-system-redirector"></a>Redirector del sistema de archivos

El directorio% WINDIR% \\ system32 está reservado para aplicaciones de 64 bits en Windows de 64 bits. La mayoría de los nombres de archivo DLL no se cambiaron cuando se crearon las versiones de 64 bits de los archivos dll, por lo que las versiones de 32 bits de los archivos DLL se almacenan en un directorio diferente. WOW64 oculta esta diferencia mediante un *redirector del sistema de archivos*.

En la mayoría de los casos, cada vez que una aplicación de 32 bits intenta tener acceso a% WINDIR% \\ system32,% WINDIR% \\ lastgood \\ system32 o% WINDIR% \\regedit.exe, el acceso se redirige a una ruta de acceso específica de la arquitectura.

> [!Note]  
> Estas rutas de acceso se proporcionan únicamente como referencia. Por compatibilidad, las aplicaciones no deben usar estas rutas de acceso directamente. En su lugar, deben llamar a las API que se describen a continuación.

 



|                              |                                          |                                          |
|------------------------------|------------------------------------------|------------------------------------------|
| Ruta de acceso original                | Ruta de acceso redirigida para los procesos x86 de 32 bits | Ruta de acceso redirigida para procesos ARM de 32 bits |
| % WINDIR% \\ system32           | % WINDIR% \\ SysWOW64                       | % WINDIR% \\ SysArm32                       |
| % WINDIR% \\ lastgood \\ system32 | % WINDIR% \\ lastgood \\ SysWOW64             | % WINDIR% \\ lastgood \\ SysArm32             |
| % WINDIR% \\regedit.exe        | % WINDIR% \\ SysWOW64 \\regedit.exe          | % WINDIR% \\ SysArm32 \\regedit.exe         |



 

Si el acceso hace que el sistema muestre el mensaje de UAC, no se produce la redirección. En su lugar, se inicia la versión de 64 bits del archivo solicitado. Para evitar este problema, especifique el directorio SysWOW64 para evitar el redireccionamiento y asegúrese de tener acceso a la versión de 32 bits del archivo, o bien ejecute la aplicación de 32 bits con privilegios de administrador para que no se muestre la solicitud de UAC.

**Windows Server 2003 y Windows XP:  ** No se admite UAC.

Algunos subdirectorios están exentos de la redirección. El acceso a estos subdirectorios no se redirige a% WINDIR% \\ SysWOW64: <dl> % WINDIR% \\ system32 \\ catroot  
% WINDIR% \\ system32 \\ catroot2  
% WINDIR% \\ system32 \\ driverstore  
% WINDIR% \\ system32 \\ drivers, \\ etc.  
% WINDIR% \\ system32 \\ logfiles  
% WINDIR% \\ system32 \\ spool  
</dl>

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:  **% WINDIR% \\ system32 \\ driverstore es redirigido.

Para recuperar el nombre del directorio del sistema de 32 bits, las aplicaciones de 64 bits deben usar la función [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) (Windows 10, versión 1511) o la función [**GetSystemWow64Directory**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .

Las aplicaciones deben usar la función [**SHGetKnownFolderPath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) para determinar el nombre del directorio% programfiles%.

**Windows Server 2003 y Windows XP:** Las aplicaciones deben usar la función [**SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) para determinar el nombre del directorio% programfiles%.

Las aplicaciones pueden controlar el redirector del sistema de archivos WOW64 mediante las funciones [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection), [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)y [**Wow64RevertWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) . Deshabilitar la redirección del sistema de archivos afecta a todas las operaciones de archivo realizadas por el subproceso que realiza la llamada, por lo que debe deshabilitarse solo cuando sea necesario para una sola llamada [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y volver a habilitarla inmediatamente después de que se devuelva la función. Deshabilitar la redirección del sistema de archivos durante períodos más largos puede impedir que las aplicaciones de 32 bits carguen archivos DLL del sistema, lo que provocará un error en las aplicaciones.

las aplicaciones de 32 bits pueden tener acceso al directorio nativo del sistema sustituyendo% WINDIR% \\ Sysnative por% WINDIR% \\ system32. WOW64 reconoce Sysnative como un alias especial que se usa para indicar que el sistema de archivos no debe redirigir el acceso. Este mecanismo es flexible y fácil de usar, por lo tanto, es el mecanismo recomendado para omitir la redirección del sistema de archivos. Tenga en cuenta que las aplicaciones de 64 bits no pueden usar el alias Sysnative, ya que se trata de un directorio virtual no uno real.

**Windows Server 2003 y Windows XP:** El alias Sysnative se ha agregado a partir de Windows Vista.

 

 