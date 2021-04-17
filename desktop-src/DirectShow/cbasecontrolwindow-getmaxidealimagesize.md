---
description: El método GetMaxIdealImageSize recupera el tamaño de imagen máximo ideal.
ms.assetid: 881c1c3d-7505-44a2-964d-3255e2072f6b
title: Método CBaseControlWindow. GetMaxIdealImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMaxIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc8ac53dd30c62f3ebb50585677f83f356b593f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660599"
---
# <a name="cbasecontrolwindowgetmaxidealimagesize-method"></a><span data-ttu-id="ee1d7-103">CBaseControlWindow. GetMaxIdealImageSize, método</span><span class="sxs-lookup"><span data-stu-id="ee1d7-103">CBaseControlWindow.GetMaxIdealImageSize method</span></span>

<span data-ttu-id="ee1d7-104">El `GetMaxIdealImageSize` método recupera el tamaño de imagen máximo ideal.</span><span class="sxs-lookup"><span data-stu-id="ee1d7-104">The `GetMaxIdealImageSize` method retrieves the maximum ideal image size.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee1d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee1d7-105">Syntax</span></span>


```C++
HRESULT GetMaxIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="ee1d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee1d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1d7-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="ee1d7-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="ee1d7-108">Puntero al ancho máximo ideal, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ee1d7-108">Pointer to the maximum ideal width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="ee1d7-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="ee1d7-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="ee1d7-110">Puntero al alto máximo ideal, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ee1d7-110">Pointer to the maximum ideal height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee1d7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee1d7-111">Return value</span></span>

<span data-ttu-id="ee1d7-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee1d7-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee1d7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee1d7-113">Remarks</span></span>

<span data-ttu-id="ee1d7-114">Varios representadores tienen restricciones de rendimiento en cuanto al tamaño de las imágenes que pueden mostrar.</span><span class="sxs-lookup"><span data-stu-id="ee1d7-114">Various renderers have performance restrictions on the size of images they can display.</span></span> <span data-ttu-id="ee1d7-115">Aunque deberían seguir funcionando correctamente cuando se solicita que muestren imágenes mayores que el máximo especificado, los representadores pueden designar los tamaños máximo y mínimo ideales a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="ee1d7-115">Although they should still function properly when requested to display images larger than the specified maximum, renderers can nominate the minimum and maximum ideal sizes through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="ee1d7-116">Solo se puede llamar a esta interfaz cuando el gráfico de filtros está en pausa o en ejecución, ya que no es hasta entonces se asignan los recursos y el representador puede reconocer sus restricciones.</span><span class="sxs-lookup"><span data-stu-id="ee1d7-116">This interface can be called only when the filter graph is paused or running, because it is not until then that resources are allocated and the renderer can recognize its restrictions.</span></span> <span data-ttu-id="ee1d7-117">Si no existen restricciones, el representador rellena los parámetros *pWidth* y *pHeight* con las dimensiones de vídeo nativas y devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="ee1d7-117">If no restrictions exist, the renderer fills in the *pWidth* and *pHeight* parameters with the native video dimensions and returns S\_FALSE.</span></span> <span data-ttu-id="ee1d7-118">Si existen restricciones, se especifican el ancho y el alto restringidos, y la función miembro devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee1d7-118">If restrictions do exist, the restricted width and height are entered, and the member function returns S\_OK.</span></span>

<span data-ttu-id="ee1d7-119">Las dimensiones se aplican al tamaño del vídeo de destino y no al tamaño total de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ee1d7-119">The dimensions apply to the size of the destination video and not to the overall window size.</span></span> <span data-ttu-id="ee1d7-120">Por lo tanto, al calcular el tamaño de la ventana que se va a establecer, tenga en cuenta los estilos de ventana actuales (por ejemplo, WS \_ Caption y WS \_ Border).</span><span class="sxs-lookup"><span data-stu-id="ee1d7-120">So, when calculating the size of the window to set, account for the current window styles (for example, WS\_CAPTION and WS\_BORDER).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee1d7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee1d7-121">Requirements</span></span>



| <span data-ttu-id="ee1d7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee1d7-122">Requirement</span></span> | <span data-ttu-id="ee1d7-123">Value</span><span class="sxs-lookup"><span data-stu-id="ee1d7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1d7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee1d7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ee1d7-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee1d7-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee1d7-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee1d7-126">Library</span></span><br/> | <dl> <span data-ttu-id="ee1d7-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ee1d7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee1d7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee1d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1d7-129">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="ee1d7-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




