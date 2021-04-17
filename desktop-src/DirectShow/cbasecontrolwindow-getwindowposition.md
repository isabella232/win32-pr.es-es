---
description: El método GetWindowPosition recupera las coordenadas actuales para la ventana.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Método CBaseControlWindow. GetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660594"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a><span data-ttu-id="90fe4-103">CBaseControlWindow. GetWindowPosition, método</span><span class="sxs-lookup"><span data-stu-id="90fe4-103">CBaseControlWindow.GetWindowPosition method</span></span>

<span data-ttu-id="90fe4-104">El `GetWindowPosition` método recupera las coordenadas actuales para la ventana.</span><span class="sxs-lookup"><span data-stu-id="90fe4-104">The `GetWindowPosition` method retrieves the current coordinates for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="90fe4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90fe4-105">Syntax</span></span>


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="90fe4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90fe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90fe4-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="90fe4-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="90fe4-108">Puntero a la coordenada izquierda, en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="90fe4-108">Pointer to the left coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="90fe4-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="90fe4-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="90fe4-110">Puntero en la coordenada superior, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="90fe4-110">Pointer to the top coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="90fe4-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="90fe4-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="90fe4-112">Puntero en el ancho de la ventana, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="90fe4-112">Pointer to the window width, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="90fe4-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="90fe4-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="90fe4-114">Puntero al alto de la ventana, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="90fe4-114">Pointer to the window height, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90fe4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90fe4-115">Return value</span></span>

<span data-ttu-id="90fe4-116">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="90fe4-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="90fe4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90fe4-117">Requirements</span></span>



| <span data-ttu-id="90fe4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="90fe4-118">Requirement</span></span> | <span data-ttu-id="90fe4-119">Value</span><span class="sxs-lookup"><span data-stu-id="90fe4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90fe4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90fe4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="90fe4-121"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90fe4-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="90fe4-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90fe4-122">Library</span></span><br/> | <dl> <span data-ttu-id="90fe4-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="90fe4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90fe4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="90fe4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90fe4-125">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="90fe4-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




