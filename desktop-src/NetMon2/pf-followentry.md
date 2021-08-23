---
description: La estructura PF \_ FOLLOWENTRY define un protocolo que Monitor de red agrega al siguiente conjunto de un analizador.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: PF_FOLLOWENTRY estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8fd7452a4db6318df0d4c23ea405d2cd4afcf6575c7abac34749a66bc88c2084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063735"
---
# <a name="pf_followentry-structure"></a>Estructura \_ PF FOLLOWENTRY

La **estructura PF \_ FOLLOWENTRY** define un protocolo que Monitor de red agrega al siguiente conjunto de un analizador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**szProtocol**
</dt> <dd>

El nombre del protocolo

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [estructura PF \_ FOLLOWSET](pf-followset.md) usa una matriz de **estructuras PF \_ FOLLOWENTRY.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[PF \_ FOLLOWSET](pf-followset.md)
</dt> </dl>

 

 




