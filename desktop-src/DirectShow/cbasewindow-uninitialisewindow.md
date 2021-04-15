---
description: El método UninitialiseWindow libera los recursos de la ventana.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Método CBaseWindow. UninitialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661322"
---
# <a name="cbasewindowuninitialisewindow-method"></a><span data-ttu-id="9cbce-103">CBaseWindow. UninitialiseWindow, método</span><span class="sxs-lookup"><span data-stu-id="9cbce-103">CBaseWindow.UninitialiseWindow method</span></span>

<span data-ttu-id="9cbce-104">El `UninitialiseWindow` método libera los recursos de la ventana.</span><span class="sxs-lookup"><span data-stu-id="9cbce-104">The `UninitialiseWindow` method releases the window's resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cbce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cbce-105">Syntax</span></span>


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a><span data-ttu-id="9cbce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9cbce-106">Parameters</span></span>

<span data-ttu-id="9cbce-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9cbce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9cbce-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9cbce-108">Return value</span></span>

<span data-ttu-id="9cbce-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="9cbce-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cbce-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cbce-110">Remarks</span></span>

<span data-ttu-id="9cbce-111">Este método libera los recursos adquiridos por el método [**CBaseWindow:: InitialiseWindow**](cbasewindow-initialisewindow.md) .</span><span class="sxs-lookup"><span data-stu-id="9cbce-111">This method frees resources that were acquired by the [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md) method.</span></span> <span data-ttu-id="9cbce-112">El método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="9cbce-112">The [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cbce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cbce-113">Requirements</span></span>



| <span data-ttu-id="9cbce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cbce-114">Requirement</span></span> | <span data-ttu-id="9cbce-115">Value</span><span class="sxs-lookup"><span data-stu-id="9cbce-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbce-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cbce-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9cbce-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cbce-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9cbce-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cbce-118">Library</span></span><br/> | <dl> <span data-ttu-id="9cbce-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9cbce-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cbce-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cbce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cbce-121">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="9cbce-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




