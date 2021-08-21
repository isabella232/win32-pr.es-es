---
description: Genera la cadena mipmap mediante un filtro de textura determinado.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: Función D3DX10FilterTexture (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 225caf2c9b08a498e77723dbb7ab43c8fd4850262c1f58f5ae37a3157e953edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497645"
---
# <a name="d3dx10filtertexture-function"></a>Función D3DX10FilterTexture

Genera la cadena mipmap mediante un filtro de textura determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexture* 
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Objeto de textura que se va a filtrar. Vea [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*SrcLevel* 
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nivel de mapa mip cuyos datos se usan para generar el resto de la cadena mipmap.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Marcas que controlan cómo se filtra cada miplevel (o D3DX10 \_ DEFAULT para D3DX10 \_ FILTER \_ BOX). Vea [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md).

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

 

 
