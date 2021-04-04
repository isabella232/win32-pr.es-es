---
description: La \_ estructura DWORD con etiqueta define una etiqueta que se muestra cuando se detecta un valor de propiedad DWORD específico.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Estructura de LABELED_DWORD (Netmon. h)
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
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277977"
---
# <a name="labeled_dword-structure"></a>\_Estructura DWORD con etiqueta

La estructura **\_ DWORD con etiqueta** define una etiqueta que se muestra cuando se detecta un valor de propiedad DWORD específico.

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

Descripción o etiqueta textual que se muestra cuando se detecta el valor DWORD especificado en el miembro de **valor** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El miembro **lpLabeledDwordTable** de la estructura de [conjunto](set.md) apunta a una matriz de estructuras **set** que definen uno o más miembros de **etiqueta** de los pares de valores DWORD. Los pares se usan cuando se desea mostrar una etiqueta en lugar de un valor DWORD específico que se encuentra en el paquete del protocolo.

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

 

 




