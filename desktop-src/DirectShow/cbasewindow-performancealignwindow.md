---
description: El método PerformanceAlignWindow alinea la posición de la ventana con los límites DWORD para obtener el máximo rendimiento.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Método CBaseWindow. PerformanceAlignWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681036"
---
# <a name="cbasewindowperformancealignwindow-method"></a><span data-ttu-id="26855-103">CBaseWindow. PerformanceAlignWindow, método</span><span class="sxs-lookup"><span data-stu-id="26855-103">CBaseWindow.PerformanceAlignWindow method</span></span>

<span data-ttu-id="26855-104">El `PerformanceAlignWindow` método alinea la posición de la ventana con los límites **DWORD** para obtener el máximo rendimiento.</span><span class="sxs-lookup"><span data-stu-id="26855-104">The `PerformanceAlignWindow` method aligns the window position to **DWORD** boundaries, for maximum performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="26855-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26855-105">Syntax</span></span>


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a><span data-ttu-id="26855-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26855-106">Parameters</span></span>

<span data-ttu-id="26855-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="26855-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26855-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26855-108">Return value</span></span>

<span data-ttu-id="26855-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="26855-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="26855-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26855-110">Remarks</span></span>

<span data-ttu-id="26855-111">Este método alinea los bordes izquierdo y superior de la ventana con los límites de DWORD, lo que puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="26855-111">This method aligns the left and top edges of the window to DWORD boundaries, which can improve performance.</span></span> <span data-ttu-id="26855-112">Si la ventana tiene un elemento primario, el método devuelve S \_ correcto, pero realiza la alineación.</span><span class="sxs-lookup"><span data-stu-id="26855-112">If the window has a parent, the method returns S\_OK but does perform the alignment.</span></span>

## <a name="requirements"></a><span data-ttu-id="26855-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26855-113">Requirements</span></span>



| <span data-ttu-id="26855-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="26855-114">Requirement</span></span> | <span data-ttu-id="26855-115">Value</span><span class="sxs-lookup"><span data-stu-id="26855-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26855-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26855-116">Header</span></span><br/>  | <dl> <span data-ttu-id="26855-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26855-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="26855-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26855-118">Library</span></span><br/> | <dl> <span data-ttu-id="26855-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="26855-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26855-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="26855-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26855-121">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="26855-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




