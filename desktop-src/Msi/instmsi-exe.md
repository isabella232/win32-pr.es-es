---
description: Instmsi.exe es el paquete redistribuible para instalar Windows Installer&\# 160;2.0 y versiones anteriores de Windows Installer. Vea Windows Installer Redistributables for the redistributables for Windows Installer&160;3.0 and later versions (Redistributables del instalador de Windows para&\# 160;3.0 y versiones posteriores).
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2177fbb145dbfe2817dba2207cff95e5d80b801cc2f442085ba396f461870f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946123"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe es el paquete redistribuible para instalar Windows Installer 2.0 y versiones anteriores de Windows Installer. Consulte [Windows Installer Redistributables](windows-installer-redistributables.md) para los redistribuibles para Windows Installer 3.0 y versiones posteriores.

Para obtener más información sobre qué versión del instalador de Windows se ha incluido con el sistema operativo, vea Versiones publicadas [de Windows Installer](released-versions-of-windows-installer.md).

Algunas redistribuibles no deben ejecutarse en determinadas versiones del sistema operativo. En la tabla siguiente se describe qué instmsi es compatible con qué sistema operativo.



| Si Instmsi.exe instala esta versión del instalador de Windows | Instmsi.exe se pueden ejecutar en estos sistemas operativos                    | Instmsi.exe deben ejecutarse en estos sistemas operativos                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows Versión del instalador 1.0                                 | Windows 95, Windows 98, Windows NT 4.0+SP3                           | Windows Me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Versión del instalador 1.1                                 | Windows 95, Windows 98, Windows NT 4.0+SP3                           | Windows Me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Versión del instalador 1.2                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0+SP3               | Windows 2000, Windows XP, Windows Server 2003, Windows Vista y Windows Server 2008             |
| Windows Versión del instalador 2.0                                 | Windows 95, Windows 98, Windows Me, Windows NT 4.0+SP6, Windows 2000 | Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008                           |



 

Por ejemplo, una aplicación que redistribuya Windows Installer versión 1.1 debe comprobar que el sistema operativo es Windows NT 4.0 SP3 o Windows 98/95 antes de ejecutar el paquete redistribuible. Las aplicaciones que usan el paquete redistribuible también deben asegurarse de que la versión ANSI del instalador de Windows esté instalada en Windows 98/95 y que la versión Unicode esté instalada en Windows NT o Windows 2000. Tenga en cuenta que algunas aplicaciones cambiarán el nombre de la versión Unicode a InstMsiW.

## <a name="syntax"></a>Syntax

**opciones de instmsi** 

## <a name="command-line-options"></a>Opciones de la línea de comandos

Las opciones de línea de comandos no tienen en cuenta mayúsculas de minúsculas.



| Opción                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | Para su uso por parte de las aplicaciones que redistribuyen Windows Installer como parte de una aplicación de arranque. No se presenta ninguna interfaz de usuario al usuario. La aplicación de arranque debe comprobar el código de retorno para determinar si se necesita un reinicio para completar la instalación del Windows instalador.                                                                                                                                                                                                                          |
| /t                         | Se usa solo con fines de depuración.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c:"msiinst /delayreboot"  | Opción de reinicio retrasado. Impide que Instmsi pida al usuario un reinicio, incluso si tuviera que reemplazar los archivos que estaban en uso durante la instalación. Si se invoca Instmsi con esta opción, devuelve ERROR SUCCESS REBOOT REQUIRED si tuviera que reemplazar los archivos \_ \_ que estaban en \_ uso. Si no tenía que reemplazar los archivos que estaban en uso, devuelve ERROR \_ SUCCESS. Disponible con Instmsi para Windows Installer 2.0 o posterior. Consulte la sección comentarios para obtener información adicional sobre los reinicios retrasados.<br/> |
| /c:"msiinst /delayrebootq" | La versión silenciosa de la opción de reinicio retrasado. No presenta ninguna interfaz de usuario al usuario. De lo contrario, el comportamiento es idéntico a la opción anterior. Disponible con Instmsi para Windows Installer 2.0 o posterior. Consulte la sección comentarios para obtener información adicional sobre los reinicios retrasados.<br/>                                                                                                                                                                                                                           |
| /?                         | Muestra información de ayuda.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentarios

[El arranque](bootstrapping.md) de aplicaciones que usan Instmsi.exe para instalar Windows Installer con otra aplicación puede requerir un reinicio adicional del sistema. Esto puede ser un reinicio adicional además de los reinicios necesarios para instalar la aplicación.

La opción de reinicio retrasado solo se recomienda para los desarrolladores de instalación que desean eliminar un reinicio adicional causado por el uso de Instmsi.exe con una aplicación de instalación que instala los archivos que están en uso.

Los desarrolladores deben hacer lo siguiente en su aplicación de instalación para usar la opción de reinicio retrasado. Esta opción no está disponible con Instmsi.exe que instalan versiones de Windows Installer anteriores a la versión 2.0:

**Para usar la opción de reinicio retrasado**

1.  Llame Instmsi.exe con una de las opciones de línea de comandos de reinicio retrasado.
2.  Trate la devolución de ERROR \_ SUCCESS o ERROR SUCCESS REBOOT REQUIRED como \_ \_ \_ correcto.
3.  Obtenga la ruta de acceso a la carpeta que contiene los archivos binarios Windows Installer recién instalados desde el valor InstallerLocation en:

    **HKEY \_ Software \_ local** \\ **de** \\ **Microsoft** \\ **Windows** \\ **Instalador de** \\ **CurrentVersion**

    Este valor es de tipo **REG \_ SZ.**

4.  Establezca el directorio actual en la ruta de acceso obtenida en el paso 3.
5.  Invoque Msiexec en el paquete de la aplicación y ejecute otro código de instalación específico de la aplicación. Si la aplicación de instalación usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), la aplicación debe cargar MSI.DLL desde la ubicación obtenida en el paso 3.
    > [!Note]  
    > Las aplicaciones que llaman **a LoadLibrary** en el nuevo MSI.DLL en la ubicación obtenida en el paso 3 deben asegurarse de que no se haya cargado una versión anterior de MSI.DLL en el proceso. Si se cargó una versión anterior de MSI.DLL en el proceso, se debe descargar desde el espacio de direcciones del proceso antes de la llamada **LoadLibrary** para el nuevo MSI.DLL.

     

6.  Si el paso (5) no requiere un reinicio y Instmsi.exe ha devuelto ERROR SUCCESS REBOOT REQUIRED en el paso \_ \_ (1), solicite al usuario un reinicio para completar la configuración de los archivos binarios del instalador de Windows en el \_ sistema. Sin embargo, si se produce un reinicio en el paso (5), no se requieren pasos adicionales.

Instmsi.exe está disponible en los componentes del [SDK de Windows para desarrolladores Windows installer .](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arranque](bootstrapping.md)
</dt> <dt>

[Arranque de descarga de Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> </dl>

 

 




