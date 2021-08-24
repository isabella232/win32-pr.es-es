---
description: Describe los parámetros usados para cargar una textura desde otra textura.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: D3DX10_TEXTURE_LOAD_INFO estructura (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 144475b4b4967ff0a1fd130a658b8276af5d8897cc043000d150417aa01b227e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753475"
---
# <a name="d3dx10_texture_load_info-structure"></a>Estructura DE INFORMACIÓN DE CARGA DE TEXTURA D3DX10 \_ \_ \_

Describe los parámetros usados para cargar una textura desde otra textura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pSrcBox**
</dt> <dd>

Tipo: **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Cuadro de textura de origen (vea [**D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Tipo: **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Cuadro de textura de destino (vea [**D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Nivel de mapa mipmap de textura de origen, [**consulte D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) para obtener más detalles.

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Nivel mipmap de textura de destino, [**consulte D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) para obtener más detalles.

</dd> <dt>

**NumMips**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de niveles de mapa mip en la textura de origen.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Primer elemento de la textura de origen.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Primer elemento de la textura de destino.

</dd> <dt>

**NumElements**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos que se cargarán.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Opciones de filtrado durante el remuestreo (vea [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Opciones de filtrado al generar niveles de mip (vea [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa en una llamada a [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
