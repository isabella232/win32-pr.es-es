---
description: Describe una tabla de cuantificación JPEG.
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: DXGI_JPEG_QUANTIZATION_TABLE estructura (Dxgitype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: c94006c4a0508068fd3962dc9ec0979a92c33198b9db5f633cf71f50981b8f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909962"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a>Estructura DE \_ TABLA DE CUANTIFICACIÓN JPEG \_ \_ DE DXGI

Describe una tabla de cuantificación JPEG.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Elementos**
</dt> <dd>

Matriz de bytes que contiene los elementos de la tabla de cuantificación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dxgitype.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




