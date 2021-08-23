---
description: 'Método LockMedia de la Msvm_DVDDrive : bloquea o libera el medio.'
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Método LockMedia de la Msvm_DVDDrive clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e86ef975d872f0fd86922f25f9752fda7508a037e293db85245ef6b1384a1570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525325"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a>Método LockMedia de la clase DVDDrive de Msvm \_

Bloquea o libera el medio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Bloqueo* \[ En\]
</dt> <dd>

**True para** bloquear el medio; **false** para liberar el medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes valores:

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> </dl>

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

[**Msvm \_ DVDDrive**](msvm-dvddrive.md)
</dt> </dl>

 

 




