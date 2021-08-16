---
description: Inicializa un color con los valores (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: D3DCOLOR_XYUV macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: caa6bc1eb9586c1526a7af674040fd703ff0a75a5055ce42e13378206e82c879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300329"
---
# <a name="d3dcolor_xyuv-macro"></a>Macro D3DCOLOR \_ XYUV

Inicializa un color con los valores (y, u, v).

## <a name="syntax"></a>Sintaxis


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*y* 
</dt> <dd>

Componente de luminosidad del color. Este valor debe estar en el intervalo de 0 a 255.

</dd> <dt>

*u* 
</dt> <dd>

Brillo azul del color. Este valor debe estar en el intervalo de 0 a 255.

</dd> <dt>

*V* 
</dt> <dd>

Brillo rojo del color. Este valor debe estar en el intervalo de 0 a 255.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [**valor D3DCOLOR**](d3dcolor.md) que corresponde a los valores proporcionados (y, u, v).

## <a name="remarks"></a>Comentarios

Un color RGB se puede reducir a 16 bits por píxel mediante la conversión a diferencias de luminosidad y color con las ecuaciones siguientes:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ AYUV**](d3dcolor-ayuv.md)
</dt> </dl>

 

 




