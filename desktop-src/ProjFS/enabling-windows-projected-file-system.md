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
# <a name="enabling-windows-projected-file-system"></a>Habilitación del sistema de archivos previsto de Windows

ProjFS se incluye con Windows como componente opcional.  Para que un proveedor pueda utilizarlo, debe estar habilitado.  Puede usar <!--the GUI or--> PowerShell para habilitar ProjFS.

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a>Cómo habilitar ProjFS con PowerShell

Para usar PowerShell para habilitar ProjFS, use el `Enable-WindowsOptionalFeature` cmdlet en una ventana de PowerShell con privilegios elevados:

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

Reinicie el equipo si el Enable-WindowsOptionalFeature informes `RestartNeeded: True` .
