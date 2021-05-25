---
description: Prototipo de función usado por D3DXComputeIMTFromSignal para describir una señal definida por el usuario en el espacio u,v de una malla de entrada. La función evalúa una señal de procedimiento de la dimensión uSignalDimension en la coordenada u,v proporcionada.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342840"
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

\[in uPrimitiveId: índice del triángulo de entrada en la malla para la \] que se debe calcular la señal.

\[en uSignalDimension: el número de elementos float que se almacenarán en la matriz de datos de \] señal (pfSignalOut).

\[en \] pUserData: el puntero pUserData pasado a [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).

\[out \] pfSignalOut: una matriz de elementos float que contiene los datos de señal.

## <a name="return-value"></a>Valor devuelto

Esta función debe implementarse para devolver S \_ OK.

## <a name="remarks"></a>Comentarios

Asegúrese de especificar la convención de llamada tipos de datos de [**Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



| Requisito               | Value            |
|----------------|-------------|
| Encabezado         | d3dx9mesh.h |
| Biblioteca de importación | d3dx9.lib   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
