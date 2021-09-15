---
title: D3DX11_TEXTURE_LOAD_INFO estructura (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Describe los parámetros usados para cargar una textura desde otra textura.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO estructura direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566309"
---
# <a name="d3dx11_texture_load_info-structure"></a>Estructura DE INFORMACIÓN DE CARGA DE TEXTURA D3DX11 \_ \_ \_

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Describe los parámetros usados para cargar una textura desde otra textura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**pSrcBox**
</dt> <dd>

Tipo: **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Cuadro de textura de origen (vea [**D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Tipo: **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Cuadro de textura de destino (vea [**D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nivel de mapa mipmap de textura de origen, [**consulte D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) para obtener más detalles.

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nivel mipmap de textura de destino, [**consulte D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) para obtener más detalles.

</dd> <dt>

**NumMips**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de niveles de mapa mip en la textura de origen.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Primer elemento de la textura de origen.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Primer elemento de la textura de destino.

</dd> <dt>

**NumElements**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de elementos que se cargarán.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Opciones de filtrado durante el remuestreo (vea [**D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Opciones de filtrado al generar niveles de mip (vea [**D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa en una llamada a [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).

Los valores predeterminados son:


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

