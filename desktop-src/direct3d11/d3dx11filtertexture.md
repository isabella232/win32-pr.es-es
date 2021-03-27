---
title: Función D3DX11FilterTexture (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, GenerateMipMaps y GenerateMipMaps3D. Genera una cadena de mipmap mediante un filtro de textura determinado.
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- Función D3DX11FilterTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e74e60e9d66e2a5251c161e4df6451266d3fb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987007"
---
# <a name="d3dx11filtertexture-function"></a>D3DX11FilterTexture función)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GenerateMipMaps** y **GenerateMipMaps3D**.

 

Genera una cadena de mipmap mediante un filtro de textura determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* 
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Un puntero a un objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*pTexture* 
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Objeto de textura que se va a filtrar. Vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*SrcLevel* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nivel de mipmap cuyos datos se utilizan para generar el resto de la cadena de mipmap.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Marcas que controlan la forma en que se filtra cada miplevel (o el \_ valor predeterminado de D3DX11 para el \_ filtro \_ lineal D3DX11). Vea [**D3DX11 \_ Filter \_ Flag**](d3dx11-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

