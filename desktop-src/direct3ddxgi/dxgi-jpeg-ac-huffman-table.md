---
description: Describe una tabla JPEG AC huffman.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: DXGI_JPEG_AC_HUFFMAN_TABLE estructura (Dxgitype.h)
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
ms.openlocfilehash: 21e279e4974d221a6feba6f135343d122f30f3da1edb18210e0e14f92fdb94a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518378"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a>ESTRUCTURA \_ DE TABLA \_ DE AC \_ HUFFMAN DE DXGI JPEG \_

Describe una tabla JPEG AC huffman.

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

Número de códigos para cada longitud de código.

</dd> <dt>

**CodeValues**
</dt> <dd>

Los valores de código Huffman, en orden de aumentar la longitud del código.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dxgitype.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




