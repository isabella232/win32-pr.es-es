---
description: La estructura LABELED WORD define una etiqueta que se muestra cuando se detecta \_ un valor de propiedad WORD específico.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: LABELED_WORD estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169270"
---
# <a name="labeled_word-structure"></a>LABELED \_ WORD (estructura)

La **estructura LABELED \_ WORD** define una etiqueta que se muestra cuando se detecta un valor de propiedad WORD específico.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a>Members

<dl> <dt>

**Valor**
</dt> <dd>

Valor WORD de la propiedad que desea detectar.

</dd> <dt>

**Label**
</dt> <dd>

Descripción textual o etiqueta que se muestra cuando se detecta el valor WORD especificado en el **miembro Value.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **miembro lpLabeledWordTable** de la estructura [SET](set.md) apunta a una matriz de estructuras SET para definir uno o varios pares de valores de etiqueta. Estos pares se usan cuando se desea mostrar una etiqueta en lugar de un valor word específico que se encuentra en un paquete de protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




