---
title: Habilitación del sistema de archivos previsto de Windows
description: Describe cómo habilitar ProjFS en Windows
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: f903192190877631084e366bcaeafd8b5b0e7e72
ms.sourcegitcommit: 42cdae4d2eca84713ab3f7a5c88f583a352991a8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/23/2019
ms.locfileid: "105676086"
---
# <a name="enabling-windows-projected-file-system"></a><span data-ttu-id="6bf3d-103">Habilitación del sistema de archivos previsto de Windows</span><span class="sxs-lookup"><span data-stu-id="6bf3d-103">Enabling Windows Projected File System</span></span>

<span data-ttu-id="6bf3d-104">ProjFS se incluye con Windows como componente opcional.</span><span class="sxs-lookup"><span data-stu-id="6bf3d-104">ProjFS ships with Windows as an Optional Component.</span></span>  <span data-ttu-id="6bf3d-105">Para que un proveedor pueda utilizarlo, debe estar habilitado.</span><span class="sxs-lookup"><span data-stu-id="6bf3d-105">Before a provider can use it, it must be enabled.</span></span>  <span data-ttu-id="6bf3d-106">Puede usar</span><span class="sxs-lookup"><span data-stu-id="6bf3d-106">You can use</span></span> <!--the GUI or--> <span data-ttu-id="6bf3d-107">PowerShell para habilitar ProjFS.</span><span class="sxs-lookup"><span data-stu-id="6bf3d-107">PowerShell to enable ProjFS.</span></span>

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a><span data-ttu-id="6bf3d-108">Cómo habilitar ProjFS con PowerShell</span><span class="sxs-lookup"><span data-stu-id="6bf3d-108">How to enable ProjFS using PowerShell</span></span>

<span data-ttu-id="6bf3d-109">Para usar PowerShell para habilitar ProjFS, use el `Enable-WindowsOptionalFeature` cmdlet en una ventana de PowerShell con privilegios elevados:</span><span class="sxs-lookup"><span data-stu-id="6bf3d-109">To use PowerShell to enable ProjFS use the `Enable-WindowsOptionalFeature` cmdlet in an elevated PowerShell window:</span></span>

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

<span data-ttu-id="6bf3d-110">Reinicie el equipo si el Enable-WindowsOptionalFeature informes `RestartNeeded: True` .</span><span class="sxs-lookup"><span data-stu-id="6bf3d-110">Reboot the computer if the Enable-WindowsOptionalFeature reports `RestartNeeded: True`.</span></span>
