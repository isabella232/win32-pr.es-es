---
description: El método PrepareWindow crea la ventana.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Método CBaseWindow. PrepareWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661232"
---
# <a name="cbasewindowpreparewindow-method"></a><span data-ttu-id="6cd55-103">CBaseWindow. PrepareWindow, método</span><span class="sxs-lookup"><span data-stu-id="6cd55-103">CBaseWindow.PrepareWindow method</span></span>

<span data-ttu-id="6cd55-104">El `PrepareWindow` método crea la ventana.</span><span class="sxs-lookup"><span data-stu-id="6cd55-104">The `PrepareWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cd55-105">Syntax</span></span>


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a><span data-ttu-id="6cd55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cd55-106">Parameters</span></span>

<span data-ttu-id="6cd55-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6cd55-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cd55-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cd55-108">Return value</span></span>

<span data-ttu-id="6cd55-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6cd55-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6cd55-110">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6cd55-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6cd55-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6cd55-111">Return code</span></span>                                                                            | <span data-ttu-id="6cd55-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cd55-112">Description</span></span>         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="6cd55-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6cd55-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="6cd55-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6cd55-114">Success.</span></span><br/> |
| <dl> <span data-ttu-id="6cd55-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="6cd55-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="6cd55-116">Error.</span><span class="sxs-lookup"><span data-stu-id="6cd55-116">Failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6cd55-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cd55-117">Remarks</span></span>

<span data-ttu-id="6cd55-118">Llame a este método después de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="6cd55-118">Call this method after creating the object.</span></span> <span data-ttu-id="6cd55-119">Este método realiza una contabilidad inicial y, a continuación, llama al método [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) para crear la ventana.</span><span class="sxs-lookup"><span data-stu-id="6cd55-119">This method performs some initial bookkeeping and then calls the [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method to create the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd55-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cd55-120">Requirements</span></span>



| <span data-ttu-id="6cd55-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cd55-121">Requirement</span></span> | <span data-ttu-id="6cd55-122">Value</span><span class="sxs-lookup"><span data-stu-id="6cd55-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd55-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cd55-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6cd55-124"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cd55-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6cd55-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cd55-125">Library</span></span><br/> | <dl> <span data-ttu-id="6cd55-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6cd55-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cd55-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cd55-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd55-128">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="6cd55-128">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




