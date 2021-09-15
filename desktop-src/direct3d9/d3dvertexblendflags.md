---
description: Define las marcas usadas para controlar el número o las matrices que el sistema aplica al realizar la mezcla de vértices multimatrix.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Enumeración D3DVERTEXBLENDFLAGS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465391"
---
# <a name="d3dvertexblendflags-enumeration"></a>Enumeración D3DVERTEXBLENDFLAGS

Define las marcas usadas para controlar el número o las matrices que el sistema aplica al realizar la mezcla de vértices multimatrix.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF \_ DISABLE**
</dt> <dd>

Deshabilitar la mezcla de vértices; aplique solo la matriz mundial establecida por la macro [**\_ WORLDMATRIX de D3DTS,**](d3dts-worldmatrix.md) donde el valor de índice para el estado de transformación es 0.

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**
</dt> <dd>

Habilite la combinación de vértices entre las dos matrices establecidas por la macro [**\_ WORLDMATRIX de D3DTS,**](d3dts-worldmatrix.md) donde el valor de índice de los estados de transformación es 0 y 1.

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**
</dt> <dd>

Habilite la combinación de vértices entre las tres matrices establecidas por la macro [**\_ WORLDMATRIX de D3DTS,**](d3dts-worldmatrix.md) donde el valor de índice de los estados de transformación es 0, 1 y 2.

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**
</dt> <dd>

Habilite la combinación de vértices entre las cuatro matrices establecidas por la macro [**\_ WORLDMATRIX de D3DTS,**](d3dts-worldmatrix.md) donde el valor de índice para los estados de transformación es 0, 1, 2 y 3.

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**INTERPOLACIÓN D3DVBF \_**
</dt> <dd>

La mezcla de vértices se realiza mediante el valor asignado a D3DRS \_ TWEENFACTOR.

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**
</dt> <dd>

Use una sola matriz con un peso de 1,0.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los miembros de este tipo se usan con el estado de representación D3DRS \_ VERTEXBLEND.

La combinación de geometría (mezcla de vértices multimatrix) requiere que la aplicación use un formato de vértice que tenga pesos de mezcla (beta) para cada vértice.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**D3DTS \_ WORLD**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
