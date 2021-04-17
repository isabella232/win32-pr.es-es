---
description: El \_ método get WindowStyle recupera los estilos de ventana estándar.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: Método CBaseControlWindow.get_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661203"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a><span data-ttu-id="41cf5-103">CBaseControlWindow. Get \_ estiloVentana (método)</span><span class="sxs-lookup"><span data-stu-id="41cf5-103">CBaseControlWindow.get\_WindowStyle method</span></span>

<span data-ttu-id="41cf5-104">El `get_WindowStyle` método recupera los estilos de ventana estándar.</span><span class="sxs-lookup"><span data-stu-id="41cf5-104">The `get_WindowStyle` method retrieves the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="41cf5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41cf5-105">Syntax</span></span>


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="41cf5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41cf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41cf5-107">*pWindowStyle*</span><span class="sxs-lookup"><span data-stu-id="41cf5-107">*pWindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="41cf5-108">Puntero a los estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="41cf5-108">Pointer to window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41cf5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41cf5-109">Return value</span></span>

<span data-ttu-id="41cf5-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41cf5-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41cf5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41cf5-111">Remarks</span></span>

<span data-ttu-id="41cf5-112">Esta función miembro devuelve los estilos de ventana estándar, como WS \_ Child y WS \_ visible.</span><span class="sxs-lookup"><span data-stu-id="41cf5-112">This member function returns the standard window styles, such as WS\_CHILD and WS\_VISIBLE.</span></span> <span data-ttu-id="41cf5-113">Llama a la función miembro [**CBaseControlWindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="41cf5-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="41cf5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41cf5-114">Requirements</span></span>



| <span data-ttu-id="41cf5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="41cf5-115">Requirement</span></span> | <span data-ttu-id="41cf5-116">Value</span><span class="sxs-lookup"><span data-stu-id="41cf5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41cf5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41cf5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="41cf5-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41cf5-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="41cf5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41cf5-119">Library</span></span><br/> | <dl> <span data-ttu-id="41cf5-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="41cf5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41cf5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="41cf5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41cf5-122">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="41cf5-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




