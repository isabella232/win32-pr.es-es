---
description: 'Método LockMedia de la Msvm_DisketteDrive : bloquea o libera el medio.'
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Método LockMedia de la Msvm_DisketteDrive clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5f5f87354aa7c39534e8b32c8985c5d18b55caa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111983"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a>Método LockMedia de la clase \_ DisketteDrive de Msvm

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

**true** para bloquear el medio; **false** para liberar el medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve uno de los valores siguientes:

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> </dl>

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

[**DisketteDrive de Msvm \_**](msvm-diskettedrive.md)
</dt> </dl>

 

 




