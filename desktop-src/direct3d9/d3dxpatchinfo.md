---
description: Estructura que contiene los atributos de una malla de revisión.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: Estructura D3DXPATCHINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362428"
---
# <a name="d3dxpatchinfo-structure"></a>Estructura D3DXPATCHINFO

Estructura que contiene los atributos de una malla de revisión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**PatchType**
</dt> <dd>

Tipo: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**

</dd> <dd>

Tipo de revisión. Para obtener información sobre los tipos de revisión, vea [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).

</dd> <dt>

**Grado**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Grado de las curvas utilizadas para construir la revisión. Para obtener información acerca de los grados admitidos, vea [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Tipo de curva que se usa para construir la revisión. Para obtener información sobre los tipos de base admitidos, vea [**D3DBASISTYPE**](./d3dbasistype.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una malla es un conjunto de caras, cada una de las cuales se describe mediante un polígono simple. Los objetos se pueden crear conectando varias mallas juntas. Una malla de revisión se construye a partir de revisiones. Una revisión es una pieza de cuatro caras de geometría construida a partir de curvas. El tipo de curva que se usa y el orden de la curva pueden ser variados para que la superficie de la revisión quepa prácticamente cualquier forma de superficie.

Se admiten los siguientes tipos de combinaciones de revisiones:



| Tipo de revisión | Basis       | Grado |
|------------|-------------|--------|
| Rectángulo  | Bézier      | 2, 3, 5  |
| Rectángulo  | Spline B    | 2, 3, 5  |
| Rectángulo  | Catmull-Rom | 3      |
| Triangle   | Bézier      | 2, 3, 5  |
| N-patch    | N/D         | 3      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**Información de D3DRECTPATCH \_**](d3drectpatch-info.md)
</dt> <dt>

[**Información de D3DTRIPATCH \_**](d3dtripatch-info.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
