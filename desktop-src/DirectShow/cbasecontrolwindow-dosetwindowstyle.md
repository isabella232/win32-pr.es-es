---
description: El método DoSetWindowStyle cambia los estilos de ventana típicos o extendidos.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Método CBaseControlWindow.DoSetWindowStyle (Ctlutil.h)
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
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909813"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="22dc4-103">CBaseControlWindow.DoSetWindowStyle (método)</span><span class="sxs-lookup"><span data-stu-id="22dc4-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="22dc4-104">El `DoSetWindowStyle` método cambia los estilos de ventana típicos o extendidos.</span><span class="sxs-lookup"><span data-stu-id="22dc4-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="22dc4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22dc4-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="22dc4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22dc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22dc4-107">*Estilo*</span><span class="sxs-lookup"><span data-stu-id="22dc4-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="22dc4-108">Estilos de ventana adecuados.</span><span class="sxs-lookup"><span data-stu-id="22dc4-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="22dc4-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="22dc4-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="22dc4-110">Valor que especifica los estilos que se establecerán.</span><span class="sxs-lookup"><span data-stu-id="22dc4-110">Value specifying which styles to set.</span></span> <span data-ttu-id="22dc4-111">Debe ser una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="22dc4-111">Must be one of the following:</span></span>



| <span data-ttu-id="22dc4-112">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="22dc4-112">Label</span></span> | <span data-ttu-id="22dc4-113">Value</span><span class="sxs-lookup"><span data-stu-id="22dc4-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="22dc4-114">ESTILO \_ GWL</span><span class="sxs-lookup"><span data-stu-id="22dc4-114">GWL\_STYLE</span></span>   | <span data-ttu-id="22dc4-115">Recupere los estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="22dc4-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="22dc4-116">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="22dc4-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="22dc4-117">Recupere los estilos de ventana extendidos.</span><span class="sxs-lookup"><span data-stu-id="22dc4-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22dc4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22dc4-118">Return value</span></span>

<span data-ttu-id="22dc4-119">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="22dc4-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22dc4-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22dc4-120">Remarks</span></span>

<span data-ttu-id="22dc4-121">Esta función miembro llama a la función **SetWindowLong** de Win32 para establecer el estilo de ventana y, a continuación, vuelve a mostrar la ventana en la posición actual.</span><span class="sxs-lookup"><span data-stu-id="22dc4-121">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="22dc4-122">Las funciones miembro [**CBaseControlWindow::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) y [**CBaseControlWindow::p ut \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) llaman a esta función miembro.</span><span class="sxs-lookup"><span data-stu-id="22dc4-122">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="22dc4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22dc4-123">Requirements</span></span>



| <span data-ttu-id="22dc4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="22dc4-124">Requirement</span></span> | <span data-ttu-id="22dc4-125">Value</span><span class="sxs-lookup"><span data-stu-id="22dc4-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22dc4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22dc4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="22dc4-127"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="22dc4-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22dc4-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22dc4-128">Library</span></span><br/> | <dl> <span data-ttu-id="22dc4-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="22dc4-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22dc4-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="22dc4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22dc4-131">**CBaseControlWindow (clase)**</span><span class="sxs-lookup"><span data-stu-id="22dc4-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




