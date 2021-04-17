---
description: El método DoGetWindowStyle recupera los estilos de ventana normales o extendidos actuales.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Método CBaseControlWindow. DoGetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670849"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="30388-103">CBaseControlWindow. DoGetWindowStyle, método</span><span class="sxs-lookup"><span data-stu-id="30388-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="30388-104">El `DoGetWindowStyle` método recupera los estilos de ventana normales o extendidos actuales.</span><span class="sxs-lookup"><span data-stu-id="30388-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="30388-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30388-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="30388-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30388-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30388-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="30388-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="30388-108">Puntero a una variable que recibe la información de estilo.</span><span class="sxs-lookup"><span data-stu-id="30388-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="30388-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="30388-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="30388-110">Valor que especifica los estilos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="30388-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="30388-111">Debe ser una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="30388-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="30388-112">\_estilo GWL</span><span class="sxs-lookup"><span data-stu-id="30388-112">GWL\_STYLE</span></span>   | <span data-ttu-id="30388-113">Recupere los estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="30388-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="30388-114">GWL \_ EXstyle</span><span class="sxs-lookup"><span data-stu-id="30388-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="30388-115">Recupere los estilos extendidos de ventana.</span><span class="sxs-lookup"><span data-stu-id="30388-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30388-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30388-116">Return value</span></span>

<span data-ttu-id="30388-117">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30388-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30388-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30388-118">Remarks</span></span>

<span data-ttu-id="30388-119">Esta función miembro llama a la función **GetWindowLong** de Win32 para recuperar el estilo de ventana.</span><span class="sxs-lookup"><span data-stu-id="30388-119">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="30388-120">Lo llaman las funciones miembro [**CBaseControlWindow:: get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) y [**CBaseControlWindow:: get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="30388-120">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="30388-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30388-121">Requirements</span></span>



| <span data-ttu-id="30388-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="30388-122">Requirement</span></span> | <span data-ttu-id="30388-123">Value</span><span class="sxs-lookup"><span data-stu-id="30388-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30388-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30388-124">Header</span></span><br/>  | <dl> <span data-ttu-id="30388-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30388-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30388-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30388-126">Library</span></span><br/> | <dl> <span data-ttu-id="30388-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="30388-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30388-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="30388-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30388-129">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="30388-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




