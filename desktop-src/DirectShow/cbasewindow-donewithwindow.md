---
description: El método DoneWithWindow destruye la ventana.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Método CBaseWindow. DoneWithWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660230"
---
# <a name="cbasewindowdonewithwindow-method"></a><span data-ttu-id="1fc5c-103">CBaseWindow. DoneWithWindow, método</span><span class="sxs-lookup"><span data-stu-id="1fc5c-103">CBaseWindow.DoneWithWindow method</span></span>

<span data-ttu-id="1fc5c-104">El `DoneWithWindow` método destruye la ventana.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-104">The `DoneWithWindow` method destroys the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc5c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fc5c-105">Syntax</span></span>


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a><span data-ttu-id="1fc5c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fc5c-106">Parameters</span></span>

<span data-ttu-id="1fc5c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1fc5c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fc5c-108">Return value</span></span>

<span data-ttu-id="1fc5c-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc5c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fc5c-110">Remarks</span></span>

<span data-ttu-id="1fc5c-111">Llame a este método desde el método de destructor del objeto derivado.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-111">Call this method from the derived object's destructor method.</span></span>

<span data-ttu-id="1fc5c-112">Si se llama a este método desde el mismo subproceso que creó la ventana, el método realiza las acciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="1fc5c-112">If this method is called from the same thread that created the window, the method performs the following actions:</span></span>

-   <span data-ttu-id="1fc5c-113">Llama al método [**CBaseWindow:: InactivateWindow**](cbasewindow-inactivatewindow.md) , que desactiva la ventana.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-113">Calls the [**CBaseWindow::InactivateWindow**](cbasewindow-inactivatewindow.md) method, which deactivates the window.</span></span>
-   <span data-ttu-id="1fc5c-114">Llama al método [**CBaseWindow:: UninitialiseWindow**](cbasewindow-uninitialisewindow.md) , que libera los recursos utilizados por la ventana.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-114">Calls the [**CBaseWindow::UninitialiseWindow**](cbasewindow-uninitialisewindow.md) method, which releases resources used by the window.</span></span>
-   <span data-ttu-id="1fc5c-115">Destruye la ventana.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-115">Destroys the window.</span></span>

<span data-ttu-id="1fc5c-116">Si el subproceso que realiza la llamada `DoneWithWindow` no es el subproceso que creó la ventana, el método envía un mensaje privado "Destroy" a la ventana.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-116">If the thread calling `DoneWithWindow` is not the thread that created the window, the method sends a private "destroy" message to the window.</span></span> <span data-ttu-id="1fc5c-117">Cuando la ventana recibe este mensaje, llama a `DoneWithWindow` sí mismo.</span><span class="sxs-lookup"><span data-stu-id="1fc5c-117">When the window receives this message, it calls `DoneWithWindow` on itself.</span></span> <span data-ttu-id="1fc5c-118">(Si [**CBaseWindow:: m \_ BDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) es **true**, la ventana envía el mensaje).</span><span class="sxs-lookup"><span data-stu-id="1fc5c-118">(If [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) is **TRUE**, the window posts the message.)</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc5c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc5c-119">Requirements</span></span>



| <span data-ttu-id="1fc5c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc5c-120">Requirement</span></span> | <span data-ttu-id="1fc5c-121">Value</span><span class="sxs-lookup"><span data-stu-id="1fc5c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc5c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fc5c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1fc5c-123"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fc5c-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1fc5c-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fc5c-124">Library</span></span><br/> | <dl> <span data-ttu-id="1fc5c-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1fc5c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc5c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fc5c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc5c-127">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="1fc5c-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




