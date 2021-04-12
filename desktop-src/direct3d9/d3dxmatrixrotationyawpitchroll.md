---
description: Crea una matriz con un guiñada, un tono y un rollo especificados.
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: Función D3DXMatrixRotationYawPitchRoll (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2a8d6a531592ce49342dae0d0ecd6b3ace995bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280245"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a>Función D3DXMatrixRotationYawPitchRoll (D3dx9math. h)

Crea una matriz con un guiñada, un tono y un rollo especificados.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*Guiñada* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Guiña alrededor del eje y, en radianes.

</dd> <dt>

*Paso* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Paso alrededor del eje x, en radianes.

</dd> <dt>

Poner al *día* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Desplazarse alrededor del eje z, en radianes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) con el guiñada, el tono y el rollo especificados.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXMatrixRotationYawPitchRoll** se puede usar como parámetro de otra función.

El orden de las transformaciones se revierte primero, después por el paso y después por el guiñada. En relación con el eje de coordenadas local del objeto, es equivalente a la rotación alrededor del eje z, seguido de la rotación alrededor del eje x, seguido de la rotación alrededor del eje y, tal y como se muestra en la siguiente ilustración.

![Ilustración del rollo, el tono y el guiñada como giros alrededor de los tres ejes](images/pitchyawroll.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**D3DXMatrixRotationQuaternion**](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
