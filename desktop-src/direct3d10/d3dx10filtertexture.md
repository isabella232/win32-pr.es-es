---
description: Genera una cadena de mipmap mediante un filtro de textura determinado.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: Función D3DX10FilterTexture (D3DX10Tex. h)
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
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707729"
---
# <a name="d3dx10filtertexture-function"></a>D3DX10FilterTexture función)

Genera una cadena de mipmap mediante un filtro de textura determinado.

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Nivel de mipmap cuyos datos se utilizan para generar el resto de la cadena de mipmap.

</dd> <dt>

*MipFilter* 
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Marcas que controlan cómo se filtra cada miplevel (o el \_ valor predeterminado de D3DX10 para el \_ cuadro de filtro D3DX10 \_ ). Vea [**D3DX10 \_ Filter \_ Flag**](d3dx10-filter-flag.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
