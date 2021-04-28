---
description: 'Función D3DXSHEvalConeLight (D3dx9math.h): evalúa una luz que es un cono de intensidad constante y devuelve datos de armónica esférica esférica (SH).'
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: Función D3DXSHEvalConeLight (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31c90e705a0bb4e82813fff42673e143c5acf171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117953"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a>Función D3DXSHEvalConeLight (D3dx9math.h)

Evalúa una luz que es un cono de intensidad constante y devuelve datos esféricos armónicos esféricos (SH).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSHEvalConeLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       Radius,
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

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*pDir* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero al vector de dirección del eje (x, y, z) en el que se evaluarán las funciones de base sh. Vea la sección Comentarios.

</dd> <dt>

*Radio* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radio de cono en radianes.

</dd> <dt>

*RIntensity* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Intensidad roja de la luz.

</dd> <dt>

*GIntensity* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Intensidad verde de la luz.

</dd> <dt>

*BIntensity* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Intensidad azul de la luz.

</dd> <dt>

*pROut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida para el componente rojo.

</dd> <dt>

*pGOut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida para el componente verde.

</dd> <dt>

*pBOut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida para el componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Evalúa una luz que es un cono de intensidad constante y devuelve datos sh espectrales. El vector de salida se calcula de modo que si la relación de intensidad R/G/B es igual a 1, la intensidad de salida de un punto directamente debajo de la luz (orientada en la dirección del cono en un objeto difuso con un albedo de 1) sería 1,0. Esto calculará tres ejemplos espectrales; *se devolverá pROut,* mientras que se pueden devolver *pGOut* y *pBOut.*

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

 

 
