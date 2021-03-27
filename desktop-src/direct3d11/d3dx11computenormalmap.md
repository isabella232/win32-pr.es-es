---
title: Función D3DX11ComputeNormalMap (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, ComputeNormalMap.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- Función D3DX11ComputeNormalMap Direct3D 11
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
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280436"
---
# <a name="d3dx11computenormalmap-function"></a>D3DX11ComputeNormalMap función)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ComputeNormalMap**.

 

Convierte un mapa de alto en un mapa normal. Los componentes (x, y, z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.

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

*pContext* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntero a una interfaz [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) que representa la textura de mapa de alto de origen.

</dd> <dt>

*pSrcTexture* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Puntero a una interfaz [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa la textura de mapa de alto de origen.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Una o varias \_ marcas de NORMALMAP de D3DX que controlan la generación de asignaciones normales.

</dd> <dt>

*Canal* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Una \_ marca de canal de D3DX que especifica el origen de la información de alto.

</dd> <dt>

*Amplitud* \[ de\]
</dt> <dd>

Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

Multiplicador de valor constante que aumenta (o reduce) los valores del mapa normal. Los valores más altos normalmente hacen que los golpes sean más visibles, los valores más bajos normalmente hacen que los golpes sean menos visibles.

</dd> <dt>

*pDestTexture* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Puntero a una interfaz [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa la textura de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método calcula el normal mediante el uso de la diferencia central con el tamaño del kernel 3x3. Los canales RGB del destino contienen componentes sesgados (x, y, z) de la normal. El denominador de diferencia central se codifica en 2,0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

