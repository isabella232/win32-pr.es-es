---
description: La estructura LABELED \_ BYTE define un par BIT etiquetado. La etiqueta del par BIT etiquetado se muestra cuando se detecta un valor de propiedad de byte específico.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: LABELED_BYTE estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 05aa29942768c0c40816eafce112f12a95cd0a713bebe612d2e5ad32776a33a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494985"
---
# <a name="labeled_byte-structure"></a>Estructura \_ BYTE ETIQUETADA

La **estructura LABELED \_ BYTE** define un par BIT etiquetado. La **etiqueta** del par BIT etiquetado se muestra cuando se detecta un valor de propiedad de byte específico.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Valor**
</dt> <dd>

Valor BYTE de la propiedad que desea detectar.

</dd> <dt>

**Label**
</dt> <dd>

Descripción textual o etiqueta que se muestra cuando se detecta el valor especificado en el **miembro Value.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **miembro lpLabeledByteTable** de la estructura [SET](set.md) apunta a una matriz de estructuras **SET** que definen uno o varios miembros **Label** de los pares de valores BYTE. Estos pares se usan cuando se desea mostrar una etiqueta en lugar de un valor BYTE específico que se encuentra en el paquete de protocolo.

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

 

 




