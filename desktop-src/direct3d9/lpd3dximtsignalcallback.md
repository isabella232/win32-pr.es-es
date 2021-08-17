---
description: Prototipo de función usado por D3DXComputeIMTFromSignal para describir una señal definida por el usuario en el espacio u,v de una malla de entrada. La función evalúa una señal de procedimiento de la dimensión uSignalDimension en la coordenada u,v proporcionada.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e4f6ffaa4c844e755d489aae52dd13b8390da1145734d50f5865bbe0e3cfc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728512"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Prototipo de función usado por [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) para describir una señal definida por el usuario en el espacio u,v de una malla de entrada. La función evalúa una señal de procedimiento de la dimensión uSignalDimension en la coordenada u,v proporcionada.

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

\[in \] uv: puntero a un vector que contiene la coordenada de textura del vértice.

\[en uPrimitiveId: índice del triángulo de entrada en la malla para la \] que se debe calcular la señal.

\[en uSignalDimension: el número de flotantes que se almacenarán en la matriz de datos de señal \] (pfSignalOut).

\[en \] pUserData: el puntero pUserData pasado a [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).

\[out \] pfSignalOut: una matriz de elementos float que contiene los datos de señal.

## <a name="return-value"></a>Valor devuelto

Esta función debe implementarse para devolver S \_ OK.

## <a name="remarks"></a>Comentarios

Asegúrese de especificar la convención de llamada [**Windows de llamada**](../winprog/windows-data-types.md) de tipos de datos al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



| Requisito               | Value            |
|----------------|-------------|
| Encabezado         | d3dx9mesh.h |
| Biblioteca de importación | d3dx9.lib   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
