---
description: La \_ estructura SYSTEMTIME con etiqueta define una etiqueta que se muestra cuando se detecta un valor de propiedad SYSTEMTIME específico.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Estructura de LABELED_SYSTEMTIME (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913445"
---
# <a name="labeled_systemtime-structure"></a>\_Estructura SYSTEMTIME con etiqueta

La estructura **\_ SYSTEMTIME con etiqueta** define una etiqueta que se muestra cuando se detecta un valor de propiedad SYSTEMTIME específico.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Valor**
</dt> <dd>

Valor SYSTEMTIME de una propiedad que desea detectar.

</dd> <dt>

**Label**
</dt> <dd>

Descripción o etiqueta textual que se muestra cuando se detecta el valor SYSTEMTIME especificado en el miembro de **valor** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El miembro **lpLabeledSystemTimeTable** de la estructura de [conjunto](set.md) apunta a una matriz de estructuras **set** que definen uno o varios pares de valores de etiqueta. Los pares se usan cuando se desea mostrar una etiqueta en lugar de un valor de LARGEINT específico que se encuentra en el paquete del protocolo.

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

 

 




