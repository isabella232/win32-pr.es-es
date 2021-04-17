---
description: El Windows Installer redistribuible es un paquete de actualización de software.
ms.assetid: 8491dfa6-b9be-4e37-8a61-a405c8eb0ab0
title: Redistribuibles de Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 9fc175a96ae1d2daed9798981b0dbe679505975e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652779"
---
# <a name="windows-installer-redistributables"></a>Redistribuibles de Windows Installer

Windows Installer 4,5 y versiones anteriores están disponibles como un paquete de actualización de software redistribuible. Vea la sección [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md) para determinar qué productos distribuyeron versiones de la Windows Installer. El paquete de actualización redistribuible de una versión está disponible después del lanzamiento del producto que se distribuye con una versión de Windows Installer específica.

> [!NOTE]
> No hay ningún redistribuible para Windows Installer 5,0. Esta versión se incluye con el sistema operativo en Windows 7, Windows Server 2008 R2 y versiones posteriores de cliente y servidor (incluido Windows 10).

## <a name="obtaining-the-windows-installer-redistributable-45-and-earlier"></a>Obtención del Windows Installer redistribuible (4,5 y versiones anteriores)

-   Puede encontrar todos los Windows Installer redistribuibles disponibles en el [centro de descarga de Microsoft](https://www.microsoft.com/Downloads/).
-   La descarga del [paquete redistribuible de Windows Installer 4,5](https://support.microsoft.com/kb/942288) está disponible en: https://go.microsoft.com/fwlink/p/?LinkID=101159 .
-   El nombre del redistribuible que instala Windows Installer 4,5 en equipos basados en x86 que ejecutan Windows Vista, Windows Vista con Service Pack 1 (SP1) y Windows Server 2008 es Windows 6.0-KB942288-v2-x86. MSU.
-   El nombre del redistribuible que instala Windows Installer 4,5 en equipos basados en x64 que ejecutan Windows Vista, Windows Vista con SP1 y Windows Server 2008 es Windows 6.0-KB942288-v2-x64. MSU.
-   El nombre del redistribuible que instala Windows Installer 4,5 en Itanium-Based equipos con Windows Vista, Windows Vista con SP1 y Windows Server 2008 es Windows 6.0-KB942288-v2-ia64. MSU.
-   Se WindowsXP-KB942288-v3-x86.exe el nombre del redistribuible que instala Windows Installer 4,5 en equipos basados en x86 que ejecutan Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3).
-   Se WindowsServer2003-KB942288-v4-x86.exe el nombre del redistribuible que instala Windows Installer 4,5 en equipos basados en x86 que ejecutan Windows Server 2003 con Service Pack 1 (SP1) y Windows Server 2003 con Service Pack 2 (SP2).
-   WindowsServer2003-KB942288-v4-x64.exe es el nombre del redistribuible que instala Windows Installer 4,5 en equipos basados en x64 que ejecutan Windows Server 2003 con SP1 y Windows Server 2003 con SP2.
-   El nombre del redistribuible que instala Windows Installer 4,5 en Itanium-Based los equipos de sistemas que ejecutan Windows Server 2003 con SP1 y Windows Server 2003 con SP2 es WindowsServer2003-KB942288-v4-ia64.exe.
-   No hay ningún redistribuible que instale Windows Installer 4,0. Esta versión del Windows Installer se incluye con Windows Vista.
-   El nombre del redistribuible que instala Windows Installer 3,1 es WindowsInstaller-KB893803-v2-x86.exe. La descarga del paquete [Windows Installer 3,1 Redistributable (V2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c) está disponible en: https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c .
    > [!Note]  
    > Si ha actualizado a Windows Installer 3,1 mediante la instalación de Windows Server 2003 con SP1 o una versión anterior de este redistribuible, es posible que también deba instalar la [actualización de Windows server 2003 Service Pack 1 (KB898715)](https://www.microsoft.com/downloads/details.aspx?FamilyID=8b4e6b93-1886-4d47-a18d-35581c42eca0) para obtener todas las actualizaciones disponibles en [Windows Installer 3,1 Redistributable (V2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c).

     

-   El redistribuible que instala Windows Installer 3,0 es WindowsInstaller-KB884016-v2-x86.exe. La descarga del [paquete redistribuible Windows Installer 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8) está disponible en: https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8 .
-   El Windows Installer 2,0 usó una Convención de nomenclatura anterior para el redistribuible: [Instmsi.exe](instmsi-exe.md). El redistribuible para instalar o actualizar a Windows Installer 2,0 en Windows 2000 no debe usarse para instalar o actualizar Windows Installer 2,0 en Windows Server 2003 y Windows XP.

    La descarga del [Windows Installer 2,0 Redistributable para Windows NT 4,0 y windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f) está disponible en https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f .

## <a name="installing-the-windows-installer-redistributable-45-and-earlier"></a>Instalación del Windows Installer redistribuible (4,5 y versiones anteriores)

El Windows Installer 4,5 resdistributable se proporciona para los sistemas operativos Windows Vista y Windows Server 2008 como archivo. MSU y debe instalarse con el [instalador independiente de Windows Update](https://support.microsoft.com/kb/934307/) (Wusa.exe).

Los sistemas operativos Windows Installer 4,5 Redistributable para Windows XP y Windows Server 2003 se pueden instalar con las siguientes opciones y sintaxis de línea de comandos.

Los redistribuibles Windows Installer 3,1 y Windows Installer 3,0 se pueden instalar con las siguientes opciones y sintaxis de línea de comandos.

### <a name="syntax"></a>Sintaxis

Use la siguiente sintaxis para instalar los redistribuibles para Windows Installer 4,5 en Windows XP y Windows Server 2003.

```CMD
<Name of the Redistributable>\[<options>\]*
```

### <a name="command-line-options"></a>Opciones de la línea de comandos

Los paquetes de actualización de software redistribuibles de Windows Installer usan las siguientes opciones de línea de comandos que no distinguen mayúsculas de minúsculas.



| Opción     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /norestart | Impide que el paquete redistribuible solicite al usuario que reinicie, incluso si tenía que reemplazar los archivos que estaban en uso durante la instalación. Si el paquete de actualización se invoca con esta opción, devolverá un **error de \_ \_ reinicio correcto \_ necesario** si tuviera que reemplazar los archivos que estaban en uso.<br/> Si no tuviera que reemplazar los archivos que estaban en uso, devolverá el **error \_ Success**. Vea la sección Comentarios para obtener información adicional sobre los reinicios retrasados.<br/> |
| /quiet     | Lo usan las aplicaciones que redistribuyen el Windows Installer como parte de una aplicación de arranque. Una interfaz de usuario (UI) no se presenta al usuario. La aplicación de arranque debe comprobar el código de retorno para determinar si es necesario reiniciar para completar la instalación del Windows Installer.<br/>                                                                                                                                                |
| /help      | Muestra la ayuda en todas las opciones disponibles.                                                                                                                                                                                                                                                                                                                                                                                                                                     |

### <a name="delayed-restart-on-windows-vista-and-windows-server-2008"></a>Reinicio retrasado en Windows Vista y Windows Server 2008

La opción de línea de comandos/norestart impide que wusa.exe reinicie el equipo. Sin embargo, si un archivo que se está actualizando mediante el paquete MSU está en uso, el paquete no se aplica al equipo hasta que el usuario reinicia el equipo. Esto significa que las aplicaciones que usan el Windows Installer 4,5 Redistributable para Windows Vista y Windows Server 2008 no pueden usar la funcionalidad de Windows Installer 4,5 hasta que se reinicie el equipo.

### <a name="delayed-restart-on-windows-xp-and-windows-server-2003"></a>Reinicio retrasado en Windows XP y Windows Server 2003

Se recomienda detener el servicio Windows Installer cuando se use el paquete de actualización. Cuando el paquete se ejecuta en modo de interfaz de usuario completa, detecta si el servicio Windows Installer se está ejecutando y solicita al usuario que detenga el servicio. Si el usuario continúa sin detener el servicio, la actualización reemplaza Windows Installer.

Las aplicaciones de [arranque](bootstrapping.md) que usan el paquete redistribuible para instalar el Windows Installer con otra aplicación pueden requerir un reinicio adicional del sistema además de los reinicios necesarios para instalar la aplicación. La opción retardo de reinicio solo se recomienda para los casos en los que es necesario eliminar un reinicio adicional debido a la instalación de archivos que están en uso. Los desarrolladores deben hacer lo siguiente en su aplicación de instalación para utilizar la opción de reinicio retrasado.

-   Llame al paquete redistribuible con la opción de línea de comandos/norestart.
-   Trate el resultado de que se **\_ \_ reinicien \_** los errores **\_ correctos** o correctos con éxito, como lo que significa que es correcto.
-   Invoque msiexec en el paquete de la aplicación y ejecute otro código de instalación específico de la aplicación. Si la aplicación de instalación usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), la aplicación debe cargar MSI.DLL del directorio del sistema. Si no se produce ningún reinicio y el redistribuible devolvió un error, se **\_ \_ \_ requiere** un reinicio correcto para completar la instalación de los archivos binarios de Windows Installer. Si se produce un reinicio, no es necesario realizar ningún paso adicional.
    > [!Note]  
    > Las aplicaciones que llaman a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) en el nuevo MSI.DLL después de que el paquete redistribuible devuelva Success deben asegurarse de que no se haya cargado previamente una versión anterior de MSI.DLL en el proceso. Si se cargó una versión anterior de MSI.DLL, se debe descargar del espacio de direcciones de proceso antes de llamar a **LoadLibrary** para el nuevo MSI.DLL.

     

Para obtener más información, vea [Windows Installer arranque](windows-installer-bootstrapping.md).

 

 
