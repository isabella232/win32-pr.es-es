---
description: Agrega dos vectores armónicos (SH). en otras palabras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Función D3DXSHAdd (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1750b473764daf030160adc42d258a1f911f5f16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280457"
---
# <a name="d3dxshadd-function-d3dx10h"></a>Función D3DXSHAdd (D3DX10. h)

Agrega dos vectores armónicos (SH). en otras palabras, pOut \[ i \] = PA \[ i \] + PB \[ i \] .

## <a name="syntax"></a>Sintaxis


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a los coeficientes de salida SH. La evaluación genera coeficientes de pedido ². Vea la sección Comentarios.

</dd> <dt>

*Pedido* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, ambos incluidos. La evaluación genera coeficientes de pedido ². El grado de evaluación es order-1.

</dd> <dt>

*PA* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntero al primer vector SH.

</dd> <dt>

*PB* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntero al segundo vector SH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a los coeficientes de salida SH.

## <a name="remarks"></a>Observaciones

Cada coeficiente de la función YLM se almacena en la ubicación de memoria l ² + m + l, donde:

-   l es el grado de la función base.
-   m es el índice de la función base para el valor l especificado y los intervalos de-l a l, ambos incluidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
