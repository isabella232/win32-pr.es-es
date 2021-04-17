---
description: Define constantes que describen los valores de estado de la transformación.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumeración D3DTRANSFORMSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717693"
---
# <a name="d3dtransformstatetype-enumeration"></a>Enumeración D3DTRANSFORMSTATETYPE

Define constantes que describen los valores de estado de la transformación.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**\_Vista D3DTS**
</dt> <dd>

Identifica la matriz de transformación que se establece como la matriz de transformación de la vista. El valor predeterminado es **null** (la matriz de identidad).

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_Proyección D3DTS**
</dt> <dd>

Identifica la matriz de transformación que se establece como la matriz de transformación de proyección. El valor predeterminado es **null** (la matriz de identidad).

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**
</dt> <dd>

Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ textura1**
</dt> <dd>

Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ textura2**
</dt> <dd>

Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**
</dt> <dd>

Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**
</dt> <dd>

Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**
</dt> <dd>

Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**
</dt> <dd>

Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**
</dt> <dd>

Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los Estados de transformación en el intervalo de 256 a 511 se reservan para almacenar hasta 256 matrices del mundo que se pueden indexar mediante las \_ macros D3DTS WORLDMATRIX y D3DTS \_ World.



| Macros                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DTS \_ World**](d3dts-world.md)                     | Equivalente a D3DTS \_ WORLDMATRIX (0).                                                                                                                                  |
| [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (índice) | Identifica la matriz de transformación que se va a establecer para la matriz universal en el índice. Las matrices de varios mundo solo se usan para la combinación de vértices. De lo contrario, solo \_ se usa D3DTS World. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**IDirect3DDevice9::MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ World**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ worlda**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
