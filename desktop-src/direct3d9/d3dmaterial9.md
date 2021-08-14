---
description: Especifica las propiedades de material.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Estructura D3DMATERIAL9 (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 640fd4ce0110f47aa20a04d0df595b0ae8bf5052c229825dd93e1066150c6306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527585"
---
# <a name="d3dmaterial9-structure"></a>D3DMATERIAL9 (estructura)

Especifica las propiedades de material.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica el color difuso del material. Vea [**D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Ambiente**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica el color ambiente del material. Vea [**D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica el color especular del material. Vea [**D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Emisor de luz**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica el color emisivo del material. Vea [**D3DCOLORVALUE.**](d3dcolorvalue.md)

</dd> <dt>

**Power**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de punto flotante que especifica la niguidad de los resaltados especulares. Cuanto mayor sea el valor, más nítido será el resaltado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para desactivar los resaltados especulares, establezca D3DRS \_ SPECULARENABLE en **FALSE** mediante [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md). Esta es la opción más rápida porque no se calculará ningún resaltado especular.

Para obtener más información sobre el uso del motor de iluminación para calcular la iluminación especular, vea [Specular Lighting (Direct3D 9) ( Iluminación especular [Direct3D 9]).](specular-lighting.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9::GetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
