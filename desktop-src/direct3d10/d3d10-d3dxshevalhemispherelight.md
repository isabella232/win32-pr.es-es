---
description: Evalúa una luz que es una interpolación lineal entre dos colores en la esfera.
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: Función D3DXSHEvalHemisphereLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c6ff3359ce0629eec472e4da24a31c24196c7f15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362664"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a>Función D3DXSHEvalHemisphereLight (D3DX10. h)

Evalúa una luz que es una interpolación lineal entre dos colores en la esfera.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pedido* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Orden de evaluación de armónicos esférico (SH). Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos incluidos. La evaluación genera coeficientes de pedido ². El grado de evaluación es order-1.

</dd> <dt>

*pDir* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero al vector de dirección del eje hemisferio (x, y, z) en el que se van a evaluar las funciones de base de SH. Vea la sección Comentarios.

</dd> <dt>

*Parte superior* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Color del cielo.

</dd> <dt>

*Inferior* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Color de fondo.

</dd> <dt>

*pROut* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida para el componente rojo.

</dd> <dt>

*pGOut* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida del componente verde.

</dd> <dt>

*pBOut* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida para el componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

La interpolación se realiza linealmente entre los dos puntos, no en la superficie de la esfera (es decir, si el eje era (0, 0, 1) es lineal en Z, no en el ángulo azimuthal). La función de iluminación esférica resultante se normaliza de modo que un punto en una superficie difusa perfecta sin sombreado y una normal señalada en la dirección pDir daría como resultado Radiance de salida con un valor de 1 (si el color superior fuera blanco y el color inferior era negro). Se trata de un modelo muy sencillo, donde la parte superior representa la intensidad del "cielo" y la parte inferior representa la intensidad de la "base".

En la esfera con radio de unidad, tal y como se muestra en la siguiente ilustración, la dirección se puede especificar simplemente con Theta, el ángulo del eje z en la dirección de la mano derecha y la PHI, el ángulo de z.

![Ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (Theta, PHI) en la esfera de unidad. El ángulo Zeta varía en el intervalo de 0 a 2 PI, mientras que la PHI varía de 0 a pi.

![ecuaciones de la relación entre las coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
