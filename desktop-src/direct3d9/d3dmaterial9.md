---
description: Especifica las propiedades del material.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Estructura D3DMATERIAL9 (D3D9Types. h)
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
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424424"
---
# <a name="d3dmaterial9-structure"></a>Estructura D3DMATERIAL9

Especifica las propiedades del material.

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

Valor que especifica el color difuso del material. Vea [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Ambiente**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica el color ambiente del material. Vea [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica el color especular del material. Vea [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Emisor de luz**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica el color de emisor del material. Vea [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Power**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de punto flotante que especifica la nitidez de los reflejos especulares. Cuanto mayor sea el valor, más nítido será el resaltado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para desactivar las iluminaciones especulares, establezca D3DRS \_ SPECULARENABLE en **false**, con [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md). Esta es la opción más rápida porque no se calcularán los reflejos especulares.

Para obtener más información sobre el uso del motor de iluminación para calcular la iluminación especular, vea [iluminación especular (Direct3D 9)](specular-lighting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9::GetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
