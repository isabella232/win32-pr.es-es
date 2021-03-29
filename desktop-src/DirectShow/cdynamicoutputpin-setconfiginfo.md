---
description: El método SetConfigInfo especifica el puntero IGraphConfig y el evento STOP.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Método CDynamicOutputPin. SetConfigInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660509"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a><span data-ttu-id="fef40-103">CDynamicOutputPin. SetConfigInfo, método</span><span class="sxs-lookup"><span data-stu-id="fef40-103">CDynamicOutputPin.SetConfigInfo method</span></span>

<span data-ttu-id="fef40-104">El `SetConfigInfo` método especifica el puntero [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) y el evento STOP.</span><span class="sxs-lookup"><span data-stu-id="fef40-104">The `SetConfigInfo` method specifies the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) pointer and the stop event.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef40-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fef40-105">Syntax</span></span>


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a><span data-ttu-id="fef40-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fef40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fef40-107">*pGraphConfig*</span><span class="sxs-lookup"><span data-stu-id="fef40-107">*pGraphConfig*</span></span> 
</dt> <dd>

<span data-ttu-id="fef40-108">Puntero a la interfaz [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) o **null**.</span><span class="sxs-lookup"><span data-stu-id="fef40-108">Pointer to the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) interface, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fef40-109">*hStopEvent*</span><span class="sxs-lookup"><span data-stu-id="fef40-109">*hStopEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="fef40-110">Identificador de un evento que se señala cuando se detiene el filtro o **null**.</span><span class="sxs-lookup"><span data-stu-id="fef40-110">Handle to an event that is signaled when the filter stops, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fef40-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fef40-111">Return value</span></span>

<span data-ttu-id="fef40-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fef40-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fef40-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fef40-113">Remarks</span></span>

<span data-ttu-id="fef40-114">El filtro debe llamar a este método cuando se une al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="fef40-114">The filter must call this method when it joins the filter graph.</span></span> <span data-ttu-id="fef40-115">El administrador de gráficos de filtros es compatible con **IGraphConfig**.</span><span class="sxs-lookup"><span data-stu-id="fef40-115">The filter graph manager supports **IGraphConfig**.</span></span> <span data-ttu-id="fef40-116">Para el parámetro *hStopEvent* , cree un evento de restablecimiento manual.</span><span class="sxs-lookup"><span data-stu-id="fef40-116">For the *hStopEvent* parameter, create a manual-reset event.</span></span> <span data-ttu-id="fef40-117">Cuando el filtro salga del gráfico de filtros, vuelva a llamar a este método con **null** para ambos parámetros.</span><span class="sxs-lookup"><span data-stu-id="fef40-117">When the filter leaves the filter graph, call this method again with **NULL** for both parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="fef40-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fef40-118">Requirements</span></span>



| <span data-ttu-id="fef40-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fef40-119">Requirement</span></span> | <span data-ttu-id="fef40-120">Value</span><span class="sxs-lookup"><span data-stu-id="fef40-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef40-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fef40-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fef40-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fef40-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fef40-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fef40-123">Library</span></span><br/> | <dl> <span data-ttu-id="fef40-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fef40-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef40-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fef40-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef40-126">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="fef40-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




