---
title: Función D3DX11ComputeNormalMap (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar la biblioteca DirectXTex ComputeNormalMap.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- D3DX11ComputeNormalMap, función Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747b8b01834126beb12e42d2fa26e15ea99c7471935af8ad74d078d15e9233ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124920"
---
# <a name="d3dx11computenormalmap-function"></a>Función D3DX11ComputeNormalMap

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) **ComputeNormalMap**.

 

Convierte un mapa de alto en un mapa normal. Los componentes (x,y,z) de cada normal se asignan a los canales (r,g,b) de la textura de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntero a una [**interfaz ID3D11DeviceContext,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) que representa la textura del mapa de alto de origen.

</dd> <dt>

*pSrcTexture* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Puntero a una [**interfaz ID3D11Texture2D,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa la textura del mapa de alto de origen.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Una o varias marcas NORMALMAP de D3DX \_ que controlan la generación de mapas normales.

</dd> <dt>

*Canal* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Una marca D3DX \_ CHANNEL que especifica el origen de la información de alto.

</dd> <dt>

*Amplitude* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**

Multiplicador de valor constante que aumenta (o disminuye) los valores del mapa normal. Los valores más altos suelen hacer que los aumentos sean más visibles; los valores más bajos suelen hacer que los aumentos sean menos visibles.

</dd> <dt>

*pDestTexture* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Puntero a una [**interfaz ID3D11Texture2D,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa la textura de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método calcula lo normal mediante la diferencia central con un tamaño de kernel de 3x3. Los canales RGB del destino contienen componentes sesgados (x,y,z) de lo normal. El denominador de diferenciación central se codifica de forma rígida en 2.0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

