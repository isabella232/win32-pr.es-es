---
description: Inicializa un color con los valores (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: Macro D3DCOLOR_AYUV (D3d9types. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649398"
---
# <a name="d3dcolor_ayuv-macro"></a>D3DCOLOR \_ AYUV (macro)

Inicializa un color con los valores (a, y, u, v).

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

*un* 
</dt> <dd>

Componente alfa del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> <dt>

*y* 
</dt> <dd>

Componente de luminancia del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> <dt>

*u* 
</dt> <dd>

Brillo azul del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> <dt>

*v* 
</dt> <dd>

Brillo rojo del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [D3DCOLOR](d3dcolor.md) que corresponde a los valores ARGB proporcionados.

## <a name="remarks"></a>Observaciones

Un color RGB se puede reducir a 16 bits por píxel mediante la conversión a las diferencias de luminancia y color con las ecuaciones siguientes:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**\_ARGB D3DCOLOR**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ XYUV**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




