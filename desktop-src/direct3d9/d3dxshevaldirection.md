---
description: Evalúa las funciones de base de armónicos esféricos (SH) a partir de un vector de dirección de entrada.
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: Función D3DXSHEvalDirection (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 005785667d25888550dea38c765a96ea56646d76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104567912"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a>Función D3DXSHEvalDirection (D3dx9math. h)

Evalúa las funciones de base de armónicos esféricos (SH) a partir de un vector de dirección de entrada.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida de armónicos esféricos (SH). La evaluación genera coeficientes de pedido ². Vea la sección Comentarios.

</dd> <dt>

*Pedido* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. La evaluación genera coeficientes de pedido ². El grado de evaluación es order-1.

</dd> <dt>

*pDir* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

(x, y, z): Vector de dirección en el que se van a evaluar las funciones de base de SH. Debe normalizarse. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a los coeficientes de salida SH. Vea la sección Comentarios.

## <a name="remarks"></a>Observaciones

Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:

-   l es el grado de la función base.
-   m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.

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

 

 
