---
description: Describe una tabla Huffman de DC JPEG.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: DXGI_JPEG_DC_HUFFMAN_TABLE estructura (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280293"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a>\_Estructura de \_ \_ tabla HUFFMAN de DC JPEG de DXGI \_

Describe una tabla Huffman de DC JPEG.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
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

 

 




