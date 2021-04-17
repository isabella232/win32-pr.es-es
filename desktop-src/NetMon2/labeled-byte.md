---
description: La estructura de \_ bytes con etiqueta define un par de bits con etiqueta. La etiqueta del par de bits con etiqueta se muestra cuando se detecta un valor de propiedad de byte específico.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Estructura de LABELED_BYTE (Netmon. h)
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
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652881"
---
# <a name="labeled_byte-structure"></a>Estructura de \_ bytes con etiqueta

La estructura de **\_ bytes con etiqueta** define un par de bits con etiqueta. La **etiqueta** del par de bits con etiqueta se muestra cuando se detecta un valor de propiedad de byte específico.

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

Valor de BYTE de la propiedad que desea detectar.

</dd> <dt>

**Label**
</dt> <dd>

Descripción o etiqueta textual que se muestra cuando se detecta el valor especificado en el miembro de **valor** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El miembro **lpLabeledByteTable** de la estructura de [conjunto](set.md) apunta a una matriz de estructuras **set** que definen uno o más miembros de **etiqueta** de los pares de valor de bytes. Estos pares se usan cuando se desea mostrar una etiqueta en lugar de un valor de BYTE específico que se encuentra en el paquete del protocolo.

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

 

 




