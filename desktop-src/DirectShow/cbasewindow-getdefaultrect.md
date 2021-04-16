---
description: El método GetDefaultRect recupera el tamaño predeterminado del área cliente.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Método CBaseWindow. GetDefaultRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679568"
---
# <a name="cbasewindowgetdefaultrect-method"></a><span data-ttu-id="349b3-103">CBaseWindow. GetDefaultRect, método</span><span class="sxs-lookup"><span data-stu-id="349b3-103">CBaseWindow.GetDefaultRect method</span></span>

<span data-ttu-id="349b3-104">El `GetDefaultRect` método recupera el tamaño predeterminado del área cliente.</span><span class="sxs-lookup"><span data-stu-id="349b3-104">The `GetDefaultRect` method retrieves the default size of the client area.</span></span>

## <a name="syntax"></a><span data-ttu-id="349b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="349b3-105">Syntax</span></span>


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a><span data-ttu-id="349b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="349b3-106">Parameters</span></span>

<span data-ttu-id="349b3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="349b3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="349b3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="349b3-108">Return value</span></span>

<span data-ttu-id="349b3-109">Devuelve el rectángulo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="349b3-109">Returns the default rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="349b3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="349b3-110">Remarks</span></span>

<span data-ttu-id="349b3-111">Cuando se activa la ventana, el objeto llama a este método para determinar el tamaño que debe tener el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="349b3-111">When the window is activated, the object calls this method to determine how large it should make the window's client area.</span></span> <span data-ttu-id="349b3-112">En la clase base, este método devuelve un rectángulo cuyo alto y ancho son las constantes definidas DEFHEIGHT y DEFWIDTH.</span><span class="sxs-lookup"><span data-stu-id="349b3-112">In the base class, this method returns a rectangle whose height and width are the defined constants DEFHEIGHT and DEFWIDTH.</span></span> <span data-ttu-id="349b3-113">Una clase derivada debe reemplazar este método.</span><span class="sxs-lookup"><span data-stu-id="349b3-113">A derived class should override this method.</span></span> <span data-ttu-id="349b3-114">En el caso de un representador de vídeo, la clase derivada normalmente devolverá el tamaño de la imagen de vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="349b3-114">For a video renderer, the derived class will typically return the size of the native video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="349b3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="349b3-115">Requirements</span></span>



| <span data-ttu-id="349b3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="349b3-116">Requirement</span></span> | <span data-ttu-id="349b3-117">Value</span><span class="sxs-lookup"><span data-stu-id="349b3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="349b3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="349b3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="349b3-119"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="349b3-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="349b3-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="349b3-120">Library</span></span><br/> | <dl> <span data-ttu-id="349b3-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="349b3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="349b3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="349b3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="349b3-123">**Clase CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="349b3-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




