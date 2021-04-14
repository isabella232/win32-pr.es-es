---
description: El \_ método visible Put hace que muestre u oculte la ventana.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: Método CBaseControlWindow.put_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf713b4ccb9932b1201e7ced40fddcd87407ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661344"
---
# <a name="cbasecontrolwindowput_visible-method"></a><span data-ttu-id="9d930-103">CBaseControlWindow. put ( \_ método visible)</span><span class="sxs-lookup"><span data-stu-id="9d930-103">CBaseControlWindow.put\_Visible method</span></span>

<span data-ttu-id="9d930-104">El `put_Visible` método hace que muestre u oculte la ventana.</span><span class="sxs-lookup"><span data-stu-id="9d930-104">The `put_Visible` method makes shows or hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d930-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d930-105">Syntax</span></span>


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a><span data-ttu-id="9d930-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d930-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d930-107">*Visible*</span><span class="sxs-lookup"><span data-stu-id="9d930-107">*Visible*</span></span> 
</dt> <dd>

<span data-ttu-id="9d930-108">Marca booleana de Automation (0 significa que la ventana está oculta; se muestra una ventana de 1).</span><span class="sxs-lookup"><span data-stu-id="9d930-108">Automation Boolean flag (0 means window is hidden,  1 means window is shown).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d930-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d930-109">Return value</span></span>

<span data-ttu-id="9d930-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d930-110">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d930-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d930-111">Requirements</span></span>



| <span data-ttu-id="9d930-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d930-112">Requirement</span></span> | <span data-ttu-id="9d930-113">Value</span><span class="sxs-lookup"><span data-stu-id="9d930-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d930-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d930-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9d930-115"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d930-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9d930-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d930-116">Library</span></span><br/> | <dl> <span data-ttu-id="9d930-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9d930-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d930-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d930-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d930-119">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="9d930-119">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




