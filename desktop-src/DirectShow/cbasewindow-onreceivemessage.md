---
description: El método OnReceiveMessage controla los mensajes de ventana.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Método CBaseWindow. OnReceiveMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660315"
---
# <a name="cbasewindowonreceivemessage-method"></a><span data-ttu-id="f9944-103">CBaseWindow. OnReceiveMessage, método</span><span class="sxs-lookup"><span data-stu-id="f9944-103">CBaseWindow.OnReceiveMessage method</span></span>

<span data-ttu-id="f9944-104">El `OnReceiveMessage` método controla los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="f9944-104">The `OnReceiveMessage` method handles window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9944-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9944-105">Syntax</span></span>


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="f9944-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9944-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9944-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="f9944-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f9944-108">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f9944-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="f9944-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="f9944-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f9944-110">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9944-110">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f9944-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9944-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9944-112">Primer parámetro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9944-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f9944-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9944-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9944-114">Segundo parámetro del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9944-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9944-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9944-115">Return value</span></span>

<span data-ttu-id="f9944-116">Devuelve 0 si se procesó el mensaje o 1 si no se procesó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9944-116">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9944-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9944-117">Remarks</span></span>

<span data-ttu-id="f9944-118">La clase base controla los siguientes mensajes:</span><span class="sxs-lookup"><span data-stu-id="f9944-118">The base class handles the following messages:</span></span>

-   <span data-ttu-id="f9944-119">cierre de WM \_</span><span class="sxs-lookup"><span data-stu-id="f9944-119">WM\_CLOSE</span></span>
-   <span data-ttu-id="f9944-120">movimiento de WM \_</span><span class="sxs-lookup"><span data-stu-id="f9944-120">WM\_MOVE</span></span>
-   <span data-ttu-id="f9944-121">PALETTECHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="f9944-121">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="f9944-122">QUERYNEWPALETTE de WM \_</span><span class="sxs-lookup"><span data-stu-id="f9944-122">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="f9944-123">tamaño de WM \_</span><span class="sxs-lookup"><span data-stu-id="f9944-123">WM\_SIZE</span></span>
-   <span data-ttu-id="f9944-124">SYSCOLORCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="f9944-124">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="f9944-125">Una clase derivada puede invalidar este método para controlar otros mensajes.</span><span class="sxs-lookup"><span data-stu-id="f9944-125">A derived class can override this method to handle other messages.</span></span> <span data-ttu-id="f9944-126">La clase derivada debe llamar al método de clase base para controlar los mensajes que la clase derivada omite.</span><span class="sxs-lookup"><span data-stu-id="f9944-126">The derived class should call the base class method to handle any messages that the derived class ignores.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9944-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9944-127">Requirements</span></span>



| <span data-ttu-id="f9944-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9944-128">Requirement</span></span> | <span data-ttu-id="f9944-129">Value</span><span class="sxs-lookup"><span data-stu-id="f9944-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9944-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9944-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f9944-131"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9944-131"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f9944-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9944-132">Library</span></span><br/> | <dl> <span data-ttu-id="f9944-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f9944-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9944-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9944-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9944-135">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="f9944-135">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




