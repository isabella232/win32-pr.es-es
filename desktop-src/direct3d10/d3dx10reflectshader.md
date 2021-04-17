---
description: Esta función, que crea un objeto de reflexión de sombreador para recuperar información sobre un sombreador compilado, ya no existe. En su lugar, use D3DReflect o D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: Función D3DX10ReflectShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105653281"
---
# <a name="d3dx10reflectshader-function"></a>D3DX10ReflectShader función)

Esta función, que crea un objeto de reflexión de sombreador para recuperar información sobre un sombreador compilado, ya no existe. En su lugar, use [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) o [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pShaderBytecode* \[ de\]
</dt> <dd>

Tipo: **const void \***

Puntero al sombreador compilado. Para obtener este puntero, vea [obtener un puntero a un sombreador compilado](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

</dd> <dt>

*BytecodeLength* \[ de\]
</dt> <dd>

Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**

Longitud de pShaderBytecode.

</dd> <dt>

*ppReflector* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

Dirección de una interfaz de reflexión del sombreador (vea la [**interfaz ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Este es un ejemplo de creación de un objeto de reflexión de sombreador. En el ejemplo se da por supuesto que empieza con un sombreador compilado (mostrado como


```
pVSBuf
```



que puede ver en el [ejemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
