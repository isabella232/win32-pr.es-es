---
description: 'Función D3DXQuaternionMultiply (D3dx9math.h): multiplica dos cuaterniones.'
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Función D3DXQuaternionMultiply (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7250484e4943e8b077a63e35951c17a44eaf2de3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118043"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a>Función D3DXQuaternionMultiply (D3dx9math.h)

Multiplica dos cuaterniones.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*pQ1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.

</dd> <dt>

*pQ2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el producto de dos cuaterniones.

## <a name="remarks"></a>Comentarios

El resultado representa la rotación Q1 seguida de la rotación Q2 (Out = Q2 \* Q1). Esto se hace para que **D3DXQuaternionMultiply** mantenga la misma semántica que [**D3DXMatrixMultiply,**](d3dxmatrixmultiply.md) ya que los cuaterniones de unidad se pueden considerar como otra manera de representar matrices de rotación.

Las transformaciones se concatenan en el mismo orden para las funciones **D3DXQuaternionMultiply** y [**D3DXMatrixMultiply.**](d3dxmatrixmultiply.md) Por ejemplo, suponiendo que mX y mY representen las mismas rotaciones que qX y qY, m y q representarán las mismas rotaciones.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



La multiplicación de cuaterniones no es conmutativa.

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De este modo, la **función D3DXQuaternionMultiply** se puede usar como parámetro para otra función.

Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




