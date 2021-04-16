---
description: El método activo crea un subproceso de trabajo que extrae datos del PIN de salida. Este método también confirma el asignador.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Método CPullPin. Active (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671823"
---
# <a name="cpullpinactive-method"></a><span data-ttu-id="a8c29-104">CPullPin. Active (método)</span><span class="sxs-lookup"><span data-stu-id="a8c29-104">CPullPin.Active method</span></span>

<span data-ttu-id="a8c29-105">El método **activo** crea un subproceso de trabajo que extrae datos del PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="a8c29-105">The **Active** method creates a worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="a8c29-106">Este método también confirma el asignador.</span><span class="sxs-lookup"><span data-stu-id="a8c29-106">This method also commits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c29-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8c29-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="a8c29-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8c29-108">Parameters</span></span>

<span data-ttu-id="a8c29-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a8c29-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8c29-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8c29-110">Return value</span></span>

<span data-ttu-id="a8c29-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8c29-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a8c29-112">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a8c29-112">Possible values include the following.</span></span>



| <span data-ttu-id="a8c29-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a8c29-113">Return code</span></span>                                                                                  | <span data-ttu-id="a8c29-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8c29-114">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="a8c29-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a8c29-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a8c29-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a8c29-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="a8c29-117"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="a8c29-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="a8c29-118">La conexión del PIN no se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8c29-118">The pin connection was not established correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="a8c29-119"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="a8c29-119"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="a8c29-120">No se pudo crear el subproceso o el subproceso ya existe.</span><span class="sxs-lookup"><span data-stu-id="a8c29-120">Could not create the thread, or the thread already exists.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8c29-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8c29-121">Remarks</span></span>

<span data-ttu-id="a8c29-122">Llame a este método cuando el filtro propietario se active.</span><span class="sxs-lookup"><span data-stu-id="a8c29-122">Call this method when the owning filter becomes active.</span></span> <span data-ttu-id="a8c29-123">(Si el PIN de entrada se deriva de [**CBasePin**](cbasepin.md), invalide el método [**CBasePin:: Active**](cbasepin-active.md) ).</span><span class="sxs-lookup"><span data-stu-id="a8c29-123">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Active**](cbasepin-active.md) method.)</span></span>

<span data-ttu-id="a8c29-124">Antes de llamar a este método, llame al método [**CPullPin:: Connect**](cpullpin-connect.md) para establecer la conexión con el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="a8c29-124">Before calling this method, call the [**CPullPin::Connect**](cpullpin-connect.md) method to establish the connection with the output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c29-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8c29-125">Requirements</span></span>



| <span data-ttu-id="a8c29-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8c29-126">Requirement</span></span> | <span data-ttu-id="a8c29-127">Value</span><span class="sxs-lookup"><span data-stu-id="a8c29-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c29-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8c29-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a8c29-129"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8c29-129"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="a8c29-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8c29-130">Library</span></span><br/> | <dl> <span data-ttu-id="a8c29-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a8c29-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8c29-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8c29-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c29-133">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="a8c29-133">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




