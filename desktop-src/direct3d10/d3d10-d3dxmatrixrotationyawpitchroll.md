---
description: 'Función D3DXMatrixRotationYawPitchRoll (D3DX10Math.h): crea una matriz con una yaw, pitch y roll especificada.'
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: Función D3DXMatrixRotationYawPitchRoll (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae00865c45878159dbf86a6f829e9d1cf50337e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108953"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a>Función D3DXMatrixRotationYawPitchRoll (D3DX10Math.h)

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a una estructura D3DXMATRIX con el yaw, pitch y roll especificados.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXMatrixRotationYawPitchRoll se puede usar como parámetro para otra función.

El orden de las transformaciones es roll first, then pitch, then yaw. En relación con el eje de coordenadas local del objeto, esto equivale a la rotación alrededor del eje Z, seguida de la rotación alrededor del eje X, seguida de la rotación alrededor del eje Y, como se muestra en la ilustración siguiente.

![ilustración de roll, pitch y yaw como giros alrededor de los tres ejes](images/pitchyawroll.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
