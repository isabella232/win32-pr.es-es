---
title: Habilitar Windows de archivos proyectados
description: Describe cómo habilitar ProjFS en Windows
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: f903192190877631084e366bcaeafd8b5b0e7e72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473646"
---
# <a name="enabling-windows-projected-file-system"></a>Habilitar Windows de archivos proyectados

ProjFS se distribuye con Windows como componente opcional.  Para que un proveedor pueda usarlo, debe estar habilitado.  Puede usar <!--the GUI or--> PowerShell para habilitar ProjFS.

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a>Habilitación de ProjFS mediante PowerShell

Para usar PowerShell para habilitar ProjFS, use el `Enable-WindowsOptionalFeature` cmdlet en una ventana de PowerShell con privilegios elevados:

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

Reinicie el equipo si el Enable-WindowsOptionalFeature notifica `RestartNeeded: True` .
