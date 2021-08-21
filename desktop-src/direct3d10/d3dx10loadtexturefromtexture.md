---
description: Cargar una textura desde una textura.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: Función D3DX10LoadTextureFromTexture (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: bfc36423154bfd56f0695a3a8178b89aefce6e4dfc5a67f3866fa13a99c5e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990505"
---
# <a name="d3dx10loadtexturefromtexture-function"></a>Función D3DX10LoadTextureFromTexture

Cargar una textura desde una textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntero a la textura de origen. Vea [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

Tipo: **[ **INFORMACIÓN DE CARGA DE TEXTURA D3DX10 \_ \_ \_**](d3dx10-texture-load-info.md)\***

Puntero a los parámetros de carga de textura. Vea INFORMACIÓN DE CARGA DE TEXTURA [**D3DX10 \_ \_ \_**](d3dx10-texture-load-info.md).

</dd> <dt>

*pDstTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Puntero a la textura de destino. Vea [**ID3D10Resource (Interfaz).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




