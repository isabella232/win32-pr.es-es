---
title: Método UpgradeEditionWithProductKeyMethod de la MDM_WindowsLicensing clase
description: Especifica una clave de producto para una actualización de edición de Windows 10 dispositivos de escritorio. Consulte también UpgradeEditionWithProductKey.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Método UpgradeEditionWithProductKeyMethod
- Método UpgradeEditionWithProductKeyMethod, MDM_WindowsLicensing clase
- MDM_WindowsLicensing clase, método UpgradeEditionWithProductKeyMethod
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
ms.openlocfilehash: a44293701c5a18f20b7e286530446c662778999f3ffa5ed8edffb5819dda8a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913245"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Método UpgradeEditionWithProductKeyMethod de la clase \_ WindowsLicensing mdm

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Especifica una clave de producto para una actualización de edición de Windows 10 dispositivos de escritorio. Vea también [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Sintaxis


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*param* \[ En\]
</dt> <dd>

Clave de producto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MDM \_ WindowsLicensing**](mdm-windowslicensing.md)
</dt> <dt>

[Uso de scripts de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

