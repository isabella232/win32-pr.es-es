---
description: El \_ método put Caption establece el título o el título de la ventana.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Método CBaseControlWindow.put_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660627"
---
# <a name="cbasecontrolwindowput_caption-method"></a><span data-ttu-id="ed242-103">CBaseControlWindow. put ( \_ método de leyenda)</span><span class="sxs-lookup"><span data-stu-id="ed242-103">CBaseControlWindow.put\_Caption method</span></span>

<span data-ttu-id="ed242-104">El `put_Caption` método establece el título o el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ed242-104">The `put_Caption` method sets the window title or caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed242-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed242-105">Syntax</span></span>


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a><span data-ttu-id="ed242-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed242-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed242-107">*strCaption*</span><span class="sxs-lookup"><span data-stu-id="ed242-107">*strCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="ed242-108">Nuevo título de ventana.</span><span class="sxs-lookup"><span data-stu-id="ed242-108">New window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed242-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed242-109">Return value</span></span>

<span data-ttu-id="ed242-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ed242-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed242-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed242-111">Remarks</span></span>

<span data-ttu-id="ed242-112">La mayoría de las ventanas de nivel superior de un escritorio basado en Windows tienen un título (título) asociado.</span><span class="sxs-lookup"><span data-stu-id="ed242-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="ed242-113">Esta propiedad se puede consultar y establecer a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="ed242-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="ed242-114">Cualquier conjunto de títulos solo será visible si la ventana tiene aplicado el \_ estilo de leyenda de WS.</span><span class="sxs-lookup"><span data-stu-id="ed242-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="ed242-115">Si no es así, el título se puede establecer (y recuperar), aunque no será visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ed242-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed242-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed242-116">Requirements</span></span>



| <span data-ttu-id="ed242-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed242-117">Requirement</span></span> | <span data-ttu-id="ed242-118">Value</span><span class="sxs-lookup"><span data-stu-id="ed242-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed242-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed242-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ed242-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed242-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed242-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed242-121">Library</span></span><br/> | <dl> <span data-ttu-id="ed242-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ed242-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed242-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed242-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed242-124">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="ed242-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




