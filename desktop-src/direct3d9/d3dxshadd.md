---
description: 'Función D3DXSHAdd (D3dx9math.h): agrega dos vectores de armónica esférica (SH); en otras palabras, pOut \[ i \] = pA i + \[ \] pB i \[ \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: Función D3DXSHAdd (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117963"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a>Función D3DXSHAdd (D3dx9math.h)

Agrega dos vectores armónicos esféricos (SH); en otras palabras, pOut \[ i \] = pA i + \[ \] pB i \[ \] .

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida sh. La evaluación genera coeficientes order-to-order. Vea la sección Comentarios.

</dd> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida sh.

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

 

 
