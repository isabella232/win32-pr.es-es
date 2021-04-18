---
description: El método OnClose controla \_ los mensajes de cierre de WM.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Método CBaseWindow. OnClose (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660317"
---
# <a name="cbasewindowonclose-method"></a><span data-ttu-id="88f30-103">CBaseWindow. OnClose (método)</span><span class="sxs-lookup"><span data-stu-id="88f30-103">CBaseWindow.OnClose method</span></span>

<span data-ttu-id="88f30-104">El `OnClose` método controla \_ los mensajes de cierre de WM.</span><span class="sxs-lookup"><span data-stu-id="88f30-104">The `OnClose` method handles WM\_CLOSE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f30-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88f30-105">Syntax</span></span>


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a><span data-ttu-id="88f30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88f30-106">Parameters</span></span>

<span data-ttu-id="88f30-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="88f30-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88f30-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88f30-108">Return value</span></span>

<span data-ttu-id="88f30-109">Devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="88f30-109">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="88f30-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88f30-110">Remarks</span></span>

<span data-ttu-id="88f30-111">En la clase base, este método simplemente oculta la ventana.</span><span class="sxs-lookup"><span data-stu-id="88f30-111">In the base class, this method simply hides the window.</span></span> <span data-ttu-id="88f30-112">Normalmente, una clase derivada invalidará este método para que envíe también un evento [**\_ USERABORT de EC**](ec-userabort.md) .</span><span class="sxs-lookup"><span data-stu-id="88f30-112">Typically, a derived class will override this method so that it sends an [**EC\_USERABORT**](ec-userabort.md) event as well.</span></span> <span data-ttu-id="88f30-113">No invalide el método para destruir la ventana.</span><span class="sxs-lookup"><span data-stu-id="88f30-113">Do not override the method to destroy the window.</span></span> <span data-ttu-id="88f30-114">En su lugar, llame al método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) cuando se destruya el filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="88f30-114">Instead, call the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method when the owning filter is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="88f30-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88f30-115">Requirements</span></span>



| <span data-ttu-id="88f30-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="88f30-116">Requirement</span></span> | <span data-ttu-id="88f30-117">Value</span><span class="sxs-lookup"><span data-stu-id="88f30-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88f30-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88f30-118">Header</span></span><br/>  | <dl> <span data-ttu-id="88f30-119"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88f30-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88f30-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88f30-120">Library</span></span><br/> | <dl> <span data-ttu-id="88f30-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="88f30-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f30-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="88f30-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f30-123">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="88f30-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




