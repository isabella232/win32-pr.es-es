---
description: 'Función D3DXQuaternionMultiply (D3DX10Math.h): multiplica dos cuaterniones.'
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: Función D3DXQuaternionMultiply (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 87d1b386409047eefc3e70ce5007082dda2158122ccfe4e2d3b2bea683a25a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991095"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a>Función D3DXQuaternionMultiply (D3DX10Math.h)

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

Tipo: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***

Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*pQ1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Puntero a una estructura [**D3DXQUATERNION de**](d3d10-d3dxquaternion.md) origen.

</dd> <dt>

*pQ2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Puntero a una estructura [**D3DXQUATERNION de**](d3d10-d3dxquaternion.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntero a una [**estructura D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el producto de dos cuaterniones.

## <a name="remarks"></a>Comentarios

El resultado representa la rotación Q1 seguida de la rotación Q2 (Out = Q2 \* Q1). Esto se hace para que **D3DXQuaternionMultiply** mantenga la misma semántica que [**D3DXMatrixMultiply,**](d3d10-d3dxmatrixmultiply.md) ya que los cuaterniones de unidad se pueden considerar como otra manera de representar matrices de rotación.

Las transformaciones se concatenan en el mismo orden para las funciones **D3DXQuaternionMultiply** y [**D3DXMatrixMultiply.**](d3d10-d3dxmatrixmultiply.md) Por ejemplo, suponiendo que mX y mY representen las mismas rotaciones que qX y qY, m y q representarán las mismas rotaciones.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



La multiplicación de cuaterniones no es conmutativa.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la **función D3DXQuaternionMultiply** se puede usar como parámetro para otra función.

Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
