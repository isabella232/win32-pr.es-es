---
description: 'Método CBaseRenderer.BeginFlush: el método BeginFlush comienza una operación de vaciado.'
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Método CBaseRenderer.BeginFlush (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76dfd77a5170a83813871143781868cae55c45ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095943"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="675d3-103">Método CBaseRenderer.BeginFlush</span><span class="sxs-lookup"><span data-stu-id="675d3-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="675d3-104">El `BeginFlush` método comienza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="675d3-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="675d3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="675d3-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="675d3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="675d3-106">Parameters</span></span>

<span data-ttu-id="675d3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="675d3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="675d3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="675d3-108">Return value</span></span>

<span data-ttu-id="675d3-109">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="675d3-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="675d3-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="675d3-110">Remarks</span></span>

<span data-ttu-id="675d3-111">El pin de entrada del filtro llama a este método cuando recibe una llamada al [**método IPin::BeginFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)</span><span class="sxs-lookup"><span data-stu-id="675d3-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="675d3-112">El filtro libera el subproceso de streaming y libera cualquier ejemplo que se retiene para la representación.</span><span class="sxs-lookup"><span data-stu-id="675d3-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="675d3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="675d3-113">Requirements</span></span>



| <span data-ttu-id="675d3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="675d3-114">Requirement</span></span> | <span data-ttu-id="675d3-115">Value</span><span class="sxs-lookup"><span data-stu-id="675d3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="675d3-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="675d3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="675d3-117"><dt>Renbase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="675d3-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="675d3-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="675d3-118">Library</span></span><br/> | <dl> <span data-ttu-id="675d3-119"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="675d3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="675d3-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="675d3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="675d3-121">**CBaseRenderer (clase)**</span><span class="sxs-lookup"><span data-stu-id="675d3-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




