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
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="4928f-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="4928f-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="4928f-105">Prototipo de función que usa [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) para describir una señal definida por el usuario en el espacio u, v de una malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="4928f-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="4928f-106">La función evalúa una señal de procedimiento de uSignalDimension de dimensión en la coordenada u, v proporcionada.</span><span class="sxs-lookup"><span data-stu-id="4928f-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="4928f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4928f-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="4928f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4928f-108">Parameters</span></span>

<span data-ttu-id="4928f-109">\[en \] UV: puntero a un vector que contiene la coordenada de textura del vértice.</span><span class="sxs-lookup"><span data-stu-id="4928f-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="4928f-110">\[en \] uPrimitiveId: el índice del triángulo de entrada en la malla para el que se debe calcular la señal.</span><span class="sxs-lookup"><span data-stu-id="4928f-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="4928f-111">\[en \] uSignalDimension: número de flotantes que se van a almacenar en la matriz de datos de señal (pfSignalOut).</span><span class="sxs-lookup"><span data-stu-id="4928f-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="4928f-112">\[en \] pUserData: el puntero pUserData se pasa a [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span><span class="sxs-lookup"><span data-stu-id="4928f-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="4928f-113">\[out \] pfSignalOut: una matriz de floats, que contiene los datos de la señal.</span><span class="sxs-lookup"><span data-stu-id="4928f-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="4928f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4928f-114">Return Value</span></span>

<span data-ttu-id="4928f-115">Esta función debe implementarse para devolver los valores \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="4928f-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4928f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4928f-116">Remarks</span></span>

<span data-ttu-id="4928f-117">Asegúrese de especificar la Convención de llamada de [**tipos de datos de Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="4928f-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="4928f-118">De lo contrario, pueden producirse desbordamientos de pila.</span><span class="sxs-lookup"><span data-stu-id="4928f-118">Otherwise, stack overflows can occur.</span></span>



|                |             |
|----------------|-------------|
| <span data-ttu-id="4928f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4928f-119">Header</span></span>         | <span data-ttu-id="4928f-120">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="4928f-120">d3dx9mesh.h</span></span> |
| <span data-ttu-id="4928f-121">Biblioteca de importación</span><span class="sxs-lookup"><span data-stu-id="4928f-121">Import Library</span></span> | <span data-ttu-id="4928f-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="4928f-122">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="4928f-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4928f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4928f-124">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="4928f-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
