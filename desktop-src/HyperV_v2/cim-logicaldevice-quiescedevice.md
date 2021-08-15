---
description: El método QuiesceDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Método QuiesceDevice de la CIM_LogicalDevice de datos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7becb86f19c245488d779e1b26ab5321ba3f2aa0ac3c7811d96f9d1cb8a5dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995697"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a>Método QuiesceDevice de la clase \_ LogicalDevice de CIM

El **método QuiesceDevice** ha quedado en desuso en lugar del método **RequestStateChange** más general que se superpone directamente con la funcionalidad proporcionada por este método.

## <a name="syntax"></a>Sintaxis


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Quiesce* \[ En\]
</dt> <dd>

Si se establece en **TRUE,** se suspende correctamente toda la actividad, si **FALSE** reanuda la actividad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_Dispositivo lógico CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




