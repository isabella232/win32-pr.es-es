---
description: Número de subprocesos de streaming con este pin.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Miembro CDynamicOutputPin:: m_dwNumOutstandingOutputPinUsers (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2ba214a2c1c6d3d056147db54c936cb61b73dcfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671754"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a><span data-ttu-id="fb701-103">Miembro dwNumOutstandingOutputPinUsers CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="fb701-103">CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers member</span></span>

<span data-ttu-id="fb701-104">Número de subprocesos de streaming con este pin.</span><span class="sxs-lookup"><span data-stu-id="fb701-104">Number of streaming threads using this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb701-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb701-105">Syntax</span></span>


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a><span data-ttu-id="fb701-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb701-106">Remarks</span></span>

<span data-ttu-id="fb701-107">El método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) incrementa esta variable y el método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) la reduce.</span><span class="sxs-lookup"><span data-stu-id="fb701-107">The [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method increments this variable, and the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method decrements it.</span></span> <span data-ttu-id="fb701-108">Cuando el valor es mayor que cero, algún subproceso está usando este pin para transmitir datos o cambiar el tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="fb701-108">When the value is greater than zero, some thread is using this pin to stream data or to change the connection type.</span></span> <span data-ttu-id="fb701-109">No se puede bloquear el PIN mientras este sea el caso.</span><span class="sxs-lookup"><span data-stu-id="fb701-109">The pin cannot be blocked while this is the case.</span></span>

<span data-ttu-id="fb701-110">Antes de tener acceso a esta variable, conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="fb701-110">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb701-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb701-111">Requirements</span></span>



| <span data-ttu-id="fb701-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb701-112">Requirement</span></span> | <span data-ttu-id="fb701-113">Value</span><span class="sxs-lookup"><span data-stu-id="fb701-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb701-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb701-114">Header</span></span><br/>  | <dl> <span data-ttu-id="fb701-115"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb701-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fb701-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb701-116">Library</span></span><br/> | <dl> <span data-ttu-id="fb701-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fb701-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb701-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb701-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb701-119">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="fb701-119">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> <dt>

[<span data-ttu-id="fb701-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="fb701-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span></span>](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




