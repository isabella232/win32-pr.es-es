---
description: Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido para una instalación de.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Descarga de una instalación desde Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652535"
---
# <a name="downloading-an-installation-from-the-internet"></a>Descarga de una instalación desde Internet

Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido para una instalación de. Windows Installer puede instalar paquetes, revisiones y transformaciones desde una ubicación de dirección URL.

Si la base de datos de instalación se encuentra en una dirección URL, el instalador descarga la base de datos en una ubicación de caché antes de iniciar la instalación. El instalador también descarga los archivos y archivos. cab desde el origen de Internet que son adecuados para las selecciones del usuario. Vea [un ejemplo de instalación de Windows Installer basado en URL](a-url-based-windows-installer-installation-example.md) para obtener más información.

Por ejemplo, para instalar un paquete con un origen ubicado en un servidor Web en https://server/share/package.msi , puede utilizar las opciones de [línea de comandos](command-line-options.md) para instalar el paquete y establecer las propiedades [públicas](public-properties.md) .

msiexec/i https://server/share/package.msi *Property = valor*

Se debe pasar al instalador una línea de comandos como la que se mostró anteriormente para iniciar una instalación desde un explorador Web. En general, no debe descargar e instalar el paquete simplemente haciendo doble clic en el archivo. msi desde el explorador. Esto descarga el archivo. msi en la carpeta de archivos temporales de Internet y pasa el siguiente comando al instalador:

**msiexec/i c: \\ \\ archivos temporales de Internet de Windows \\package.msi**

Se produce un error en la instalación si el paquete requiere archivos de origen o archivadores externos, ya que no se encuentran en la misma ubicación que el archivo. msi.

Tenga en cuenta que, como el objeto de [**instalador**](installer-object.md) no está marcado como [SafeForScripting](safeforscripting.md) en el equipo del usuario, los usuarios deben ajustar la configuración de seguridad del explorador para que el ejemplo funcione correctamente.

El método [**InstallProduct**](installer-installproduct.md) se puede usar para ejecutar el comando anterior desde un explorador como un evento de clic.


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



Tenga en cuenta que, dado que algunos servidores web distinguen mayúsculas de minúsculas, el campo Nombre de archivo de la tabla de [archivos](file-table.md) debe coincidir exactamente con las mayúsculas y minúsculas de los archivos de origen para garantizar la compatibilidad con las descargas

Vea [Descargar e instalar una revisión desde Internet](downloading-and-installing-a-patch-from-the-internet.md). Para obtener más información acerca de la protección de instalaciones y el uso de certificados digitales, consulte las [instrucciones para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md) y [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md). Para obtener más información sobre cómo crear una instalación Web de un paquete de Windows Installer, vea [arranque de descarga en Internet](internet-download-bootstrapping.md).

## <a name="available-internet-protocols"></a>Protocolos de Internet disponibles

A partir de Windows Server 2003 y Windows XP, el instalador puede usar los protocolos HTTP, HTTPS y FILE. El instalador no admite los protocolos FTP y GOPHER.

Windows Installer versión 2,0 puede usar los protocolos HTTP, archivo y FTP y no puede usar los protocolos HTTPS y GOPHER.

 

 



