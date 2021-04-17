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
# <a name="determining-the-windows-installer-version"></a><span data-ttu-id="16780-103">Determinar la versión de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="16780-103">Determining the Windows Installer Version</span></span>

<span data-ttu-id="16780-104">Puede usar los métodos siguientes para determinar la versión de Windows Installer:</span><span class="sxs-lookup"><span data-stu-id="16780-104">You can use the following methods to determine the Windows Installer version:</span></span>

-   <span data-ttu-id="16780-105">Llame a la función [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) con el parámetro *szFilePath* establecido en la ruta de acceso al archivo Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="16780-105">Call the [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) function with the *szFilePath* parameter set to the path to the file Msi.dll.</span></span>

    <span data-ttu-id="16780-106">Puede llamar a la función [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) con la **constante \_ del sistema CSIDL** para obtener la ruta de acceso a Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="16780-106">You can call the [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function with the **CSIDL\_SYSTEM** constant to get the path to Msi.dll.</span></span> <span data-ttu-id="16780-107">A partir de Windows Vista, las aplicaciones deben usar la función [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) y el **REFKNOWNFOLDERID** "System".</span><span class="sxs-lookup"><span data-stu-id="16780-107">Beginning with Windows Vista, applications should use the [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) function and the **REFKNOWNFOLDERID** "System."</span></span> <span data-ttu-id="16780-108">Las aplicaciones existentes que usan la función **SHGetFolderPath** y el tipo **CSIDL** seguirán funcionando.</span><span class="sxs-lookup"><span data-stu-id="16780-108">Existing applications that use the **SHGetFolderPath** function and the **CSIDL** type will continue to work.</span></span>

-   <span data-ttu-id="16780-109">El valor de la propiedad [**Installer. version**](installer-version.md) del [**objeto Installer**](installer-object.md) es equivalente a las cadenas de cuatro campos enumeradas en las [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md) tema.</span><span class="sxs-lookup"><span data-stu-id="16780-109">The value of the [**Installer.Version**](installer-version.md) property of the [**Installer Object**](installer-object.md) is equivalent to the four-field strings listed in the [Released Versions of Windows Installer](released-versions-of-windows-installer.md) topic.</span></span>
-   <span data-ttu-id="16780-110">Las aplicaciones pueden obtener la versión de Windows Installer mediante [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="16780-110">Applications can get the Windows Installer version by using [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span></span>
-   <span data-ttu-id="16780-111">El instalador establece la propiedad [**VersionMsi**](versionmsi.md) en la versión de Windows Installer que se ejecuta durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="16780-111">The installer sets the [**VersionMsi**](versionmsi.md) property to the version of Windows Installer that is run during the installation.</span></span>

<span data-ttu-id="16780-112">Para obtener más información, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="16780-112">For more information, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

 

 
