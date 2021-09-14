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
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159905"
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



## <a name="members"></a>Members

<dl> <dt>

**Offset**
</dt> <dd>

Desplazamiento con respecto a una dirección virtual proporcionada (inicio). Este desplazamiento debe tener una alineación de 16 bytes.

</dd> <dt>

**Marcas**
</dt> <dd>

Marcas que describen la operación que se va a realizar en la dirección. Si **se establece CFG CALL TARGET \_ \_ \_ VALID,** la dirección se marcará como válida para CFG. De lo contrario, se marcará como un destino de llamada no válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Ntmmapi.h</dt> </dl> |



 

 




