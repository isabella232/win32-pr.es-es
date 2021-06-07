---
title: Redirector del sistema de archivos
description: El directorio System32 windir \\ está reservado para aplicaciones de 64 bits en Windows de 64 bits.
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- Programación de Windows de redirector de sistema de archivos de 64 bits
- Guía de programación de Windows de 64 bits programación de Windows de 64 bits, redirector del sistema de archivos
- WOW64 Programación de Windows de 64 bits, redirector del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568ddde85d18f90b951051251774c3509081dfdd
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443636"
---
# <a name="file-system-redirector"></a>Redirector del sistema de archivos

El directorio %windir% System32 está reservado para aplicaciones de \\ 64 bits en Windows de 64 bits. La mayoría de los nombres de archivo DLL no se cambiaron cuando se crearon versiones de 64 bits de los archivos DLL, por lo que las versiones de 32 bits de los archivos DLL se almacenan en un directorio diferente. WOW64 oculta esta diferencia mediante un *redirector del sistema de archivos*.

En la mayoría de los casos, cada vez que una aplicación de 32 bits intenta acceder a %windir% \\ System32, %windir% \\ lastgood \\ system32 o %windir%regedit.exe, el acceso se redirige a una ruta de acceso específica de la \\ arquitectura.

> [!Note]  
> Estas rutas de acceso solo se proporcionan como referencia. Por compatibilidad, las aplicaciones no deben usar estas rutas de acceso directamente. En su lugar, deben llamar a las API que se describen a continuación.

 



| Ruta de acceso original                | Ruta de acceso redirigida para procesos x86 de 32 bits | Ruta de acceso redirigida para procesos arm de 32 bits |
|------------------------------|------------------------------------------|------------------------------------------|
| %windir% \\ System32           | %windir% \\ SysWOW64                       | %windir% \\ SysArm32                       |
| %windir% \\ lastgood \\ system32 | %windir% \\ lastgood \\ SysWOW64             | %windir% \\ lastgood \\ SysArm32             |
| %windir% \\regedit.exe        | %windir% \\ SysWOW64 \\regedit.exe          | %windir% \\ SysArm32 \\regedit.exe         |



 

Si el acceso hace que el sistema muestre el símbolo del sistema de UAC, no se produce el redireccionamiento. En su lugar, se inicia la versión de 64 bits del archivo solicitado. Para evitar este problema, especifique el directorio SysWOW64 para evitar el redireccionamiento y garantizar el acceso a la versión de 32 bits del archivo, o ejecute la aplicación de 32 bits con privilegios de administrador para que no se muestre el símbolo del sistema de UAC.

**Windows Server 2003 y Windows XP: ** No se admite UAC.

Algunos subdirectorios están exentos del redireccionamiento. El acceso a estos subdirectorios no se redirige a %windir% \\ SysWOW64: <dl> %windir% \\ system32 \\ catroot  
%windir% \\ system32 \\ catroot2  
%windir% \\ system32 \\ driverstore  
%windir% \\ system32 \\ drivers \\ etc.  
%windir% \\ system32 \\ logfiles  
%windir% \\ system32 \\ spool  
</dl>

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP: **%windir% \\ system32 \\ driverstore se redirige.

Para recuperar el nombre del directorio del sistema de 32 bits, las aplicaciones de 64 bits deben usar la función [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) (Windows 10, versión 1511) o la [**función GetSystemWow64Directory.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)

Las aplicaciones deben usar [**la función SHGetKnownFolderPath para**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) determinar el nombre de directorio %ProgramFiles%.

**Windows Server 2003 y Windows XP:** Las aplicaciones deben usar [**la función SHGetSpecialFolderPath para**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) determinar el nombre de directorio %ProgramFiles%.

Las aplicaciones pueden controlar el redirector del sistema de archivos WOW64 mediante las funciones [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection), [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)y [**Wow64RevertWow64FsRedirection.**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) Deshabilitar el redireccionamiento del sistema de archivos afecta a todas las operaciones de archivo realizadas por el subproceso que realiza la llamada, por lo que solo debe deshabilitarse cuando sea necesario para una única llamada [**a CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y volver a habilitarse inmediatamente después de que se devuelva la función. Deshabilitar la redirección del sistema de archivos durante períodos más largos puede impedir que las aplicaciones de 32 bits carguen archivos DLL del sistema, lo que provoca un error en las aplicaciones.

Las aplicaciones de 32 bits pueden acceder al directorio del sistema nativo sustituyendo %windir% \\ Sysnative por %windir% \\ System32. WOW64 reconoce Sysnative como un alias especial que se usa para indicar que el sistema de archivos no debe redirigir el acceso. Este mecanismo es flexible y fácil de usar, por lo que es el mecanismo recomendado para omitir el redireccionamiento del sistema de archivos. Tenga en cuenta que las aplicaciones de 64 bits no pueden usar el alias Sysnative, ya que es un directorio virtual no real.

**Windows Server 2003 y Windows XP:** El alias Sysnative se agregó a partir de Windows Vista.

 

 