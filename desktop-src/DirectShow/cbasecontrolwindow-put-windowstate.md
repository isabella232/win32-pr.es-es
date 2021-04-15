---
description: El \_ método de WindowState Put establece el estado de la ventana.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: Método CBaseControlWindow.put_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661341"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a><span data-ttu-id="e2759-103">CBaseControlWindow. put ( \_ método de WindowState)</span><span class="sxs-lookup"><span data-stu-id="e2759-103">CBaseControlWindow.put\_WindowState method</span></span>

<span data-ttu-id="e2759-104">El `put_WindowState` método establece el estado de la ventana.</span><span class="sxs-lookup"><span data-stu-id="e2759-104">The `put_WindowState` method sets the window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2759-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2759-105">Syntax</span></span>


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a><span data-ttu-id="e2759-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2759-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2759-107">*WindowState*</span><span class="sxs-lookup"><span data-stu-id="e2759-107">*WindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="e2759-108">Nuevo estado de ventana.</span><span class="sxs-lookup"><span data-stu-id="e2759-108">New window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2759-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2759-109">Return value</span></span>

<span data-ttu-id="e2759-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e2759-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2759-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2759-111">Remarks</span></span>

<span data-ttu-id="e2759-112">Esta función miembro toma los mismos parámetros que la función **ShowWindow** de Microsoft Win32 (por ejemplo, WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE y WS \_ SHOWMAXIMIZED).</span><span class="sxs-lookup"><span data-stu-id="e2759-112">This member function takes the same parameters as the Microsoft Win32 **ShowWindow** function (for example, WS\_SHOWNORMAL, WS\_SHOWMINNOACTIVATE, and WS\_SHOWMAXIMIZED).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2759-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2759-113">Requirements</span></span>



| <span data-ttu-id="e2759-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2759-114">Requirement</span></span> | <span data-ttu-id="e2759-115">Value</span><span class="sxs-lookup"><span data-stu-id="e2759-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2759-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2759-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e2759-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2759-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e2759-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2759-118">Library</span></span><br/> | <dl> <span data-ttu-id="e2759-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e2759-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2759-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2759-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2759-121">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="e2759-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




