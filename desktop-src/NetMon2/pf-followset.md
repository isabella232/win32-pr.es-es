---
description: La estructura \_ PF FOLLOWSET define los protocolos que pueden preceder o seguir un protocolo.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: PF_FOLLOWSET estructura (Netmon.h)
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
ms.openlocfilehash: d404e602e78452a38343a6e62fce8c5b16941270eaa2825de8339f583c064a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036835"
---
# <a name="pf_followset-structure"></a>Estructura \_ PF FOLLOWSET

La **estructura \_ PF FOLLOWSET** define los protocolos que pueden preceder o seguir un protocolo.

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

Matriz de [estructuras \_ PF FOLLOWENTRY](pf-followentry.md) que describen cada protocolo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [estructura \_ PF PARSERINFO](pf-parserinfo.md) usa la estructura **PF \_ FOLLOWSET** para enumerar los protocolos que pueden preceder o seguir el protocolo que el analizador detecta.

Monitor de red usa la información de la estructura **\_ PF FOLLOWSET** para actualizar los siguientes conjuntos de analizadores específicos. La **estructura \_ PF FOLLOWSET** debe asignarse mediante **HeapAlloc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ FOLLOWENTRY](pf-followentry.md)
</dt> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> </dl>

 

 




