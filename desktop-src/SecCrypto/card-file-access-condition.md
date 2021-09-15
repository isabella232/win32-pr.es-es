---
description: Especifica los permisos de control de acceso para un archivo en una tarjeta inteligente.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: CARD_FILE_ACCESS_CONDITION enumeración (Cardmod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476510"
---
# <a name="card_file_access_condition-enumeration"></a>Enumeración CARD \_ FILE \_ ACCESS \_ CONDITION

La **\_ enumeración CARD FILE \_ ACCESS \_ CONDITION** especifica los permisos de control de acceso para un archivo en una [*tarjeta inteligente.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Este valor no es válido.

</dd> <dt>

<span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**
</dt> <dd>

Todos pueden leer el archivo. Los usuarios específicos pueden escribir en el archivo.

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**
</dt> <dd>

Solo determinados usuarios pueden leer o escribir en el archivo.

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**
</dt> <dd>

Todos pueden leer el archivo. Los administradores pueden escribir en el archivo.

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**
</dt> <dd>

Se desconocen los permisos de acceso para el archivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows xp \[ solo aplicaciones de escritorio\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 Windows Server 2003 \[\]<br/>            |
| Encabezado<br/>                   | <dl> <dt>Cardmod.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Proveedor de servicios criptográficos de tarjeta inteligente base de Microsoft](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**INFORMACIÓN DEL \_ ARCHIVO DE \_ TARJETA**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**CardCreateFile**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
