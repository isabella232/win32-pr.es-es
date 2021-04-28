---
description: 'Función D3DXSHEvalDirection (D3dx9math.h): evalúa las funciones básicas de armónica esférica (SH) a partir de un vector de dirección de entrada.'
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: Función D3DXSHEvalDirection (D3dx9math.h)
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
ms.openlocfilehash: e02f0f3d8770b4b703f275de3225eacb301a7843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093970"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a>Función D3DXSHEvalDirection (D3dx9math.h)

Evalúa las funciones básicas de armónica esférica (SH) a partir de un vector de dirección de entrada.

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

*pOut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida de armónica esférica (SH). La evaluación genera coeficientes order-to-order. Vea la sección Comentarios.

</dd> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*pDir* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

(x, y, z) vector de dirección en el que se evaluarán las funciones de base sh. Debe normalizarse. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida sh. Vea la sección Comentarios.

## <a name="remarks"></a>Comentarios

Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:

-   l es el grado de la función base.
-   m es el índice de función base para el valor l especificado y va de -l a l, ambos incluidos.

En la esfera con radio de unidad, como se muestra en la ilustración siguiente, la dirección [](coordinate-systems.md)se puede especificar simplemente con theta, el ángulo sobre el eje Z en la dirección derecha y el ángulo de la z.

![ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (theta, phi) en la esfera de unidad. El ángulo de theta varía en el intervalo de 0 a 2 pi, mientras que phi varía de 0 a pi.

![ecuaciones de la relación entre coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Transferencia de radiancia precalutada (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
