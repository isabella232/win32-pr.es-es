---
description: 'Función D3DXSHDot (D3dx9math.h): calcula el producto de puntos de dos vectores de armónica esférica (SH).'
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: Función D3DXSHDot (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87f88c7c7b80871a68084607cb99621199dfcc0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093933"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a>Función D3DXSHDot (D3dx9math.h)

Calcula el producto de punto de dos vectores armónicos esféricos (SH).

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación del armónico esférico (SH). Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*pA* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero al primer vector SH.

</dd> <dt>

*pB* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero al segundo vector SH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Coeficientes de salida sh.

## <a name="remarks"></a>Comentarios

Cada coeficiente de la función base Ylm se almacena en la ubicación de memoria lmiento + m + l, donde:

-   l es el grado de la función base.
-   m es el índice de función base para el valor l especificado y va de -l a l, ambos incluidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Transferencia de radiancia precalcalada (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
