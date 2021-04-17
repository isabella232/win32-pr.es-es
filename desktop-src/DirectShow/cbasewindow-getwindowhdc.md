---
description: El método GetWindowHDC recupera un identificador para el contexto de dispositivo (DC) de la ventana.
ms.assetid: 35ee2a66-ee56-44dc-ad59-fd467bb4aa63
title: Método CBaseWindow. GetWindowHDC (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetWindowHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16c2502b3a9de587e91ff43ddc45a84ae08492db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660568"
---
# <a name="cbasewindowgetwindowhdc-method"></a><span data-ttu-id="81caa-103">CBaseWindow. GetWindowHDC, método</span><span class="sxs-lookup"><span data-stu-id="81caa-103">CBaseWindow.GetWindowHDC method</span></span>

<span data-ttu-id="81caa-104">El `GetWindowHDC` método recupera un identificador para el contexto de dispositivo (DC) de la ventana.</span><span class="sxs-lookup"><span data-stu-id="81caa-104">The `GetWindowHDC` method retrieves a handle to the window's device context (DC).</span></span>

## <a name="syntax"></a><span data-ttu-id="81caa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81caa-105">Syntax</span></span>


```C++
HDC GetWindowHDC();
```



## <a name="parameters"></a><span data-ttu-id="81caa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81caa-106">Parameters</span></span>

<span data-ttu-id="81caa-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="81caa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81caa-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81caa-108">Return value</span></span>

<span data-ttu-id="81caa-109">Devuelve un identificador para el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="81caa-109">Returns a handle to the DC.</span></span>

## <a name="requirements"></a><span data-ttu-id="81caa-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81caa-110">Requirements</span></span>



| <span data-ttu-id="81caa-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="81caa-111">Requirement</span></span> | <span data-ttu-id="81caa-112">Value</span><span class="sxs-lookup"><span data-stu-id="81caa-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81caa-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81caa-113">Header</span></span><br/>  | <dl> <span data-ttu-id="81caa-114"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81caa-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81caa-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81caa-115">Library</span></span><br/> | <dl> <span data-ttu-id="81caa-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="81caa-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81caa-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="81caa-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81caa-118">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="81caa-118">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




