---
description: El método NotifyOwnerMessage pasa mensajes específicos a la ventana de vídeo.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Método CBaseControlWindow. NotifyOwnerMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661386"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a><span data-ttu-id="8f0d4-103">CBaseControlWindow. NotifyOwnerMessage, método</span><span class="sxs-lookup"><span data-stu-id="8f0d4-103">CBaseControlWindow.NotifyOwnerMessage method</span></span>

<span data-ttu-id="8f0d4-104">El `NotifyOwnerMessage` método pasa mensajes específicos a la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-104">The `NotifyOwnerMessage` method passes along specific messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f0d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f0d4-105">Syntax</span></span>


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a><span data-ttu-id="8f0d4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f0d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f0d4-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="8f0d4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8f0d4-108">Identificador de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-108">Handle to the video window.</span></span>

</dd> <dt>

<span data-ttu-id="8f0d4-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="8f0d4-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8f0d4-110">Detalles del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-110">Message details.</span></span>

</dd> <dt>

<span data-ttu-id="8f0d4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f0d4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f0d4-112">Primer parámetro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8f0d4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f0d4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f0d4-114">Segundo parámetro del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f0d4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f0d4-115">Return value</span></span>

<span data-ttu-id="8f0d4-116">NO devuelve ningún \_ error.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-116">Returns NO\_ERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f0d4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f0d4-117">Remarks</span></span>

<span data-ttu-id="8f0d4-118">Cuando la ventana de vídeo es un elemento secundario de otra ventana, no recibe ciertos mensajes de ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-118">When the video window is a child of another window, it does not receive certain top-level window messages.</span></span> <span data-ttu-id="8f0d4-119">Estos mensajes pueden ser valiosos para un representador, porque podrían afectar a su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-119">These messages can be valuable to a renderer, because they could affect its behavior.</span></span> <span data-ttu-id="8f0d4-120">`NotifyOwnerMessage` pasa cualquiera de los mensajes siguientes a la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-120">`NotifyOwnerMessage` passes any of the following messages to the video window.</span></span>

-   <span data-ttu-id="8f0d4-121">ACTIVATEAPP de WM \_</span><span class="sxs-lookup"><span data-stu-id="8f0d4-121">WM\_ACTIVATEAPP</span></span>
-   <span data-ttu-id="8f0d4-122">DEVMODECHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="8f0d4-122">WM\_DEVMODECHANGE</span></span>
-   <span data-ttu-id="8f0d4-123">DISPLAYCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="8f0d4-123">WM\_DISPLAYCHANGE</span></span>
-   <span data-ttu-id="8f0d4-124">PALETTECHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="8f0d4-124">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="8f0d4-125">PALETTEISCHANGING de WM \_</span><span class="sxs-lookup"><span data-stu-id="8f0d4-125">WM\_PALETTEISCHANGING</span></span>
-   <span data-ttu-id="8f0d4-126">QUERYNEWPALETTE de WM \_</span><span class="sxs-lookup"><span data-stu-id="8f0d4-126">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="8f0d4-127">SYSCOLORCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="8f0d4-127">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="8f0d4-128">Puede solicitar que el distribuidor de complementos de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) haga que una ventana se convierta en un elemento secundario de otra ventana.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-128">You can request that the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor (PID) make a window become a child of another window.</span></span> <span data-ttu-id="8f0d4-129">Cuando esto ocurre, el PID buscará determinados mensajes que puedan enviarse a la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-129">When this occurs, the PID will look for certain messages that might be sent to the owning window.</span></span> <span data-ttu-id="8f0d4-130">A continuación, el PID reenviará esos mensajes a la ventana de propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-130">The PID will then forward those messages to the owned window.</span></span> <span data-ttu-id="8f0d4-131">El procesamiento predeterminado de los mensajes es enviarlos al procedimiento de ventana propiedad de forma sincrónica mediante una llamada a la función **SendMessage** de Win32.</span><span class="sxs-lookup"><span data-stu-id="8f0d4-131">The default processing for the messages is to send them to the owned window procedure synchronously by calling the Win32 **SendMessage** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f0d4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f0d4-132">Requirements</span></span>



| <span data-ttu-id="8f0d4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f0d4-133">Requirement</span></span> | <span data-ttu-id="8f0d4-134">Value</span><span class="sxs-lookup"><span data-stu-id="8f0d4-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f0d4-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f0d4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8f0d4-136"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f0d4-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8f0d4-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f0d4-137">Library</span></span><br/> | <dl> <span data-ttu-id="8f0d4-138"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8f0d4-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f0d4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f0d4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f0d4-140">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="8f0d4-140">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




