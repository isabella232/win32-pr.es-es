---
description: Define constantes que describen los valores de estado de transformación.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumeración D3DTRANSFORMSTATETYPE (D3D9Types.h)
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
ms.openlocfilehash: 022aa20fab0739b32aa75eb5f4bc575c0a8ad853
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343000"
---
# <a name="d3dtransformstatetype-enumeration"></a>D3DTRANSFORMSTATETYPE (enumeración)

Define constantes que describen los valores de estado de transformación.

## <a name="syntax"></a>Syntax


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

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**VISTA \_ D3DTS**
</dt> <dd>

Identifica la matriz de transformación que se establece como la matriz de transformación de vista. El valor predeterminado es **NULL** (la matriz de identidad).

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**PROYECCIÓN DE \_ D3DTS**
</dt> <dd>

Identifica la matriz de transformación que se establece como matriz de transformación de proyección. El valor predeterminado es **NULL** (la matriz de identidad).

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**TEXTURA DE \_ D3DTS0**
</dt> <dd>

Identifica la matriz de transformación que se establece para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**TEXTURA D3DTS1 \_**
</dt> <dd>

Identifica la matriz de transformación que se establece para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**TEXTURA DE \_ D3DTS2**
</dt> <dd>

Identifica la matriz de transformación que se establece para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**TEXTURA DE \_ D3DTS3**
</dt> <dd>

Identifica la matriz de transformación que se establece para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**TEXTURA D3DTS4 \_**
</dt> <dd>

Identifica la matriz de transformación que se establece para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**TEXTURA DE \_ D3DTS5**
</dt> <dd>

Identifica la matriz de transformación que se establece para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**TEXTURA DE \_ D3DTS6**
</dt> <dd>

Identifica la matriz de transformación que se establece para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**TEXTURA D3DTS7 \_**
</dt> <dd>

Identifica la matriz de transformación que se establece para la fase de textura especificada.

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los estados de transformación del intervalo de 256 a 511 están reservados para almacenar hasta 256 matrices globales que se pueden indexar mediante las \_ macros WORLDMATRIX y D3DTS WORLD de D3DTS. \_



| Macros                                                  | Descripción                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DTS \_ WORLD**](d3dts-world.md)                     | Equivalente a D3DTS \_ WORLDMATRIX(0).                                                                                                                                  |
| [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (índice) | Identifica la matriz de transformación que se establecerá para la matriz mundial en el índice. Solo se usan varias matrices de mundo para la mezcla de vértices. De lo contrario, solo se usa D3DTS \_ WORLD. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



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

[**D3DTS \_ WORLD**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
