---
description: 'Puede usar los métodos siguientes para determinar la versión de Windows Installer:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Determinar la versión de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a48434fe415084a93158fb3445a36906d8b8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667805"
---
# <a name="determining-the-windows-installer-version"></a>Determinar la versión de Windows Installer

Puede usar los métodos siguientes para determinar la versión de Windows Installer:

-   Llame a la función [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) con el parámetro *szFilePath* establecido en la ruta de acceso al archivo Msi.dll.

    Puede llamar a la función [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) con la **constante \_ del sistema CSIDL** para obtener la ruta de acceso a Msi.dll. A partir de Windows Vista, las aplicaciones deben usar la función [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) y el **REFKNOWNFOLDERID** "System". Las aplicaciones existentes que usan la función **SHGetFolderPath** y el tipo **CSIDL** seguirán funcionando.

-   El valor de la propiedad [**Installer. version**](installer-version.md) del [**objeto Installer**](installer-object.md) es equivalente a las cadenas de cuatro campos enumeradas en las [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md) tema.
-   Las aplicaciones pueden obtener la versión de Windows Installer mediante [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).
-   El instalador establece la propiedad [**VersionMsi**](versionmsi.md) en la versión de Windows Installer que se ejecuta durante la instalación.

Para obtener más información, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

 

 
