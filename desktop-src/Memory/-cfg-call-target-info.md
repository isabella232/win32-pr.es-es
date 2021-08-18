---
description: Representa información sobre los destinos de llamada para Control Flow Guard (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: CFG_CALL_TARGET_INFO estructura (Ntmmapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: e3bd7d351e890a968f2fa01ddffa6c8e3be16164d78393894055f55660c516bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040285"
---
# <a name="cfg_call_target_info-structure"></a>Estructura CFG \_ CALL \_ TARGET \_ INFO

Representa información sobre los destinos de llamada para Control Flow Guard (CFG).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Offset**
</dt> <dd>

Desplazamiento relativo a una dirección virtual proporcionada (inicio). Este desplazamiento debe tener una alineación de 16 bytes.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas que describen la operación que se va a realizar en la dirección. Si **se establece \_ CFG CALL TARGET \_ \_ VALID,** la dirección se marcará como válida para CFG. De lo contrario, se marcará como un destino de llamada no válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Ntmmapi.h</dt> </dl> |



 

 




