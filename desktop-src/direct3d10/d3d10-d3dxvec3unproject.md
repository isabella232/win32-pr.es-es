---
description: Proyecta un vector a partir del espacio de la pantalla en el espacio de objeto.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: Función D3DXVec3Unproject (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 21916392c689bcac794d44ec2c42c3e0b39abb0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678823"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a>Función D3DXVec3Unproject (D3DX10Math. h)

Proyecta un vector a partir del espacio de la pantalla en el espacio de objeto.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

*PV* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a la estructura de D3DXVECTOR3 de origen.

</dd> <dt>

*pViewport* \[ de\]
</dt> <dd>

Tipo: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***

Puntero a una [**\_ ventanilla D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)que representa la ventanilla.

</dd> <dt>

*pProjection* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a una estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que representa la matriz de proyección.

</dd> <dt>

*pView* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a una estructura D3DXMATRIX que representa la matriz de la vista.

</dd> <dt>

*pWorld* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a una estructura D3DXMATRIX que representa la matriz universal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura D3DXVECTOR3 que es el vector proyectado desde el espacio de la pantalla hasta el espacio del objeto.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función D3DXVec3Unproject se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
