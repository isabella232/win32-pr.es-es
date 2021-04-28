---
description: 'Función D3DXSHRotate (D3dx9math.h): gira el vector de armónico esférico (SH) por la matriz dada.'
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: Función D3DXSHRotate (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f888186fb6d7563a5904d4e6e3f1eabe626afd1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093873"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a>Función D3DXSHRotate (D3dx9math.h)

Gira el vector armónico esférico (SH) por la matriz dada.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a coeficientes de salida de armónica esférica (SH). La evaluación genera coeficientes order-to-order. Este puntero no debe incluir un alias *con pIn*. Vea la sección Comentarios.

</dd> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*pMatrix* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la matriz de rotación. La submatriz de rotación debe ser ortogonal, con una unidad determinante.

</dd> <dt>

*pIn* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero a coeficientes SH girados.

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

[Transferencia de radiancia precalutada (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
