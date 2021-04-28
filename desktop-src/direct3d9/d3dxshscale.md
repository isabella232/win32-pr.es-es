---
description: 'Función D3DXSHScale (D3dx9math.h): escala un vector de armónica esférica (SH); en otras palabras, pOut \[ i \] = pA i \[ \] \* Scale.'
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: Función D3DXSHScale (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6a91c3ea1cb49c4c501ab847cb63fe8a39d66665
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093863"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a>Función D3DXSHScale (D3dx9math.h)

Escala un vector armónico esférico (SH); en otras palabras, pOut \[ i \] = pA i \[ \] \* Scale.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
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

*pIn* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero al vector SH que se escala.

</dd> <dt>

*Escala* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero al valor de escala.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida sh.

## <a name="remarks"></a>Comentarios

Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:

-   l es el grado de la función base.
-   m es el índice de función base para el valor l especificado y va de -l a l, ambos inclusive.

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

 

 
