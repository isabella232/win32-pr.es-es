---
description: 'Función D3DXPlaneNormalize (D3dx9math.h): normaliza los coeficientes de plano para que el plano normal tenga longitud de unidad.'
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Función D3DXPlaneNormalize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d38ccbc3f688ed61779cf48a77e97dfb544c686e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094153"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>Función D3DXPlaneNormalize (D3dx9math.h)

Normaliza los coeficientes del plano para que el plano normal tenga longitud de unidad.

## <a name="syntax"></a>Sintaxis


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a la [**estructura D3DXPLANE**](d3dxplane.md) que es el resultado de la operación.

</dd> <dt>

*pP* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntero a la estructura [**D3DXPLANE de**](d3dxplane.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntero a una [**estructura D3DXPLANE**](d3dxplane.md) que representa la normalidad del plano.

## <a name="remarks"></a>Comentarios

Esta función normaliza un plano para \| que a,b,c \| == 1.

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, esta función se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




