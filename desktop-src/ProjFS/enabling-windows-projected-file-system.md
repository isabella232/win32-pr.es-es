---
title: Habilitar Windows sistema de archivos proyectado
description: Describe cómo habilitar ProjFS en Windows
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: ca891b9b7f89b3722ea9db1c606961d4ba47f0a1a1d05d1bebc2951c68e00f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031265"
---
# <a name="enabling-windows-projected-file-system"></a>Habilitar Windows sistema de archivos proyectado

ProjFS se incluye Windows como componente opcional.  Para que un proveedor pueda usarlo, debe estar habilitado.  Puede usar <!--the GUI or--> PowerShell para habilitar ProjFS.

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
