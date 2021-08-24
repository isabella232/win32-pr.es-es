---
description: 'Puede usar los métodos siguientes para determinar la versión Windows instalador:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Determinar la versión Windows instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e13907790585356fa4a5bc8376fe87f30793e0e3af71e1b0c113f30cf04b8f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764225"
---
# <a name="determining-the-windows-installer-version"></a>Determinar la versión Windows instalador

Puede usar los métodos siguientes para determinar la versión Windows instalador:

-   Llame a [**la función MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) con el *parámetro szFilePath* establecido en la ruta de acceso al archivo Msi.dll.

    Puede llamar a la [**función SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) con la constante **SYSTEM de CSIDL \_** para obtener la ruta de acceso a Msi.dll. A partir Windows Vista, las aplicaciones deben usar la [**función SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) y **refKNOWNFOLDERID** "System". Las aplicaciones existentes que **usan la función SHGetFolderPath** y el **tipo CSIDL** seguirán funcionando.

-   El valor de la propiedad [**Installer.Version**](installer-version.md) del objeto [**Installer**](installer-object.md) es equivalente a las cadenas de cuatro campos enumeradas en el tema Versiones publicadas [de Windows Installer.](released-versions-of-windows-installer.md)
-   Las aplicaciones pueden obtener la Windows del instalador mediante [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).
-   El instalador establece la [**propiedad VersionMsi**](versionmsi.md) en la versión de Windows Installer que se ejecuta durante la instalación.

Para obtener más información, vea [Versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

 

 
