---
description: El método ActivateWindow ajusta el tamaño de la ventana según los requisitos de la clase derivada.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Método CBaseWindow. ActivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680653"
---
# <a name="cbasewindowactivatewindow-method"></a><span data-ttu-id="7731d-103">CBaseWindow. ActivateWindow, método</span><span class="sxs-lookup"><span data-stu-id="7731d-103">CBaseWindow.ActivateWindow method</span></span>

<span data-ttu-id="7731d-104">El `ActivateWindow` método ajusta el tamaño de la ventana según los requisitos de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="7731d-104">The `ActivateWindow` method sizes the window according to the requirements of the derived class.</span></span>

## <a name="syntax"></a><span data-ttu-id="7731d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7731d-105">Syntax</span></span>


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="7731d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7731d-106">Parameters</span></span>

<span data-ttu-id="7731d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7731d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7731d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7731d-108">Return value</span></span>

<span data-ttu-id="7731d-109">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7731d-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7731d-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7731d-110">Return code</span></span>                                                                             | <span data-ttu-id="7731d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7731d-111">Description</span></span>                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="7731d-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7731d-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="7731d-113">La ventana ya estaba activada.</span><span class="sxs-lookup"><span data-stu-id="7731d-113">Window was already activated.</span></span><br/> |
| <dl> <span data-ttu-id="7731d-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7731d-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="7731d-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7731d-115">Success.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="7731d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7731d-116">Remarks</span></span>

<span data-ttu-id="7731d-117">Estos métodos llaman al método [**CBaseWindow:: GetDefaultRect**](cbasewindow-getdefaultrect.md) para determinar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7731d-117">This methods calls the [**CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) method to determine the window size.</span></span> <span data-ttu-id="7731d-118">La clase derivada debe invalidar **GetDefaultRect** para devolver el tamaño de las imágenes que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="7731d-118">The derived class should override **GetDefaultRect** to return the size of the images that will be displayed.</span></span>

<span data-ttu-id="7731d-119">Si la ventana ya está activa, al llamar a `ActivateWindow` se mueve la ventana a la parte superior del orden Z, pero no se cambia el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7731d-119">If the window is already active, calling `ActivateWindow` moves the window to the top of the Z order, but does not resize the window.</span></span> <span data-ttu-id="7731d-120">Lo mismo sucede si la ventana tiene un elemento primario.</span><span class="sxs-lookup"><span data-stu-id="7731d-120">The same is true if the window has a parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="7731d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7731d-121">Requirements</span></span>



| <span data-ttu-id="7731d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7731d-122">Requirement</span></span> | <span data-ttu-id="7731d-123">Value</span><span class="sxs-lookup"><span data-stu-id="7731d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7731d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7731d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7731d-125"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7731d-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7731d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7731d-126">Library</span></span><br/> | <dl> <span data-ttu-id="7731d-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7731d-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7731d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7731d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7731d-129">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="7731d-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




