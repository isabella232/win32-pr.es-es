---
description: El método DoSetWindowStyle cambia el estilo de ventana típico o extendido.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Método CBaseControlWindow. DoSetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660258"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="0574a-103">CBaseControlWindow. DoSetWindowStyle, método</span><span class="sxs-lookup"><span data-stu-id="0574a-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="0574a-104">El `DoSetWindowStyle` método cambia el estilo de ventana típico o extendido.</span><span class="sxs-lookup"><span data-stu-id="0574a-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="0574a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0574a-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="0574a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0574a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0574a-107">*Estilo*</span><span class="sxs-lookup"><span data-stu-id="0574a-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="0574a-108">Estilos de ventana adecuados.</span><span class="sxs-lookup"><span data-stu-id="0574a-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="0574a-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="0574a-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="0574a-110">Valor que especifica los estilos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="0574a-110">Value specifying which styles to set.</span></span> <span data-ttu-id="0574a-111">Debe ser una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="0574a-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="0574a-112">\_estilo GWL</span><span class="sxs-lookup"><span data-stu-id="0574a-112">GWL\_STYLE</span></span>   | <span data-ttu-id="0574a-113">Recupere los estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="0574a-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="0574a-114">GWL \_ EXstyle</span><span class="sxs-lookup"><span data-stu-id="0574a-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="0574a-115">Recupere los estilos extendidos de ventana.</span><span class="sxs-lookup"><span data-stu-id="0574a-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0574a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0574a-116">Return value</span></span>

<span data-ttu-id="0574a-117">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0574a-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0574a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0574a-118">Remarks</span></span>

<span data-ttu-id="0574a-119">Esta función miembro llama a la función **SetWindowLong** de Win32 para establecer el estilo de ventana y, a continuación, vuelve a mostrar la ventana en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="0574a-119">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="0574a-120">Esta función miembro se llama mediante las funciones miembro [**CBaseControlWindow::p UT \_ estiloVentana**](cbasecontrolwindow-put-windowstyle.md) y [**CBaseControlWindow::p UT \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="0574a-120">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0574a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0574a-121">Requirements</span></span>



| <span data-ttu-id="0574a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0574a-122">Requirement</span></span> | <span data-ttu-id="0574a-123">Value</span><span class="sxs-lookup"><span data-stu-id="0574a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0574a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0574a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0574a-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0574a-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0574a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0574a-126">Library</span></span><br/> | <dl> <span data-ttu-id="0574a-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0574a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0574a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0574a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0574a-129">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="0574a-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




