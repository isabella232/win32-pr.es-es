---
description: 'Método CDynamicOutputPin.Disconnect: el método Disconnect interrumpe la conexión de pin actual. Este método implementa el método IPin::D isconnect.'
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Método CDynamicOutputPin.Disconnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099303"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="d7bd6-104">Método CDynamicOutputPin.Disconnect</span><span class="sxs-lookup"><span data-stu-id="d7bd6-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="d7bd6-105">El `Disconnect` método interrumpe la conexión de pin actual.</span><span class="sxs-lookup"><span data-stu-id="d7bd6-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="d7bd6-106">Este método implementa el [**método IPin::D isconnect.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)</span><span class="sxs-lookup"><span data-stu-id="d7bd6-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7bd6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7bd6-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="d7bd6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7bd6-108">Parameters</span></span>

<span data-ttu-id="d7bd6-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d7bd6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7bd6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7bd6-110">Return value</span></span>

<span data-ttu-id="d7bd6-111">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d7bd6-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d7bd6-112">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d7bd6-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d7bd6-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d7bd6-113">Return code</span></span>                                                                             | <span data-ttu-id="d7bd6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7bd6-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d7bd6-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d7bd6-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d7bd6-116">El pin no estaba conectado.</span><span class="sxs-lookup"><span data-stu-id="d7bd6-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="d7bd6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7bd6-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d7bd6-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d7bd6-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="d7bd6-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7bd6-119">Remarks</span></span>

<span data-ttu-id="d7bd6-120">Este método invalida el método [**CBasePin::D isconnect**](cbasepin-disconnect.md) para habilitar la desconexión mientras el filtro está activo.</span><span class="sxs-lookup"><span data-stu-id="d7bd6-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7bd6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7bd6-121">Requirements</span></span>



| <span data-ttu-id="d7bd6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7bd6-122">Requirement</span></span> | <span data-ttu-id="d7bd6-123">Value</span><span class="sxs-lookup"><span data-stu-id="d7bd6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bd6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7bd6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d7bd6-125"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7bd6-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d7bd6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7bd6-126">Library</span></span><br/> | <dl> <span data-ttu-id="d7bd6-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d7bd6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7bd6-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d7bd6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bd6-129">**CDynamicOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="d7bd6-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




