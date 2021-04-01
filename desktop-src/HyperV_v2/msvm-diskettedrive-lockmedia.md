---
description: Bloquea o libera los medios.
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Método LockMedia de la clase Msvm_DisketteDrive
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
ms.openlocfilehash: 4f9bce4e9e46d76c3426271af16c28026c242fa9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914150"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a>Método LockMedia de la \_ clase DisketteDrive de MSVM

Bloquea o libera los medios.

## <a name="syntax"></a>Sintaxis


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Bloquear* \[ de\]
</dt> <dd>

**true** para bloquear el medio; **false** para liberar el medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve uno de los valores siguientes:

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ DisketteDrive**](msvm-diskettedrive.md)
</dt> </dl>

 

 




