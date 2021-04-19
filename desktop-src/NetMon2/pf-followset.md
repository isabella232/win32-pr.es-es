---
description: La \_ estructura PF FOLLOWSET define los protocolos que pueden preceder o seguir un protocolo.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: Estructura de PF_FOLLOWSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678063"
---
# <a name="pf_followset-structure"></a>\_Estructura PF FOLLOWSET

La estructura **PF \_ FOLLOWSET** define los protocolos que pueden preceder o seguir un protocolo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nEntries**
</dt> <dd>

Número de protocolos de la lista.

</dd> <dt>

**Entrada**
</dt> <dd>

Matriz de estructuras [PF \_ FOLLOWENTRY](pf-followentry.md) que describen cada protocolo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura [PF \_ PARSERINFO](pf-parserinfo.md) utiliza la estructura **PF \_ FOLLOWSET** para enumerar los protocolos que pueden preceder o seguir el protocolo que detecta el analizador.

Monitor de red usa la información de la estructura **PF \_ FOLLOWSET** para actualizar los siguientes conjuntos de analizadores específicos. La estructura **PF \_ FOLLOWSET** debe estar asignada mediante **HeapAlloc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ FOLLOWENTRY](pf-followentry.md)
</dt> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> </dl>

 

 




