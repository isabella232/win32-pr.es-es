---
description: Devuelve información de material guardada en archivos de Direct3D (.x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: Estructura D3DXMATERIAL (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969724"
---
# <a name="d3dxmaterial-structure"></a>Estructura D3DXMATERIAL

Devuelve información de material guardada en archivos de Direct3D (.x).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a>Members

<dl> <dt>

**MatD3D**
</dt> <dd>

Tipo: **[ **D3DMATERIAL9**](d3dmaterial9.md)**

</dd> <dd>

[**Estructura D3DMATERIAL9**](d3dmaterial9.md) que describe las propiedades del material.

</dd> <dt>

**pTextureFilename**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Puntero a una cadena que especifica el nombre de archivo de la textura.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las funciones [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) y [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) devuelven una matriz de estructuras **D3DXMATERIAL** que especifican el color del material y el nombre de la textura para cada material de la malla. A continuación, se requiere que la aplicación cargue la textura.

El tipo LPD3DXMATERIAL se define como un puntero a la **estructura D3DXMATERIAL.**


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md)
</dt> <dt>

[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




