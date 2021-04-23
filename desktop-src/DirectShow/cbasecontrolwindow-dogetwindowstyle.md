---
description: El método DoGetWindowStyle recupera los estilos de ventana normales o extendidos actuales.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Método CBaseControlWindow.DoGetWindowStyle (Ctlutil.h)
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
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909823"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="09731-103">CBaseControlWindow.DoGetWindowStyle (método)</span><span class="sxs-lookup"><span data-stu-id="09731-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="09731-104">El `DoGetWindowStyle` método recupera los estilos de ventana normales o extendidos actuales.</span><span class="sxs-lookup"><span data-stu-id="09731-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="09731-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09731-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="09731-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09731-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09731-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="09731-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="09731-108">Puntero a una variable que recibe la información de estilo.</span><span class="sxs-lookup"><span data-stu-id="09731-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="09731-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="09731-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="09731-110">Valor que especifica los estilos que se recuperarán.</span><span class="sxs-lookup"><span data-stu-id="09731-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="09731-111">Debe ser una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="09731-111">Must be one of the following:</span></span>



| <span data-ttu-id="09731-112">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="09731-112">Label</span></span> | <span data-ttu-id="09731-113">Value</span><span class="sxs-lookup"><span data-stu-id="09731-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="09731-114">ESTILO \_ GWL</span><span class="sxs-lookup"><span data-stu-id="09731-114">GWL\_STYLE</span></span>   | <span data-ttu-id="09731-115">Recupere los estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="09731-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="09731-116">GWL \_ EXSTYLE</span><span class="sxs-lookup"><span data-stu-id="09731-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="09731-117">Recupere los estilos de ventana extendidos.</span><span class="sxs-lookup"><span data-stu-id="09731-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09731-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09731-118">Return value</span></span>

<span data-ttu-id="09731-119">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="09731-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09731-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09731-120">Remarks</span></span>

<span data-ttu-id="09731-121">Esta función miembro llama a la función **GetWindowLong** de Win32 para recuperar el estilo de ventana.</span><span class="sxs-lookup"><span data-stu-id="09731-121">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="09731-122">Lo llaman las funciones [**miembro CBaseControlWindow::get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) y [**CBaseControlWindow::get \_ WindowStyleEx.**](cbasecontrolwindow-get-windowstyleex.md)</span><span class="sxs-lookup"><span data-stu-id="09731-122">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="09731-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09731-123">Requirements</span></span>



| <span data-ttu-id="09731-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="09731-124">Requirement</span></span> | <span data-ttu-id="09731-125">Value</span><span class="sxs-lookup"><span data-stu-id="09731-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09731-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09731-126">Header</span></span><br/>  | <dl> <span data-ttu-id="09731-127"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="09731-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09731-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09731-128">Library</span></span><br/> | <dl> <span data-ttu-id="09731-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="09731-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09731-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="09731-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09731-131">**CBaseControlWindow (clase)**</span><span class="sxs-lookup"><span data-stu-id="09731-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




