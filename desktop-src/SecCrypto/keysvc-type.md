---
description: La enumeración KEYSVC \_ TYPE define si una clave se aplica a un equipo o a un servicio.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: KEYSVC_TYPE enumeración (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3c23cc259029cf76fcb1590e6261623827d59b48c9a0728e21c8250ca3e858f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976105"
---
# <a name="keysvc_type-enumeration"></a>Enumeración KEYSVC \_ TYPE

La **enumeración KEYSVC \_ TYPE** define si una clave se aplica a un equipo o a un servicio.

## <a name="syntax"></a>Syntax


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**
</dt> <dd>

La clave es para un equipo.

</dd> <dt>

<span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**
</dt> <dd>

La clave es para un servicio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




