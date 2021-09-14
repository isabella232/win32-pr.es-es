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
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161139"
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



## <a name="members"></a>Members

<dl> <dt>

**nEntries**
</dt> <dd>

Número de protocolos de la lista.

</dd> <dt>

**Entrada**
</dt> <dd>

Matriz de [estructuras \_ PF FOLLOWENTRY](pf-followentry.md) que describen cada protocolo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [estructura \_ PF PARSERINFO](pf-parserinfo.md) usa la estructura **PF \_ FOLLOWSET** para enumerar los protocolos que pueden preceder o seguir el protocolo que detecta el analizador.

Monitor de red usa la información de la estructura **\_ PF FOLLOWSET** para actualizar los siguientes conjuntos de analizadores específicos. La **estructura \_ PF FOLLOWSET** debe asignarse mediante **HeapAlloc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[PF \_ FOLLOWENTRY](pf-followentry.md)
</dt> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> </dl>

 

 




