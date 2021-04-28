---
description: 'Método CBaseRenderer.EndFlush: el método EndFlush finaliza una operación de vaciado.'
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: Método CBaseRenderer.EndFlush (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 87e29f405430ca87943773d19793ffc1941ec42c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095913"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="461ae-103">Método CBaseRenderer.EndFlush</span><span class="sxs-lookup"><span data-stu-id="461ae-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="461ae-104">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="461ae-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="461ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="461ae-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="461ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="461ae-106">Parameters</span></span>

<span data-ttu-id="461ae-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="461ae-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="461ae-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="461ae-108">Return value</span></span>

<span data-ttu-id="461ae-109">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="461ae-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="461ae-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="461ae-110">Remarks</span></span>

<span data-ttu-id="461ae-111">El pin de entrada del filtro llama a este método cuando recibe una llamada al [**método IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)</span><span class="sxs-lookup"><span data-stu-id="461ae-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="461ae-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="461ae-112">Requirements</span></span>



| <span data-ttu-id="461ae-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="461ae-113">Requirement</span></span> | <span data-ttu-id="461ae-114">Value</span><span class="sxs-lookup"><span data-stu-id="461ae-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="461ae-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="461ae-115">Header</span></span><br/>  | <dl> <span data-ttu-id="461ae-116"><dt>Renbase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="461ae-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="461ae-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="461ae-117">Library</span></span><br/> | <dl> <span data-ttu-id="461ae-118"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="461ae-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="461ae-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="461ae-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="461ae-120">**CBaseRenderer (clase)**</span><span class="sxs-lookup"><span data-stu-id="461ae-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




