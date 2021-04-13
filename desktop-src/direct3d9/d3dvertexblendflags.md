---
description: Define las marcas que se usan para controlar el número o las matrices que el sistema aplica al realizar la combinación de vértices multimatrix.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Enumeración D3DVERTEXBLENDFLAGS (D3D9Types. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362546"
---
# <a name="d3dvertexblendflags-enumeration"></a>Enumeración D3DVERTEXBLENDFLAGS

Define las marcas que se usan para controlar el número o las matrices que el sistema aplica al realizar la combinación de vértices multimatrix.

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

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**Deshabilitación de D3DVBF \_**
</dt> <dd>

Deshabilitar la fusión de vértices; Aplique solo la matriz universal establecida por la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , donde el valor de índice para el estado de transformación es 0.

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**
</dt> <dd>

Habilite la fusión de vértices entre las dos matrices establecidas por la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , donde el valor de índice para los Estados de transformación es 0 y 1.

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**
</dt> <dd>

Habilite la fusión de vértices entre las tres matrices establecidas por la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , donde el valor de índice para los Estados de transformación es 0, 1 y 2.

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**
</dt> <dd>

Habilite la fusión de vértices entre las cuatro matrices establecidas por la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , donde el valor de índice para los Estados de transformación es 0, 1, 2 y 3.

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**Intercalación de D3DVBF \_**
</dt> <dd>

La mezcla de vértices se realiza mediante el valor asignado a D3DRS \_ TWEENFACTOR.

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**
</dt> <dd>

Use una sola matriz con un peso de 1,0.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los miembros de este tipo se usan con el \_ Estado de representación de VERTEXBLEND de D3DRS.

La combinación de geometría (combinación de vértices multimatriz) requiere que la aplicación use un formato de vértice con pesos de fusión (beta) para cada vértice.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**D3DTS \_ World**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ worlda**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
