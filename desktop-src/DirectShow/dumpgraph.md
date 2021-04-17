---
description: La función DumpGraph envía información sobre un gráfico de filtros a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Función DumpGraph (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653746"
---
# <a name="dumpgraph-function"></a><span data-ttu-id="2040c-104">DumpGraph función)</span><span class="sxs-lookup"><span data-stu-id="2040c-104">DumpGraph function</span></span>

<span data-ttu-id="2040c-105">La `DumpGraph` función envía información sobre un gráfico de filtro a la ubicación de salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="2040c-105">The `DumpGraph` function sends information about a filter graph to the debug output location.</span></span> <span data-ttu-id="2040c-106">Se omite en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="2040c-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="2040c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2040c-107">Syntax</span></span>


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a><span data-ttu-id="2040c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2040c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2040c-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="2040c-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="2040c-110">Puntero a la interfaz [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="2040c-110">Pointer to the [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface on the filter graph manager.</span></span>

</dd> <dt>

<span data-ttu-id="2040c-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="2040c-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="2040c-112">Nivel de registro.</span><span class="sxs-lookup"><span data-stu-id="2040c-112">Logging level.</span></span> <span data-ttu-id="2040c-113">La función genera un mensaje de seguimiento de registro \_ con el nivel de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="2040c-113">The function generates a LOG\_TRACE message with the specified logging level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2040c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2040c-114">Return value</span></span>

<span data-ttu-id="2040c-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2040c-115">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2040c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2040c-116">Requirements</span></span>



| <span data-ttu-id="2040c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2040c-117">Requirement</span></span> | <span data-ttu-id="2040c-118">Value</span><span class="sxs-lookup"><span data-stu-id="2040c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2040c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2040c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2040c-120"><dt>Wxdebug. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2040c-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2040c-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2040c-121">Library</span></span><br/> | <dl> <span data-ttu-id="2040c-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2040c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2040c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2040c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2040c-124">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="2040c-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




