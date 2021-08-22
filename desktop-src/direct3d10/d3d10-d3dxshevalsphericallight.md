---
description: 'Función D3DXSHEvalSphericalLight (D3DX10.h): evalúa una luz esférica y devuelve datos esféricos esféricos (SH).'
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: Función D3DXSHEvalSphericalLight (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fa5d1a8dedd9620a3111a1973a26c62c69f138325a19b58632d978f25415b268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990859"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a>Función D3DXSHEvalSphericalLight (D3DX10.h)

Evalúa una luz esférica y devuelve datos esféricos esféricos (SH).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pPos,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*pPos* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a la posición ligera.

</dd> <dt>

*Radio* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radio de la fuente de luz esférica.

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

*pROut* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida para el componente rojo.

</dd> <dt>

*pGOut* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida para el componente verde.

</dd> <dt>

*pBOut* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero al vector SH de salida para el componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Evalúa una luz esférica y devuelve datos sh espectrales. No hay ninguna normalización de la intensidad de la luz como en el caso de las luces direccionales, por lo que se debe tener cuidado al especificar las intensidades. Esto calculará tres ejemplos espectrales; Se devolverá pROut, mientras que se pueden devolver pGOut y pBOut.

En la esfera con radio de unidad, como se muestra en la ilustración siguiente, la dirección se puede especificar simplemente con theta, el ángulo sobre el eje Z en la dirección derecha y el ángulo de la z.

![ilustración de una esfera con radio de unidad](images/spherical-coordinates.png)

Las ecuaciones siguientes muestran la relación entre las coordenadas cartesianas (x, y, z) y esféricas (theta, phi) en la esfera de unidad. El ángulo de theta varía en el intervalo de 0 a 2 pi, mientras que phi varía de 0 a pi.

![ecuaciones de la relación entre coordenadas cartesianas y esféricas](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
