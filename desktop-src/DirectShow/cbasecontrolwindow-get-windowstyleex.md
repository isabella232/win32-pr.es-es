---
description: El \_ método get WindowStyleEx recupera los estilos extendidos de ventana.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: Método CBaseControlWindow.get_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c59336ab57e92e99366494a272f2b995191b494b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661202"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a><span data-ttu-id="af30c-103">CBaseControlWindow. Get \_ WindowStyleEx (método)</span><span class="sxs-lookup"><span data-stu-id="af30c-103">CBaseControlWindow.get\_WindowStyleEx method</span></span>

<span data-ttu-id="af30c-104">El `get_WindowStyleEx` método recupera los estilos extendidos de ventana.</span><span class="sxs-lookup"><span data-stu-id="af30c-104">The `get_WindowStyleEx` method retrieves the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="af30c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af30c-105">Syntax</span></span>


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="af30c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af30c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af30c-107">*pWindowStyleEx*</span><span class="sxs-lookup"><span data-stu-id="af30c-107">*pWindowStyleEx*</span></span> 
</dt> <dd>

<span data-ttu-id="af30c-108">Puntero a estilos de ventana extendidos.</span><span class="sxs-lookup"><span data-stu-id="af30c-108">Pointer to extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af30c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af30c-109">Return value</span></span>

<span data-ttu-id="af30c-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af30c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af30c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af30c-111">Remarks</span></span>

<span data-ttu-id="af30c-112">Esta función miembro recupera los estilos extendidos de ventana.</span><span class="sxs-lookup"><span data-stu-id="af30c-112">This member function retrieves the extended window styles.</span></span> <span data-ttu-id="af30c-113">Llama a la función miembro [**CBaseControlWindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="af30c-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="af30c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af30c-114">Requirements</span></span>



| <span data-ttu-id="af30c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="af30c-115">Requirement</span></span> | <span data-ttu-id="af30c-116">Value</span><span class="sxs-lookup"><span data-stu-id="af30c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af30c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af30c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="af30c-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af30c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af30c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af30c-119">Library</span></span><br/> | <dl> <span data-ttu-id="af30c-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="af30c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af30c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="af30c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af30c-122">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="af30c-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




