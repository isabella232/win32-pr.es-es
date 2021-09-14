---
description: 'Función D3DXVec3Project (D3dx9math.h): proyecta un vector 3D desde el espacio de objetos en el espacio de la pantalla.'
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: Función D3DXVec3Project (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5a9abcb54c883d74bde831570b9df0b40fedfae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060681"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a>Función D3DXVec3Project (D3dx9math.h)

Proyecta un vector 3D desde el espacio del objeto en el espacio de la pantalla.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.

</dd> <dt>

*pViewport* \[ En\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Puntero a una [**estructura D3DVIEWPORT9,**](d3dviewport9.md) que representa la ventanilla.

</dd> <dt>

*pProjection* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz de proyección.

</dd> <dt>

*pView* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz de vistas.

</dd> <dt>

*pWorld* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz mundial.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el vector proyectado desde el espacio del objeto al espacio de pantalla.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXVec3Project** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Unproject**](d3dxvec3unproject.md)
</dt> </dl>

 

 




