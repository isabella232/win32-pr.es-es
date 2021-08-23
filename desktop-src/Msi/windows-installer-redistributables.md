---
description: El instalador Windows redistribuible es un paquete de actualización de software.
ms.assetid: 8491dfa6-b9be-4e37-8a61-a405c8eb0ab0
title: Redistribuibles de Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 831abe9a19f8b2d4999229b1d40e701c5869aa79e6dda9f0933ab8117656652b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526705"
---
# <a name="windows-installer-redistributables"></a>Redistribuibles de Windows Installer

Windows El instalador 4.5 y versiones anteriores está disponible como un paquete de actualización de software redistribuible. Consulte la sección [Versiones publicadas de Windows Installer para](released-versions-of-windows-installer.md) determinar qué productos enviaron las versiones del Windows instalador. El paquete de actualización redistribuible de una versión está disponible después del lanzamiento del producto que se incluye con una versión Windows instalador.

> [!NOTE]
> No hay ningún redistribuible para Windows Installer 5.0. Esta versión se incluye con el sistema operativo en Windows 7, Windows Server 2008 R2 y versiones posteriores de cliente y servidor (incluidas Windows 10).

## <a name="obtaining-the-windows-installer-redistributable-45-and-earlier"></a>Obtener el instalador Windows redistribuible (4.5 y versiones anteriores)

-   Puede encontrar todos los archivos redistribuibles Windows Installer disponibles en el [Centro de descarga de Microsoft](https://www.microsoft.com/Downloads/).
-   La descarga del paquete [redistribuible Windows Installer 4.5](https://support.microsoft.com/kb/942288) está disponible en: https://go.microsoft.com/fwlink/p/?LinkID=101159 .
-   El nombre del redistribuible que instala Windows Installer 4.5 en equipos basados en x86 que ejecutan Windows Vista, Windows Vista con Service Pack 1 (SP1) y Windows Server 2008 es Windows6.0-KB942288-v2-x86.MSU.
-   El nombre del redistribuible que instala Windows Installer 4.5 en equipos basados en x64 que ejecutan Windows Vista, Windows Vista con SP1 y Windows Server 2008 es Windows6.0-KB942288-v2-x64.MSU.
-   El nombre del redistribuible que instala Windows Installer 4.5 en equipos de Itanium-Based Systems que ejecutan Windows Vista, Windows Vista con SP1 y Windows Server 2008 es Windows6.0-KB942288-v2-ia64.MSU.
-   El nombre del redistribuible que instala Windows Installer 4.5 en equipos basados en x86 que ejecutan Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3) es WindowsXP-KB942288-v3-x86.exe.
-   El nombre del redistribuible que instala Windows Installer 4.5 en equipos basados en x86 que ejecutan Windows Server 2003 con Service Pack 1 (SP1) y Windows Server 2003 con Service Pack 2 (SP2) es WindowsServer2003-KB942288-v4-x86.exe.
-   El nombre del redistribuible que instala Windows Installer 4.5 en equipos basados en x64 que ejecutan Windows Server 2003 con SP1 y Windows Server 2003 con SP2 es WindowsServer2003-KB942288-v4-x64.exe.
-   El nombre del redistribuible que instala Windows Installer 4.5 en equipos de Itanium-Based Systems que ejecutan Windows Server 2003 con SP1 y Windows Server 2003 con SP2 es WindowsServer2003-KB942288-v4-ia64.exe.
-   No hay ningún redistribuible que instale Windows Installer 4.0. Esta versión del instalador de Windows se incluye Windows Vista.
-   El nombre del redistribuible que instala Windows Installer 3.1 es WindowsInstaller-KB893803-v2-x86.exe. La descarga del paquete [Windows Installer 3.1 Redistributable (v2)](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c) está disponible en: https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c .
    > [!Note]  
    > Si ha actualizado a Windows Installer 3.1 mediante la instalación de Windows Server 2003 con SP1 o una versión anterior de este redistribuible, es posible que también tenga que instalar update [for Windows Server 2003 Service Pack 1 (KB898715)](https://www.microsoft.com/downloads/details.aspx?FamilyID=8b4e6b93-1886-4d47-a18d-35581c42eca0) para obtener todas las actualizaciones disponibles en [Windows Installer 3.1 Redistributable (v2).](https://www.microsoft.com/downloads/details.aspx?FamilyID=889482fc-5f56-4a38-b838-de776fd4138c)

     

-   El redistribuible que instala Windows Installer 3.0 es WindowsInstaller-KB884016-v2-x86.exe. La descarga de [Windows Installer 3.0 Redistributable](https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8) está disponible en: https://www.microsoft.com/downloads/details.aspx?FamilyID=5fbc5470-b259-4733-a914-a956122e08e8 .
-   El Windows 2.0 usó una convención de nomenclatura anterior para el redistribuible: [Instmsi.exe](instmsi-exe.md). El redistribuible para instalar o actualizar a Windows Installer 2.0 en Windows 2000 no debe usarse para instalar o actualizar Windows Installer 2.0 en Windows Server 2003 y Windows XP.

    La descarga del instalador [de Windows 2.0 Redistributable para Windows NT 4.0 y Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f) está disponible en https://www.microsoft.com/downloads/details.aspx?FamilyID=4b6140f9-2d36-4977-8fa1-6f8a0f5dca8f .

## <a name="installing-the-windows-installer-redistributable-45-and-earlier"></a>Instalación de Windows Installer Redistributable (4.5 y versiones anteriores)

El instalador de Windows 4.5 se proporciona para los sistemas operativos Windows Vista y Windows Server 2008 como un archivo .msu y debe instalarse mediante el instalador independiente de Windows [Update](https://support.microsoft.com/kb/934307/) (Wusa.exe).

El instalador de Windows 4.5 redistribuible para los sistemas operativos Windows XP y Windows Server 2003 se puede instalar mediante las siguientes opciones y sintaxis de línea de comandos.

Los archivos redistribuibles Windows Installer 3.1 y Windows Installer 3.0 se pueden instalar mediante la siguiente sintaxis y opciones de línea de comandos.

### <a name="syntax"></a>Syntax

Use la sintaxis siguiente para instalar los redistribuibles para Windows Installer 4.5 en Windows XP y Windows Server 2003.

```CMD
<Name of the Redistributable>\[<options>\]*
```

### <a name="command-line-options"></a>Opciones de la línea de comandos

Los Windows paquetes de actualización de software redistribuibles del instalador de aplicaciones usan las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas.



| Opción     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /norestart | Impide que el paquete redistribuible pida al usuario que reinicie, incluso si tuviera que reemplazar los archivos que estaban en uso durante la instalación. Si el paquete de actualización se invoca con esta opción, devuelve **ERROR \_ SUCCESS REBOOT \_ \_ REQUIRED** si tuviera que reemplazar los archivos que estaban en uso.<br/> Si no tenía que reemplazar los archivos que estaban en uso, devuelve **ERROR \_ SUCCESS**. Consulte la sección de comentarios para obtener información adicional sobre los reinicios retrasados.<br/> |
| /quiet     | Para su uso por parte de las aplicaciones que redistribuyen Windows installer como parte de una aplicación de arranque. Una interfaz de usuario (UI) no se presenta al usuario. La aplicación de arranque debe comprobar el código de retorno para determinar si es necesario reiniciar para completar la instalación del instalador Windows.<br/>                                                                                                                                                |
| /help      | Muestra ayuda sobre todas las opciones disponibles.                                                                                                                                                                                                                                                                                                                                                                                                                                     |

### <a name="delayed-restart-on-windows-vista-and-windows-server-2008"></a>Reinicio retrasado en Windows Vista y Windows Server 2008

La opción de línea de comandos /norestart impide wusa.exe reiniciar el equipo. Sin embargo, si un archivo que está actualizando el paquete MSU está en uso, el paquete no se aplica al equipo hasta que el usuario reinicia el equipo. Esto significa que las aplicaciones que usan el instalador de Windows 4.5 redistribuible para Windows Vista y Windows Server 2008 no pueden usar la funcionalidad del Instalador de Windows 4.5 hasta que se reinicie el equipo.

### <a name="delayed-restart-on-windows-xp-and-windows-server-2003"></a>Reinicio retrasado en Windows XP y Windows Server 2003

Se recomienda detener el servicio Windows instalador cuando se usa el paquete de actualización. Cuando el paquete se ejecuta en modo de interfaz de usuario completa, detecta si el servicio Windows Installer se está ejecutando y solicita al usuario que detenga el servicio. Si el usuario continúa sin detener el servicio, la actualización reemplaza Windows Instalador.

[El arranque](bootstrapping.md) de aplicaciones que usan el paquete redistribuible para instalar el instalador de Windows con otra aplicación puede requerir un reinicio adicional del sistema, además de los reinicios necesarios para instalar la aplicación. La opción de reinicio retrasado solo se recomienda para los casos en los que es necesario eliminar un reinicio adicional causado por la instalación de archivos que están en uso. Los desarrolladores deben hacer lo siguiente en su aplicación de instalación para usar la opción de reinicio retrasado.

-   Llame al paquete redistribuible con la opción de línea de comandos /norestart.
-   Trate la devolución de **ERROR \_ SUCCESS o** ERROR SUCCESS REBOOT REQUIRED **\_ \_ \_ como** correcto.
-   Invoque Msiexec en el paquete de la aplicación y ejecute otro código de instalación específico de la aplicación. Si la aplicación de instalación usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), la aplicación debe cargar MSI.DLL desde el directorio del sistema. Si no se produce ningún reinicio y el redistribuible devuelve **ERROR \_ SUCCESS REBOOT \_ \_ REQUIRED**, solicite al usuario un reinicio para completar la instalación de los archivos binarios del instalador de Windows. Si se produce un reinicio, no se requieren pasos adicionales.
    > [!Note]  
    > Las aplicaciones que llaman a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) en el nuevo MSI.DLL después de que el paquete redistribuible devuelva un resultado correcto deben asegurarse de que una versión anterior de MSI.DLL no se haya cargado ya dentro del proceso. Si se cargó una versión anterior de MSI.DLL, se debe descargar del espacio de direcciones del proceso antes de llamar a **LoadLibrary** para el nuevo MSI.DLL.

     

Para obtener más información, [vea Windows Installer Bootstrapping](windows-installer-bootstrapping.md).

 

 
