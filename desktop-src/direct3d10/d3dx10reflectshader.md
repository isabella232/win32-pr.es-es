---
description: Esta función , que crea un objeto de reflexión de sombreador para recuperar información sobre un sombreador compilado, ya no existe. En su lugar, use D3DReflect o D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: Función D3DX10ReflectShader (D3DX10Core.h)
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
ms.openlocfilehash: 7694aa0dcfcc256358993f29c9ed448c1648b35768e5844a959726a6737c2371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753085"
---
# <a name="d3dx10reflectshader-function"></a>Función D3DX10ReflectShader

Esta función , que crea un objeto de reflexión de sombreador para recuperar información sobre un sombreador compilado, ya no existe. En su lugar, [**use D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) o [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).

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

*pShaderBytecode* \[ En\]
</dt> <dd>

Tipo: **const \* void**

Puntero al sombreador compilado. Para obtener este puntero, [vea Getting a Pointer to a Compiled Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

</dd> <dt>

*BytecodeLength* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Longitud de pShaderBytecode.

</dd> <dt>

*ppReflector* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

Dirección de una interfaz de reflexión de sombreador [**(vea ID3D10ShaderReflection1 Interface).**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Este es un ejemplo de creación de un objeto de reflexión de sombreador. En el ejemplo se supone que comienza con un sombreador compilado (que se muestra como


```
pVSBuf
```



que puede ver en [ejemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


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
| Encabezado<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
