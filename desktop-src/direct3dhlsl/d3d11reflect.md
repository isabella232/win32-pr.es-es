---
title: Función D3D11Reflect
description: Obtiene un puntero a una interfaz de reflexión.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- Función HLSL D3D11Reflect
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264327"
---
# <a name="d3d11reflect-function"></a>Función D3D11Reflect

Obtiene un puntero a una interfaz de reflexión.

## <a name="syntax"></a>Sintaxis

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Puntero a los datos de origen como código HLSL compilado.

</dd> <dt>

*SrcDataSize* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Longitud de *pSrcData.*

</dd> <dt>

*ppReflector* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***

Dirección de un puntero a la [**interfaz ID3D11ShaderReflection.**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

Devuelve uno de los códigos de retorno descritos en el tema Códigos de retorno de [Direct3D 11.](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues)

## <a name="remarks"></a>Observaciones

La función del **compilador D3D11Reflect** insertada es un contenedor para la función del [**compilador D3DReflect.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) **D3D11Reflect** solo puede recuperar una [**interfaz ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) de un sombreador. **D3DReflect** puede recuperar una interfaz **ID3D11ShaderReflection** o una interfaz de reflexión Direct3D 10 o Direct3D 10.1, por ejemplo, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).

El código del sombreador contiene metadatos que se pueden inspeccionar mediante las API de reflexión.

El código siguiente muestra cómo recuperar una [**interfaz ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) de un sombreador.


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DCompiler.inl</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>D3dcompiler \_ 47.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3dcompiler \_47.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

