---
description: La \_ estructura LARGEINT con etiqueta define una etiqueta que se muestra cuando se detecta un valor de propiedad LARGEINT específico.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Estructura de LABELED_LARGEINT (Netmon. h)
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
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082715"
---
# <a name="labeled_largeint-structure"></a>\_Estructura LARGEINT con etiqueta

La estructura **\_ LARGEINT con etiqueta** define una etiqueta que se muestra cuando se detecta un valor de propiedad LARGEINT específico.

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

Valor de LARGEINT de la propiedad que desea detectar.

</dd> <dt>

**Label**
</dt> <dd>

Descripción o etiqueta textual que se muestra cuando se detecta el valor de LARGEINT especificado en el miembro de **valor** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El miembro **lpLabeledLargeIntTable** de la estructura de [conjunto](set.md) apunta a una matriz de estructuras **set** que definen uno o más miembros de **etiqueta** de los pares de valores LARGEINT. Los pares se usan cuando se desea mostrar una etiqueta en lugar de un valor de LARGEINT específico que se encuentra en un paquete de protocolo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




