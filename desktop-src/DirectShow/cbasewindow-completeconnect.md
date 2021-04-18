---
description: El método CompleteConnect notifica a la ventana que se ha conectado el PIN de entrada del representador.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Método CBaseWindow. CompleteConnect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679091"
---
# <a name="cbasewindowcompleteconnect-method"></a><span data-ttu-id="c4c66-103">CBaseWindow. CompleteConnect, método</span><span class="sxs-lookup"><span data-stu-id="c4c66-103">CBaseWindow.CompleteConnect method</span></span>

<span data-ttu-id="c4c66-104">El `CompleteConnect` método notifica a la ventana que el PIN de entrada del representador se ha conectado.</span><span class="sxs-lookup"><span data-stu-id="c4c66-104">The `CompleteConnect` method notifies the window that the renderer's input pin has been connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c66-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4c66-105">Syntax</span></span>


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a><span data-ttu-id="c4c66-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4c66-106">Parameters</span></span>

<span data-ttu-id="c4c66-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c4c66-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4c66-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4c66-108">Return value</span></span>

<span data-ttu-id="c4c66-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="c4c66-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c66-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4c66-110">Remarks</span></span>

<span data-ttu-id="c4c66-111">Este método restablece la marca de activación de la ventana ([**CBaseWindow:: m \_ bActivated**](cbasewindow-m-bactivated.md)) en **false**.</span><span class="sxs-lookup"><span data-stu-id="c4c66-111">This method resets the window activation flag ([**CBaseWindow::m\_bActivated**](cbasewindow-m-bactivated.md)) to **FALSE**.</span></span> <span data-ttu-id="c4c66-112">Cuando un representador de vídeo completa una conexión de PIN, puede llamar al método [**CBaseWindow:: ActivateWindow**](cbasewindow-activatewindow.md) para establecer el tamaño y la posición de la ventana.</span><span class="sxs-lookup"><span data-stu-id="c4c66-112">When a video renderer completes a pin connection, it might call the [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) method to set the window's size and position.</span></span> <span data-ttu-id="c4c66-113">Para forzar que **ActivateWindow** vuelva a calcular estos atributos, primero llame al `CompleteConnect` método.</span><span class="sxs-lookup"><span data-stu-id="c4c66-113">To force **ActivateWindow** to recalculate these attributes, first call the `CompleteConnect` method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c66-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4c66-114">Requirements</span></span>



| <span data-ttu-id="c4c66-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4c66-115">Requirement</span></span> | <span data-ttu-id="c4c66-116">Value</span><span class="sxs-lookup"><span data-stu-id="c4c66-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c66-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4c66-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c4c66-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c66-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c4c66-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4c66-119">Library</span></span><br/> | <dl> <span data-ttu-id="c4c66-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c66-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c66-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4c66-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c66-122">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="c4c66-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




