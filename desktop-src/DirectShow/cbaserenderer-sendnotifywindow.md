---
description: El método SendNotifyWindow notifica el filtro de nivel superior del identificador de la ventana de vídeo.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Método CBaseRenderer. SendNotifyWindow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660384"
---
# <a name="cbaserenderersendnotifywindow-method"></a><span data-ttu-id="81c17-103">CBaseRenderer. SendNotifyWindow, método</span><span class="sxs-lookup"><span data-stu-id="81c17-103">CBaseRenderer.SendNotifyWindow method</span></span>

<span data-ttu-id="81c17-104">El `SendNotifyWindow` método notifica el filtro de nivel superior del identificador de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="81c17-104">The `SendNotifyWindow` method notifies the upstream filter of the video window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c17-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81c17-105">Syntax</span></span>


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="81c17-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81c17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81c17-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="81c17-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="81c17-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de salida del filtro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="81c17-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the upstream filter's output pin.</span></span>

</dd> <dt>

<span data-ttu-id="81c17-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="81c17-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="81c17-110">Identificador de la ventana de vídeo o **null**.</span><span class="sxs-lookup"><span data-stu-id="81c17-110">Handle to the video window, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81c17-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81c17-111">Return value</span></span>

<span data-ttu-id="81c17-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="81c17-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81c17-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81c17-113">Remarks</span></span>

<span data-ttu-id="81c17-114">Si el PIN de salida del filtro de nivel superior admite la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , este método lo envía al código de evento de la [**ventana de \_ notificación \_ de EC**](ec-notify-window.md) junto con el identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="81c17-114">If the output pin of the upstream filter supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, this method sends it the [**EC\_NOTIFY\_WINDOW**](ec-notify-window.md) event code along with the window handle.</span></span>

<span data-ttu-id="81c17-115">Los representadores de vídeo pueden invalidar sus métodos [**CBaseRenderer:: CompleteConnect**](cbaserenderer-completeconnect.md) para llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="81c17-115">Video renderers can override their [**CBaseRenderer::CompleteConnect**](cbaserenderer-completeconnect.md) methods to call this method.</span></span> <span data-ttu-id="81c17-116">Proporciona un mecanismo para informar del filtro de nivel superior del identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="81c17-116">It provides a mechanism for informing the upstream filter of the window handle.</span></span> <span data-ttu-id="81c17-117">Si lo hace, invalide también el método [**CBaseRenderer:: BreakConnect**](cbaserenderer-breakconnect.md) y llame a `SendNotifyWindow` con un identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="81c17-117">If you do this, override the [**CBaseRenderer::BreakConnect**](cbaserenderer-breakconnect.md) method as well, and call `SendNotifyWindow` with a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="81c17-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81c17-118">Requirements</span></span>



| <span data-ttu-id="81c17-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="81c17-119">Requirement</span></span> | <span data-ttu-id="81c17-120">Value</span><span class="sxs-lookup"><span data-stu-id="81c17-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81c17-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81c17-121">Header</span></span><br/>  | <dl> <span data-ttu-id="81c17-122"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81c17-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81c17-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81c17-123">Library</span></span><br/> | <dl> <span data-ttu-id="81c17-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="81c17-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81c17-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="81c17-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81c17-126">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="81c17-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




