---
description: La estructura HANDOFFSET PF define los protocolos que se entregan al analizador o los protocolos a los que el analizador \_ entrega.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: PF_HANDOFFSET estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 68e3f3608ac1aeff0f6d54ee7c94c39b76b0df08bb7dc41b05063f9cf53c48a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036845"
---
# <a name="pf_handoffset-structure"></a>Estructura \_ HANDOFFSET PF

La **estructura \_ HANDOFFSET** PF define los protocolos que se entregan al analizador o los protocolos a los que el analizador entrega.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nEntries**
</dt> <dd>

Número de protocolos.

</dd> <dt>

**Entrada**
</dt> <dd>

Matriz de [estructuras \_ PF HANDOFFENTRY](pf-handoffentry.md) que definen cada protocolo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [estructura \_ PF PARSERINFO](pf-parserinfo.md) usa la **estructura PF \_ HANDOFFSET** para enumerar lo siguiente:

-   Qué protocolos se entregan al analizador.
-   Protocolos a los que se entrega el analizador.

La **estructura \_ PF HANDOFFSET** debe asignarse mediante **HeapAlloc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[PF \_ HANDOFFENTRY](pf-handoffentry.md)
</dt> </dl>

 

 




