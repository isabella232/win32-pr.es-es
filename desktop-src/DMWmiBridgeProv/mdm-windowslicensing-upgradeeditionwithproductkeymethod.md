---
title: Método UpgradeEditionWithProductKeyMethod de la clase MDM_WindowsLicensing
description: Especifica una clave de producto para una actualización de edición de dispositivos de escritorio de Windows 10. Vea también UpgradeEditionWithProductKey.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Método UpgradeEditionWithProductKeyMethod
- Método UpgradeEditionWithProductKeyMethod, clase MDM_WindowsLicensing
- Clase MDM_WindowsLicensing, método UpgradeEditionWithProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85824fc6fac9e5a15bf2bc890215afcbd0958680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491933"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Método UpgradeEditionWithProductKeyMethod de la \_ clase WindowsLicensing de MDM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Especifica una clave de producto para una actualización de edición de dispositivos de escritorio de Windows 10. Vea también [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Sintaxis


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*parámetro* \[ de\]
</dt> <dd>

La clave de producto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WindowsLicensing de MDM \_**](mdm-windowslicensing.md)
</dt> <dt>

[Usar scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

