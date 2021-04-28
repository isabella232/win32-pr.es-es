---
description: 'Función D3DXMatrixRotationYawPitchRoll (D3dx9math.h): crea una matriz con una yaw, pitch y roll especificada.'
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: Función D3DXMatrixRotationYawPitchRoll (D3dx9math.h)
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
ms.openlocfilehash: 789812b6e94efd40ff71209348f0c9727088c253
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118153"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a>Función D3DXMatrixRotationYawPitchRoll (D3dx9math.h)

Crea una matriz con una yaw, pitch y roll especificada.

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

Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*Yaw* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Moverse alrededor del eje Y, en radianes.

</dd> <dt>

*Pitch* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Inclinar alrededor del eje X, en radianes.

</dd> <dt>

*Roll* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Revierte el eje Z, en radianes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) con el yaw, pitch y roll especificados.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la función **D3DXMatrixRotationYawPitchRoll** se puede usar como parámetro para otra función.

El orden de las transformaciones es roll first, then pitch, then yaw. En relación con el eje de coordenadas local del objeto, esto equivale a la rotación alrededor del eje Z, seguida de la rotación alrededor del eje X, seguida de la rotación alrededor del eje Y, como se muestra en la ilustración siguiente.

![ilustración de roll, pitch y yaw como giros alrededor de los tres ejes](images/pitchyawroll.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

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

 

 
