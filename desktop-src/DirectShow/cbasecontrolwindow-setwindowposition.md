---
description: El método SetWindowPosition establece la posición de la ventana en el escritorio.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Método CBaseControlWindow. SetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660876"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a><span data-ttu-id="074f2-103">CBaseControlWindow. SetWindowPosition, método</span><span class="sxs-lookup"><span data-stu-id="074f2-103">CBaseControlWindow.SetWindowPosition method</span></span>

<span data-ttu-id="074f2-104">El `SetWindowPosition` método establece la posición de la ventana en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="074f2-104">The `SetWindowPosition` method sets the window position on the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="074f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="074f2-105">Syntax</span></span>


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="074f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="074f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074f2-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="074f2-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="074f2-108">Nueva coordenada izquierda.</span><span class="sxs-lookup"><span data-stu-id="074f2-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="074f2-109">*Top* (Principales)</span><span class="sxs-lookup"><span data-stu-id="074f2-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="074f2-110">Nueva coordenada superior.</span><span class="sxs-lookup"><span data-stu-id="074f2-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="074f2-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="074f2-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="074f2-112">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="074f2-112">Width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="074f2-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="074f2-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="074f2-114">Alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="074f2-114">Height of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074f2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="074f2-115">Return value</span></span>

<span data-ttu-id="074f2-116">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="074f2-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="074f2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="074f2-117">Requirements</span></span>



| <span data-ttu-id="074f2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="074f2-118">Requirement</span></span> | <span data-ttu-id="074f2-119">Value</span><span class="sxs-lookup"><span data-stu-id="074f2-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="074f2-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="074f2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="074f2-121"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="074f2-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="074f2-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="074f2-122">Library</span></span><br/> | <dl> <span data-ttu-id="074f2-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="074f2-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="074f2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="074f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074f2-125">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="074f2-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




