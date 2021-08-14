---
description: La estructura LABELED DWORD define una etiqueta que se muestra cuando se detecta un valor de propiedad \_ DWORD específico.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: LABELED_DWORD estructura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 10f3e0dd09b37821a00f2c10f99c0ea6d509ff388e9d7394a8b2c4958438f979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364850"
---
# <a name="labeled_dword-structure"></a>Estructura \_ DWORD ETIQUETADA

La **estructura LABELED \_ DWORD** define una etiqueta que se muestra cuando se detecta un valor de propiedad DWORD específico.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Valor**
</dt> <dd>

Valor DWORD de la propiedad que desea detectar.

</dd> <dt>

**Label**
</dt> <dd>

Descripción textual o etiqueta que se muestra cuando se detecta el valor DWORD especificado en el **miembro Value.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **miembro lpLabeledDwordTable** de la estructura [SET](set.md) apunta a una matriz de estructuras **SET** que definen uno o varios miembros **Label** de los pares de valores DWORD. Los pares se usan cuando se desea mostrar una etiqueta en lugar de un valor DWORD específico que se encuentra en el paquete de protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




