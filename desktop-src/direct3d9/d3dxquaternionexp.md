---
description: 'Función D3DXQuaternionExp (D3dx9math.h): calcula el valor exponencial.'
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: Función D3DXQuaternionExp (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2a69364e3cb294f088023d7e67973fb55f6e3396987ee9b63e9f9383dcf81917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044753"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a>Función D3DXQuaternionExp (D3dx9math.h)

Calcula el valor exponencial.

## <a name="syntax"></a>Sintaxis


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.

</dd> <dt>

*pQ* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a la estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es exponencial.

## <a name="remarks"></a>Comentarios

Este método convierte un cuaternión puro en un cuaternión de unidad. **D3DXQuaternionExp** espera un cuaternión puro, donde w se omite en el cálculo (w == 0).


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



donde v es la parte vectorial de un cuaternión.

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXQuaternionExp** se puede usar como parámetro para otra función.

El [**método D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) también se puede usar para configurar los puntos de control de un cuaternión.

Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionLn**](d3dxquaternionln.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 




