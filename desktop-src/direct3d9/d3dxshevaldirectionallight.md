---
description: Evalúa una luz direccional y devuelve datos armónicos esféricos (SH).
ms.assetid: 6e2e9b02-13bb-4cef-ae9d-343fbf64e5d7
title: Función D3DXSHEvalDirectionalLight (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c78ee4059ed83b97e7ac1f392f857351df48ee7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104567659"
---
# <a name="d3dxshevaldirectionallight-function-d3dx9mathh"></a>Función D3DXSHEvalDirectionalLight (D3dx9math. h)

Evalúa una [luz direccional](light-types.md) y devuelve datos armónicos esféricos (SH).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pedido* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. La evaluación genera coeficientes de pedido ². El grado de evaluación es order-1.

</dd> <dt>

*pDir* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero al vector de dirección del eje hemisferio (x, y, z) en el que se van a evaluar las funciones de base de SH. Vea la sección Comentarios.

</dd> <dt>

*RIntensity* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Intensidad roja de la luz.

</dd> <dt>

*GIntensity* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Intensidad verde de la luz.

</dd> <dt>

*BIntensity* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Intensidad azul de la luz.

</dd> <dt>

*pROut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida para el componente rojo.

</dd> <dt>

*pGOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero opcional al vector SH de salida para el componente verde.

</dd> <dt>

*pBOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero opcional al vector SH de salida para el componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

El vector de salida se calcula de modo que si la relación de intensidad R/G/B es igual a 1, el Radiance de salida resultante de un punto situado directamente debajo de la luz en un objeto difuso con un albedo de 1 sería 1,0. Se calcularán tres muestras espectrales; se devolverá *pROut* , mientras que *pGOut* y *pBOut* se pueden devolver.

En la esfera con radio de unidad, tal y como se muestra en la siguiente ilustración, la dirección se puede especificar simplemente con Theta, el ángulo del eje z en la dirección de la [mano derecha](coordinate-systems.md)y la PHI, el ángulo de z.

![Ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (Theta, PHI) en la esfera de unidad. El ángulo Zeta varía en el intervalo de 0 a 2 PI, mientras que la PHI varía de 0 a pi.

![ecuaciones de la relación entre las coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Transferencia Radiance precalculada (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
