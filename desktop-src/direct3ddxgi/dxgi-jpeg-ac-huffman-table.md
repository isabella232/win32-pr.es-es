---
description: Describe una tabla de formato de CA JPEG.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: DXGI_JPEG_AC_HUFFMAN_TABLE estructura (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717717"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a>Estructura de tabla de gráfico de CA de DXGI \_ JPEG \_ \_ \_

Describe una tabla de formato de CA JPEG.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**CodeCounts**
</dt> <dd>

El número de códigos para cada longitud de código.

</dd> <dt>

**CodeValues**
</dt> <dd>

Valores de código de Huffman, en orden de aumento de la longitud del código.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




