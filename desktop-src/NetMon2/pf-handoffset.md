---
description: La estructura PF HANDOFFSET define los protocolos que se entregan al analizador o los protocolos a los que entrega \_ el analizador.
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
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074098"
---
# <a name="pf_handoffset-structure"></a>Estructura \_ HANDOFFSET PF

La **\_ estructura PF HANDOFFSET** define los protocolos que se entregan al analizador o los protocolos a los que entrega el analizador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a>Members

<dl> <dt>

**nEntries**
</dt> <dd>

Número de protocolos.

</dd> <dt>

**Entrada**
</dt> <dd>

Matriz de [estructuras \_ PF HANDOFFENTRY](pf-handoffentry.md) que definen cada protocolo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[PF \_ HANDOFFENTRY](pf-handoffentry.md)
</dt> </dl>

 

 




