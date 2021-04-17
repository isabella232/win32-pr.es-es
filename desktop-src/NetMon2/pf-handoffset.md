---
description: La \_ estructura PF HANDOFFSET define los protocolos que se entregan al analizador, o los protocolos a los que se entrega el analizador.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: Estructura de PF_HANDOFFSET (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667935"
---
# <a name="pf_handoffset-structure"></a>\_Estructura PF HANDOFFSET

La estructura **PF \_ HANDOFFSET** define los protocolos que se entregan al analizador, o los protocolos a los que se entrega el analizador.

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

Una matriz de estructuras [PF \_ HANDOFFENTRY](pf-handoffentry.md) que definen cada protocolo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura [PF \_ PARSERINFO](pf-parserinfo.md) utiliza la estructura **PF \_ HANDOFFSET** para enumerar lo siguiente:

-   Los protocolos que se entregan al analizador.
-   A qué protocolos se entrega el analizador.

La estructura **PF \_ HANDOFFSET** debe estar asignada mediante **HeapAlloc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[PF \_ HANDOFFENTRY](pf-handoffentry.md)
</dt> </dl>

 

 




