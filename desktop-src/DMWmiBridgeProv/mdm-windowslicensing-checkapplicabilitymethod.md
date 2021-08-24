---
title: Método CheckApplicabilityMethod de la MDM_WindowsLicensing clase
description: Comprueba si la clave de producto especificada se puede usar para una actualización de edición, activación o cambio de una clave de producto Windows 10 dispositivos de escritorio. Consulte también CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Método CheckApplicabilityMethod
- Método CheckApplicabilityMethod, MDM_WindowsLicensing clase
- MDM_WindowsLicensing clase, método CheckApplicabilityMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db236e05ffe7b5b6273e7cba594266c31720932b43a7df2de751a0fa66cced5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750155"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>Método CheckApplicabilityMethod de la clase \_ WindowsLicensing de MDM

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Comprueba si la clave de producto especificada se puede usar para una actualización de edición, activación o cambio de una clave de producto Windows 10 dispositivos de escritorio. Consulte también [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Sintaxis


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*param* \[ En\]
</dt> <dd>

Clave de producto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

TRUE o FALSE

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

 

