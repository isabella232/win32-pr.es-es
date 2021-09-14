---
description: Inicializa un color con los valores (a, y, u,v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: D3DCOLOR_AYUV macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160446"
---
# <a name="d3dcolor_ayuv-macro"></a>Macro D3DCOLOR \_ AYUV

Inicializa un color con los valores (a, y, u,v).

## <a name="syntax"></a>Sintaxis


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Un* 
</dt> <dd>

Componente alfa del color. Este valor debe estar entre 0 y 255.

</dd> <dt>

*y* 
</dt> <dd>

Componente de luminosidad del color. Este valor debe estar entre 0 y 255.

</dd> <dt>

*u* 
</dt> <dd>

Brillo azul del color. Este valor debe estar entre 0 y 255.

</dd> <dt>

*V* 
</dt> <dd>

Brillo rojo del color. Este valor debe estar entre 0 y 255.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [valor D3DCOLOR](d3dcolor.md) que corresponde a los valores ARGB proporcionados.

## <a name="remarks"></a>Observaciones

Un color RGB se puede reducir a 16 bits por píxel mediante la conversión a las diferencias de luminosidad y color con las siguientes ecuaciones:


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

[**D3DCOLOR \_ XYUV**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




