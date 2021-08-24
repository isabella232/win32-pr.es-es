---
description: La estructura LABELED LARGEINT define una etiqueta que se muestra cuando se detecta un \_ valor de propiedad LARGEINT específico.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: LABELED_LARGEINT estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fab2942a2a5188527c57663af0c6000aa2cb628eaa2499eef054854df9187784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778775"
---
# <a name="labeled_largeint-structure"></a>LABELED \_ LARGEINT (estructura)

La **estructura LABELED \_ LARGEINT** define una etiqueta que se muestra cuando se detecta un valor de propiedad LARGEINT específico.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Valor**
</dt> <dd>

Valor LARGEINT de la propiedad que desea detectar.

</dd> <dt>

**Label**
</dt> <dd>

Descripción textual o etiqueta que se muestra cuando se detecta el valor LARGEINT especificado en el **miembro Value.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **miembro lpLabeledLargeIntTable** de la estructura [SET](set.md) apunta a una matriz de estructuras **SET** que definen uno o varios miembros **Label** de los pares de valores LARGEINT. Los pares se usan cuando se desea mostrar una etiqueta en lugar de un valor LARGEINT específico que se encuentra en un paquete de protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




