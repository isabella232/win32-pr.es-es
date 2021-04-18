---
description: Prototipo de función que usa D3DXComputeIMTFromSignal para describir una señal definida por el usuario en el espacio u, v de una malla de entrada. La función evalúa una señal de procedimiento de uSignalDimension de dimensión en la coordenada u, v proporcionada.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714655"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Prototipo de función que usa [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) para describir una señal definida por el usuario en el espacio u, v de una malla de entrada. La función evalúa una señal de procedimiento de uSignalDimension de dimensión en la coordenada u, v proporcionada.

## <a name="syntax"></a>Sintaxis


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a>Parámetros

\[en \] UV: puntero a un vector que contiene la coordenada de textura del vértice.

\[en \] uPrimitiveId: el índice del triángulo de entrada en la malla para el que se debe calcular la señal.

\[en \] uSignalDimension: número de flotantes que se van a almacenar en la matriz de datos de señal (pfSignalOut).

\[en \] pUserData: el puntero pUserData se pasa a [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).

\[out \] pfSignalOut: una matriz de floats, que contiene los datos de la señal.

## <a name="return-value"></a>Valor devuelto

Esta función debe implementarse para devolver los valores \_ correctos.

## <a name="remarks"></a>Observaciones

Asegúrese de especificar la Convención de llamada de [**tipos de datos de Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



|                |             |
|----------------|-------------|
| Encabezado         | d3dx9mesh. h |
| Biblioteca de importación | d3dx9. lib   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
