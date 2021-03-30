---
description: La \_ estructura PF FOLLOWENTRY define un protocolo que monitor de red agrega al siguiente conjunto de un analizador.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Estructura de PF_FOLLOWENTRY (Netmon. h)
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
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910881"
---
# <a name="pf_followentry-structure"></a>\_Estructura PF FOLLOWENTRY

La estructura **PF \_ FOLLOWENTRY** define un protocolo que monitor de red agrega al siguiente conjunto de un analizador.

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

## <a name="remarks"></a>Observaciones

La estructura [PF \_ FOLLOWSET](pf-followset.md) usa una matriz de estructuras **PF \_ FOLLOWENTRY** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ FOLLOWSET](pf-followset.md)
</dt> </dl>

 

 




