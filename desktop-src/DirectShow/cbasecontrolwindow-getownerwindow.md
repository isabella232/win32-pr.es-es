---
description: El método GetOwnerWindow recupera el identificador de la ventana propietaria, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Método CBaseControlWindow. GetOwnerWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660597"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a><span data-ttu-id="5c89a-103">CBaseControlWindow. GetOwnerWindow, método</span><span class="sxs-lookup"><span data-stu-id="5c89a-103">CBaseControlWindow.GetOwnerWindow method</span></span>

<span data-ttu-id="5c89a-104">El `GetOwnerWindow` método recupera el identificador de la ventana propietaria, **m \_ hwndOwner**.</span><span class="sxs-lookup"><span data-stu-id="5c89a-104">The `GetOwnerWindow` method retrieves the owning window handle, **m\_hwndOwner**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c89a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c89a-105">Syntax</span></span>


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a><span data-ttu-id="5c89a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c89a-106">Parameters</span></span>

<span data-ttu-id="5c89a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5c89a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c89a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c89a-108">Return value</span></span>

<span data-ttu-id="5c89a-109">Devuelve la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="5c89a-109">Returns the owner window.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c89a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c89a-110">Remarks</span></span>

<span data-ttu-id="5c89a-111">Recupera la ventana propietaria sin llamar al método de interfaz.</span><span class="sxs-lookup"><span data-stu-id="5c89a-111">Retrieves the owning window without calling the interface method.</span></span> <span data-ttu-id="5c89a-112">Use esta función miembro en lugar de [**CBaseControlWindow:: get \_ Owner**](cbasecontrolwindow-get-owner.md), a menos que llame a esto externamente a través del método [**IVideoWindow:: get \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .</span><span class="sxs-lookup"><span data-stu-id="5c89a-112">Use this member function instead of [**CBaseControlWindow::get\_Owner**](cbasecontrolwindow-get-owner.md), unless you are calling this externally through the [**IVideoWindow::get\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c89a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c89a-113">Requirements</span></span>



| <span data-ttu-id="5c89a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c89a-114">Requirement</span></span> | <span data-ttu-id="5c89a-115">Value</span><span class="sxs-lookup"><span data-stu-id="5c89a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c89a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c89a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5c89a-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c89a-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5c89a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c89a-118">Library</span></span><br/> | <dl> <span data-ttu-id="5c89a-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5c89a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c89a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c89a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c89a-121">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="5c89a-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




