---
description: Describe los datos incluidos en la enumeración.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: Enumeración D3DXPARAMETER_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362430"
---
# <a name="d3dxparameter_type-enumeration"></a>\_Enumeración de tipo D3DXPARAMETER

Describe los datos incluidos en la enumeración.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**
</dt> <dd>

El parámetro es un puntero void.

</dd> <dt>

<span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT \_ bool**
</dt> <dd>

El parámetro es un valor booleano. Cualquier valor distinto de cero que se pase a [**ID3DXConstantTable:: SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable:: SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: SetVector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) se asignará a 1 (true) antes de escribirse en la tabla de constantes. de lo contrario, el valor se establecerá en 0 en la tabla Constant.

</dd> <dt>

<span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ int**
</dt> <dd>

El parámetro es un entero. Los valores de punto flotante pasados en [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: SetVector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) se redondearán (a cero posiciones decimales) antes de escribirse en la tabla de constantes.

</dd> <dt>

<span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ float**
</dt> <dd>

El parámetro es un número de punto flotante.

</dd> <dt>

<span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Cadena D3DXPT**
</dt> <dd>

El parámetro es una cadena.

</dd> <dt>

<span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Textura D3DXPT**
</dt> <dd>

El parámetro es una textura.

</dd> <dt>

<span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**
</dt> <dd>

El parámetro es una textura 1D.

</dd> <dt>

<span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**
</dt> <dd>

El parámetro es una textura 2D.

</dd> <dt>

<span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**
</dt> <dd>

El parámetro es una textura 3D.

</dd> <dt>

<span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**
</dt> <dd>

El parámetro es una textura del cubo.

</dd> <dt>

<span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**Muestra de D3DXPT \_**
</dt> <dd>

El parámetro es una muestra.

</dd> <dt>

<span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**
</dt> <dd>

El parámetro es una muestra 1D.

</dd> <dt>

<span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**
</dt> <dd>

El parámetro es una muestra 2D.

</dd> <dt>

<span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**
</dt> <dd>

El parámetro es una muestra 3D.

</dd> <dt>

<span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**
</dt> <dd>

El parámetro es una muestra de cubo.

</dd> <dt>

<span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ u**
</dt> <dd>

El parámetro es un sombreador de píxeles.

</dd> <dt>

<span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**
</dt> <dd>

El parámetro es un sombreador de vértices.

</dd> <dt>

<span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**
</dt> <dd>

El parámetro es un fragmento de sombreador de píxeles.

</dd> <dt>

<span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**
</dt> <dd>

El parámetro es un fragmento de sombreador de vértices.

</dd> <dt>

<span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ no compatible**
</dt> <dd>

No se admite el parámetro.

</dd> <dt>

<span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




