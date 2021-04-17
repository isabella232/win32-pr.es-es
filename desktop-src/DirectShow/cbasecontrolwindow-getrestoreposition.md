---
description: El método GetRestorePosition recupera la posición en la que se restaurará la ventana cuando no esté maximizada o minimizada.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Método CBaseControlWindow. GetRestorePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660595"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a><span data-ttu-id="6b7df-103">CBaseControlWindow. GetRestorePosition, método</span><span class="sxs-lookup"><span data-stu-id="6b7df-103">CBaseControlWindow.GetRestorePosition method</span></span>

<span data-ttu-id="6b7df-104">El `GetRestorePosition` método recupera la posición en la que se restaurará la ventana cuando no esté maximizada o minimizada.</span><span class="sxs-lookup"><span data-stu-id="6b7df-104">The `GetRestorePosition` method retrieves the position to which the window will be restored when it is not maximized or minimized.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b7df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b7df-105">Syntax</span></span>


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="6b7df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b7df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b7df-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="6b7df-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7df-108">Puntero al valor de la coordenada izquierda.</span><span class="sxs-lookup"><span data-stu-id="6b7df-108">Pointer to the value for leftmost coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6b7df-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="6b7df-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7df-110">Puntero en el valor de la parte superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6b7df-110">Pointer to the value for top of the window.</span></span>

</dd> <dt>

<span data-ttu-id="6b7df-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="6b7df-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7df-112">Puntero al valor del ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6b7df-112">Pointer to the value for width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="6b7df-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="6b7df-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7df-114">Puntero al valor para el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6b7df-114">Pointer to the value for height of window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b7df-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b7df-115">Return value</span></span>

<span data-ttu-id="6b7df-116">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b7df-116">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b7df-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b7df-117">Remarks</span></span>

<span data-ttu-id="6b7df-118">Es igual que los valores devueltos por la función [**CBaseControlWindow:: GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) cuando la ventana no está maximizada ni minimizada.</span><span class="sxs-lookup"><span data-stu-id="6b7df-118">This is the same as the values returned by the [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) function when the window is neither maximized nor minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7df-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b7df-119">Requirements</span></span>



| <span data-ttu-id="6b7df-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b7df-120">Requirement</span></span> | <span data-ttu-id="6b7df-121">Value</span><span class="sxs-lookup"><span data-stu-id="6b7df-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7df-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b7df-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6b7df-123"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b7df-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6b7df-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b7df-124">Library</span></span><br/> | <dl> <span data-ttu-id="6b7df-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6b7df-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b7df-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b7df-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b7df-127">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="6b7df-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




