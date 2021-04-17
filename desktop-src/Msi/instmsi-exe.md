---
description: Instmsi.exe es el paquete redistribuible para instalar Windows Installer&\# 160; 2.0 y versiones anteriores de Windows Installer. Consulte Windows Installer redistribuibles de los redistribuibles para Windows Installer&\# 160; 3.0 y versiones posteriores.
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 229d748cda68731627a6af2af992e321755b5ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688330"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe es el paquete redistribuible para instalar Windows Installer 2,0 y versiones anteriores de Windows Installer. Consulte [Windows Installer redistribuibles](windows-installer-redistributables.md) de los redistribuibles para Windows Installer 3,0 y versiones posteriores.

Para obtener más información acerca de la versión de Windows Installer que se incluye con el sistema operativo, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

Algunos redistribuibles no deben ejecutarse en determinadas versiones del sistema operativo. En la tabla siguiente se describe qué Instmsi es compatible con qué sistema operativo.



| Si Instmsi.exe instala esta versión del Windows Installer | Instmsi.exe se pueden ejecutar en estos sistemas operativos                    | Instmsi.exe no se deben ejecutar en estos sistemas operativos                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows Installer versión 1,0                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installer versión 1,1                                 | Windows 95, Windows 98, Windows NT 4.0 + SP3                           | Windows me, Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008 |
| Windows Installer versión 1,2                                 | Windows 95, Windows 98, Windows me, Windows NT 4.0 + SP3               | Windows 2000, Windows XP, Windows Server 2003, Windows Vista y Windows Server 2008             |
| Windows Installer versión 2,0                                 | Windows 95, Windows 98, Windows me, Windows NT 4.0 + SP6, Windows 2000 | Windows XP, Windows Server 2003, Windows Vista y Windows Server 2008                           |



 

Por ejemplo, una aplicación que redistribuye Windows Installer versión 1,1 debe comprobar que el sistema operativo es Windows NT 4,0 SP3 o Windows 98/95 antes de ejecutar el paquete redistribuible. Las aplicaciones que usan el paquete redistribuible también deben asegurarse de que la versión ANSI del Windows Installer esté instalada en Windows 98/95 y que la versión de Unicode esté instalada en Windows NT o Windows 2000. Tenga en cuenta que algunas aplicaciones cambia el nombre de la versión Unicode a InstMsiW.

## <a name="syntax"></a>Sintaxis

 *Opciones* de Instmsi

## <a name="command-line-options"></a>Opciones de la línea de comandos

Las opciones de la línea de comandos no distinguen mayúsculas de minúsculas.



| Opción                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | Lo usan las aplicaciones que redistribuyen el Windows Installer como parte de una aplicación de arranque. No se muestra ninguna interfaz de usuario al usuario. La aplicación de arranque debe comprobar el código de retorno para determinar si es necesario reiniciar para completar la instalación del Windows Installer.                                                                                                                                                                                                                          |
| /t                         | Se usa solo con fines de depuración.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c: "msiinst/delayreboot"  | Opción de reinicio retrasado. Impide que Instmsi solicite al usuario un reinicio aunque tuviera que reemplazar los archivos que estaban en uso durante la instalación. Si se invoca Instmsi con esta opción, devolverá un ERROR de \_ \_ reinicio correcto \_ necesario si tuviera que reemplazar los archivos que estaban en uso. Si no tuviera que reemplazar los archivos que estaban en uso, devolverá el ERROR \_ Success. Disponible con Instmsi para Windows Installer 2,0 o posterior. Vea la sección Comentarios para obtener información adicional sobre los reinicios retrasados.<br/> |
| /c: "msiinst/delayrebootq" | Versión silenciosa de la opción de reinicio retrasado. No presenta ninguna interfaz de usuario para el usuario. De lo contrario, el comportamiento es idéntico al de la opción anterior. Disponible con Instmsi para Windows Installer 2,0 o posterior. Vea la sección Comentarios para obtener información adicional sobre los reinicios retrasados.<br/>                                                                                                                                                                                                                           |
| /?                         | Muestra información de ayuda.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

Las aplicaciones de [arranque](bootstrapping.md) que usan Instmsi.exe para instalar el Windows Installer con otra aplicación pueden requerir un reinicio adicional del sistema. Es posible que se reinicie Adicionalmente además de los reinicios necesarios para instalar la aplicación.

La opción retardo de reinicio solo se recomienda para los programadores de instalación que deseen eliminar un reinicio adicional debido al uso de Instmsi.exe con una aplicación de instalación que instala los archivos que están en uso.

Los desarrolladores deben hacer lo siguiente en su aplicación de instalación para utilizar la opción de reinicio retrasado. Esta opción no está disponible con Instmsi.exe versiones que instalan versiones de Windows Installer anteriores a la versión 2,0:

**Para utilizar la opción de reinicio retrasado**

1.  Llame a Instmsi.exe con una de las opciones de línea de comandos de reinicio retrasado.
2.  Trate el resultado de que se \_ REinicien los errores correctos o correctos \_ \_ con éxito \_ , como lo que significa que es correcto.
3.  Obtenga la ruta de acceso a la carpeta que contiene los archivos binarios de Windows Installer recién instalados del valor InstallerLocation en:

    **HKEY \_ Software de \_ equipo local** \\  \\  \\  \\  \\ **instalador** de CurrentVersion de Microsoft Windows

    Este valor es de tipo **reg \_ SZ**.

4.  Establezca el directorio actual en la ruta de acceso obtenida en el paso 3.
5.  Invoque msiexec en el paquete de la aplicación y ejecute otro código de instalación específico de la aplicación. Si la aplicación de instalación usa [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), la aplicación debe cargar MSI.DLL desde la ubicación obtenida en el paso 3.
    > [!Note]  
    > Las aplicaciones que llaman a **LoadLibrary** en el nuevo MSI.DLL en la ubicación obtenida en el paso 3 deben asegurarse de que no se haya cargado todavía una versión anterior de MSI.DLL en el proceso. Si se cargó una versión anterior de MSI.DLL dentro del proceso, se debe descargar del espacio de direcciones de proceso antes de la llamada **LoadLibrary** para el nuevo MSI.DLL.

     

6.  Si el paso (5) no requiere un reinicio y si Instmsi.exe ha devuelto \_ el \_ reinicio \_ de error correcto necesario en el paso (1), pida al usuario que reinicie el equipo para completar la instalación de los archivos binarios de Windows Installer en el sistema. Sin embargo, si se produce un reinicio en el paso (5), no se requiere ningún paso adicional.

Instmsi.exe está disponible en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arranque](bootstrapping.md)
</dt> <dt>

[Arranque de descarga de Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> </dl>

 

 




