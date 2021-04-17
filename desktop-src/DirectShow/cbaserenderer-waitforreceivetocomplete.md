---
description: 'El método WaitForReceiveToComplete espera a que se complete el método CBaseRenderer:: Receive.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Método CBaseRenderer. WaitForReceiveToComplete (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670343"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a><span data-ttu-id="dae91-103">CBaseRenderer. WaitForReceiveToComplete, método</span><span class="sxs-lookup"><span data-stu-id="dae91-103">CBaseRenderer.WaitForReceiveToComplete method</span></span>

<span data-ttu-id="dae91-104">El `WaitForReceiveToComplete` método espera a que se complete el método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="dae91-104">The `WaitForReceiveToComplete` method waits for the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method to complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae91-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dae91-105">Syntax</span></span>


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a><span data-ttu-id="dae91-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dae91-106">Parameters</span></span>

<span data-ttu-id="dae91-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dae91-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dae91-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dae91-108">Return value</span></span>

<span data-ttu-id="dae91-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dae91-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dae91-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dae91-110">Remarks</span></span>

<span data-ttu-id="dae91-111">Los métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) y [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) llaman a este método para sincronizar el cambio de estado con el método **Receive** .</span><span class="sxs-lookup"><span data-stu-id="dae91-111">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method to synchronize the state change with the **Receive** method.</span></span>

<span data-ttu-id="dae91-112">En concreto, este método envía los mensajes mientras espera a que la marca [**CBaseRenderer:: m \_ bInReceive**](cbaserenderer-m-binreceive.md) se convierta en **false**.</span><span class="sxs-lookup"><span data-stu-id="dae91-112">Specifically, this method dispatches messages while it waits for the [**CBaseRenderer::m\_bInReceive**](cbaserenderer-m-binreceive.md) flag to become **FALSE**.</span></span> <span data-ttu-id="dae91-113">La marca se convierte en **true** en el método [**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md) y vuelve a cambiar a **false** después de que el método **Receive** llame al método [**CBaseRenderer::P reparerender**](cbaserenderer-preparerender.md) .</span><span class="sxs-lookup"><span data-stu-id="dae91-113">The flag becomes **TRUE** in the [**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md) method and switches back to **FALSE** after the **Receive** method calls the [**CBaseRenderer::PrepareRender**](cbaserenderer-preparerender.md) method.</span></span> <span data-ttu-id="dae91-114">La clase derivada puede usar **PrepareRender** para establecer la paleta.</span><span class="sxs-lookup"><span data-stu-id="dae91-114">The derived class can use **PrepareRender** to set the palette.</span></span> <span data-ttu-id="dae91-115">Esperar a que se complete **PrepareRender** se asegura de que los mensajes de cambio de paleta se envíen antes de que se produzca el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="dae91-115">Waiting for **PrepareRender** to complete ensures that palette-change messages are dispatched before the state change occurs.</span></span> <span data-ttu-id="dae91-116">Esto evita un posible interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="dae91-116">This avoids a potential deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae91-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae91-117">Requirements</span></span>



| <span data-ttu-id="dae91-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae91-118">Requirement</span></span> | <span data-ttu-id="dae91-119">Value</span><span class="sxs-lookup"><span data-stu-id="dae91-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae91-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dae91-120">Header</span></span><br/>  | <dl> <span data-ttu-id="dae91-121"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dae91-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dae91-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dae91-122">Library</span></span><br/> | <dl> <span data-ttu-id="dae91-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dae91-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae91-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="dae91-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae91-125">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="dae91-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




