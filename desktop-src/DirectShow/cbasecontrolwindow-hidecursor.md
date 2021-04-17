---
description: El método HideCursor oculta o muestra el cursor.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Método CBaseControlWindow. HideCursor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660738"
---
# <a name="cbasecontrolwindowhidecursor-method"></a><span data-ttu-id="e3722-103">CBaseControlWindow. HideCursor, método</span><span class="sxs-lookup"><span data-stu-id="e3722-103">CBaseControlWindow.HideCursor method</span></span>

<span data-ttu-id="e3722-104">El `HideCursor` método oculta o muestra el cursor.</span><span class="sxs-lookup"><span data-stu-id="e3722-104">The `HideCursor` method hides or displays the cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3722-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3722-105">Syntax</span></span>


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a><span data-ttu-id="e3722-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3722-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3722-107">*HideCursor*</span><span class="sxs-lookup"><span data-stu-id="e3722-107">*HideCursor*</span></span> 
</dt> <dd>

<span data-ttu-id="e3722-108">Valor que especifica si se va a mostrar el cursor.</span><span class="sxs-lookup"><span data-stu-id="e3722-108">Value specifying whether to show the cursor.</span></span> <span data-ttu-id="e3722-109">Establézcalo en OATRUE para ocultar el cursor, o OAFALSE para mostrar el cursor.</span><span class="sxs-lookup"><span data-stu-id="e3722-109">Set to OATRUE to hide the cursor, or OAFALSE to display the cursor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3722-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3722-110">Return value</span></span>

<span data-ttu-id="e3722-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3722-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3722-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3722-112">Requirements</span></span>



| <span data-ttu-id="e3722-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3722-113">Requirement</span></span> | <span data-ttu-id="e3722-114">Value</span><span class="sxs-lookup"><span data-stu-id="e3722-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3722-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3722-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e3722-116"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3722-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3722-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3722-117">Library</span></span><br/> | <dl> <span data-ttu-id="e3722-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e3722-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3722-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3722-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3722-120">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="e3722-120">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




