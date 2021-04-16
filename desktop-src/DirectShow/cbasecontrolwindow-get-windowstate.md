---
description: El \_ método get WindowState recupera el estado actual de la ventana.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Método CBaseControlWindow.get_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671565"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a><span data-ttu-id="079f9-103">CBaseControlWindow. Get \_ WindowState (método)</span><span class="sxs-lookup"><span data-stu-id="079f9-103">CBaseControlWindow.get\_WindowState method</span></span>

<span data-ttu-id="079f9-104">El `get_WindowState` método recupera el estado actual de la ventana.</span><span class="sxs-lookup"><span data-stu-id="079f9-104">The `get_WindowState` method retrieves the current window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="079f9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="079f9-105">Syntax</span></span>


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a><span data-ttu-id="079f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="079f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="079f9-107">*pWindowState*</span><span class="sxs-lookup"><span data-stu-id="079f9-107">*pWindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="079f9-108">Puntero al estado de la ventana.</span><span class="sxs-lookup"><span data-stu-id="079f9-108">Pointer to the window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="079f9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="079f9-109">Return value</span></span>

<span data-ttu-id="079f9-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="079f9-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="079f9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="079f9-111">Remarks</span></span>

<span data-ttu-id="079f9-112">Esta función miembro devuelve un subconjunto de los parámetros de la función **ShowWindow** de Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="079f9-112">This member function returns a subset of the parameters of the Microsoft Win32 **ShowWindow** function.</span></span> <span data-ttu-id="079f9-113">En concreto, devuelve SW \_ Show y SW \_ Hide, dependiendo de la visibilidad actual de la ventana.</span><span class="sxs-lookup"><span data-stu-id="079f9-113">In particular, it returns SW\_SHOW and SW\_HIDE, depending on the current visibility of the window.</span></span> <span data-ttu-id="079f9-114">También devuelve SW \_ minimizar y SW \_ maximizar, dependiendo de si la ventana es un icono o está expandida.</span><span class="sxs-lookup"><span data-stu-id="079f9-114">It also returns SW\_MINIMIZE and SW\_MAXIMIZE, depending on whether the window is an icon or is expanded.</span></span>

## <a name="requirements"></a><span data-ttu-id="079f9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="079f9-115">Requirements</span></span>



| <span data-ttu-id="079f9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="079f9-116">Requirement</span></span> | <span data-ttu-id="079f9-117">Value</span><span class="sxs-lookup"><span data-stu-id="079f9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="079f9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="079f9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="079f9-119"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="079f9-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="079f9-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="079f9-120">Library</span></span><br/> | <dl> <span data-ttu-id="079f9-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="079f9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="079f9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="079f9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="079f9-123">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="079f9-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




