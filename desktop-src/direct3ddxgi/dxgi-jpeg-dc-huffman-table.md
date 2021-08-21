---
description: Describe una tabla JPEG DC huffman.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: DXGI_JPEG_DC_HUFFMAN_TABLE estructura (Dxgitype.h)
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
ms.openlocfilehash: b431bbccb66bcb24e068229493ef87f2ac96736161bb306609ac4dd479dfb7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987125"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a>Estructura DE \_ TABLA \_ \_ HUFFMAN DE DC DE \_ DXGI JPEG

Describe una tabla JPEG DC huffman.

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

Número de códigos para cada longitud de código.

</dd> <dt>

**CodeValues**
</dt> <dd>

Los valores de código de Huffman, en orden de aumentar la longitud del código.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dxgitype.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




