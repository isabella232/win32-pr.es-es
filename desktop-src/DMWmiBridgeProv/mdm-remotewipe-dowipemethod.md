---
title: Método doWipeMethod de la MDM_RemoteWipe clase
description: Desencadena el dispositivo para iniciar el borrado remoto.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- Método doWipeMethod
- Método doWipeMethod, MDM_RemoteWipe clase
- MDM_RemoteWipe, método doWipeMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cff9cb831931c96fa8df1b376f96ea4c20b05bafdb12a85dec00b4f505af4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045645"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a>Método doWipeMethod de la clase \_ RemoteWipe mdm

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Desencadena el dispositivo para iniciar el borrado remoto. Consulte también [doWipe](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Sintaxis


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*param* \[ En\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | DMMap \\ de MDM \\ de CIMv2 \\ raíz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MDM \_ RemoteWipe**](mdm-remotewipe.md)
</dt> <dt>

[Uso de scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

