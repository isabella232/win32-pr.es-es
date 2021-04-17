---
description: El \_ método put MessageDrain establece la ventana para recibir los mensajes de ventana enviados al representador de vídeo.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Método CBaseControlWindow.put_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661146"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a><span data-ttu-id="348b0-103">CBaseControlWindow. put \_ MessageDrain (método)</span><span class="sxs-lookup"><span data-stu-id="348b0-103">CBaseControlWindow.put\_MessageDrain method</span></span>

<span data-ttu-id="348b0-104">El `put_MessageDrain` método establece la ventana para recibir los mensajes de ventana enviados al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="348b0-104">The `put_MessageDrain` method sets the window to receive window messages sent to the video renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="348b0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="348b0-105">Syntax</span></span>


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a><span data-ttu-id="348b0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="348b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="348b0-107">*Purga*</span><span class="sxs-lookup"><span data-stu-id="348b0-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="348b0-108">Ventana en la que se van a enviar mensajes.</span><span class="sxs-lookup"><span data-stu-id="348b0-108">Window to post messages to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="348b0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="348b0-109">Return value</span></span>

<span data-ttu-id="348b0-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="348b0-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="348b0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="348b0-111">Remarks</span></span>

<span data-ttu-id="348b0-112">Los mensajes enviados al filtro de representador de vídeo se pueden publicar en otra ventana.</span><span class="sxs-lookup"><span data-stu-id="348b0-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="348b0-113">Esta función miembro registra la ventana para recibir estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="348b0-113">This member function registers the window to receive these messages.</span></span> <span data-ttu-id="348b0-114">A diferencia de la función miembro [**CBaseControlWindow::p UT \_ Owner**](cbasecontrolwindow-put-owner.md) , esta función miembro no hace que la ventana de vídeo sea un elemento secundario de otra ventana.</span><span class="sxs-lookup"><span data-stu-id="348b0-114">Unlike the [**CBaseControlWindow::put\_Owner**](cbasecontrolwindow-put-owner.md) member function, this member function does not make the video window a child of another window.</span></span> <span data-ttu-id="348b0-115">Es especialmente útil para los representadores de vídeo de pantalla completa, que no pueden ser ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="348b0-115">It is particularly useful for full-screen video renderers, which cannot be child windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="348b0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="348b0-116">Requirements</span></span>



| <span data-ttu-id="348b0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="348b0-117">Requirement</span></span> | <span data-ttu-id="348b0-118">Value</span><span class="sxs-lookup"><span data-stu-id="348b0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="348b0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="348b0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="348b0-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="348b0-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="348b0-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="348b0-121">Library</span></span><br/> | <dl> <span data-ttu-id="348b0-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="348b0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="348b0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="348b0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="348b0-124">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="348b0-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




