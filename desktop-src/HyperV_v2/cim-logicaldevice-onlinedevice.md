---
description: El método OnlineDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Método OnlineDevice de la CIM_LogicalDevice clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f34d08ad72bd04cd94e35ac229fde82ca4847ec13410e35d57d0de0778d50af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695515"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a>Método OnlineDevice de la clase \_ LogicalDevice de CIM

El **método OnlineDevice** ha quedado en desuso en lugar del método **RequestStateChange** más general que se superpone directamente con la funcionalidad proporcionada por este método.

## <a name="syntax"></a>Sintaxis


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*En línea* \[ En\]
</dt> <dd>

Si **es TRUE,** haga que el dispositivo se en línea, **si es FALSE,** des línea el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Dispositivo lógico CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




