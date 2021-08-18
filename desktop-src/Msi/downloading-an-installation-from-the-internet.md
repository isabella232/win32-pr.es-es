---
description: Windows El instalador acepta un localizador uniforme de recursos (URL) como origen válido para una instalación.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Descarga de una instalación desde Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5195b0ec0e5c36e7b6866232c498c02a9f4022d207cd86cc229a49ec5a5e8bac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637772"
---
# <a name="downloading-an-installation-from-the-internet"></a>Descarga de una instalación desde Internet

Windows El instalador acepta un localizador uniforme de recursos (URL) como origen válido para una instalación. Windows El instalador puede instalar paquetes, revisiones y transformaciones desde una ubicación de dirección URL.

Si la base de datos de instalación se encuentra en una dirección URL, el instalador descarga la base de datos en una ubicación de caché antes de iniciar la instalación. El instalador también descarga los archivos y archivos archivadores del origen de Internet que son adecuados para las selecciones del usuario. Consulte [A URL-based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md) (Ejemplo de instalación del instalador de archivos basado en url) para obtener más información.

Por ejemplo, para instalar un paquete con un origen ubicado en un servidor web en , puede usar las opciones de línea de comandos para instalar el paquete y establecer https://server/share/package.msi [propiedades](public-properties.md) públicas. [](command-line-options.md)

msiexec /i https://server/share/package.msi *PROPERTY=VALUE*

Una línea de comandos como la mostrada anteriormente debe pasarse al instalador para iniciar una instalación desde un explorador web. En general, no debe descargar e instalar el paquete simplemente haciendo doble clic en el archivo .msi desde el explorador. Esto descarga el archivo .msi en la carpeta de archivos temporales de Internet y pasa el siguiente comando al instalador:

**msiexec /i c: \\ archivos temporales de Internet de Windows \\ \\package.msi**

Se produce un error en la instalación si el paquete requiere archivos o archivadores de código fuente externos porque no se encuentran en la misma ubicación que el .msi archivo.

Tenga en cuenta que, dado que el objeto [**Installer**](installer-object.md) no está marcado como [SafeForScripting](safeforscripting.md) en el equipo del usuario, los usuarios deben ajustar la configuración de seguridad del explorador para que el ejemplo funcione correctamente.

El [**método InstallProduct**](installer-installproduct.md) se podría usar para ejecutar el comando anterior desde un explorador como un evento al hacer clic.


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



Tenga en cuenta que, dado que algunos servidores [](file-table.md) web distinguen mayúsculas de minúsculas, el campo FileName de la tabla File debe coincidir exactamente con el caso de los archivos de origen para garantizar la compatibilidad con las descargas de Internet.

Consulte [Descarga e instalación de una revisión desde Internet.](downloading-and-installing-a-patch-from-the-internet.md) Para obtener más información sobre la protección de instalaciones y el uso de certificados digitales, vea [Directrices](guidelines-for-authoring-secure-installations.md) para crear instalaciones seguras y firmas [digitales y Windows Installer](digital-signatures-and-windows-installer.md). Para obtener más información sobre cómo crear una instalación web de un paquete Windows Installer, vea [Arranque de descarga de Internet.](internet-download-bootstrapping.md)

## <a name="available-internet-protocols"></a>Protocolos de Internet disponibles

A partir Windows Server 2003 y Windows XP, el instalador puede usar los protocolos HTTP, HTTPS y FILE. El instalador no admite los protocolos FTP y GOPHER.

Windows La versión 2.0 del instalador puede usar los protocolos HTTP, FILE y FTP y no puede usar los protocolos HTTPS y GOPHER.

 

 



