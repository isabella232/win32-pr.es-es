---
description: 'Función D3DXSHDot (D3DX10.h): calcula el producto de puntos de dos vectores armónicos esféricos (SH).'
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: Función D3DXSHDot (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 77595f5aac53572813be72f498944b029dc42491c376410645037dcbfd4c01f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990925"
---
# <a name="d3dxshdot-function-d3dx10h"></a>Función D3DXSHDot (D3DX10.h)

Calcula el producto de puntos de dos vectores armónicos esféricos (SH).

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

Orden de la evaluación armónica esférica (SH). Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*pA* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero al primer vector SH.

</dd> <dt>

*pB* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero al segundo vector sh.

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
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
