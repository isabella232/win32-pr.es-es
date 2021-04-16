---
description: El método Gethresult (recupera el valor HRESULT del comando invocado.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Método CDeferredCommand. Gethresult ((Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671769"
---
# <a name="cdeferredcommandgethresult-method"></a><span data-ttu-id="c8e34-103">CDeferredCommand. Gethresult (, método</span><span class="sxs-lookup"><span data-stu-id="c8e34-103">CDeferredCommand.GetHResult method</span></span>

<span data-ttu-id="c8e34-104">El `GetHResult` método recupera el valor **HRESULT** del comando invocado.</span><span class="sxs-lookup"><span data-stu-id="c8e34-104">The `GetHResult` method retrieves the **HRESULT** value from the invoked command.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e34-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8e34-105">Syntax</span></span>


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a><span data-ttu-id="c8e34-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8e34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e34-107">*phrResult*</span><span class="sxs-lookup"><span data-stu-id="c8e34-107">*phrResult*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e34-108">Puntero al valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8e34-108">Pointer to the **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e34-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8e34-109">Return value</span></span>

<span data-ttu-id="c8e34-110">Devuelve E \_ Abort si **m \_ pQueue** es **null**.</span><span class="sxs-lookup"><span data-stu-id="c8e34-110">Returns E\_ABORT if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="c8e34-111">De lo contrario, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c8e34-111">Otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e34-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8e34-112">Remarks</span></span>

<span data-ttu-id="c8e34-113">Esta función miembro implementa el método [**IDeferredCommand:: gethresult (**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .</span><span class="sxs-lookup"><span data-stu-id="c8e34-113">This member function implements the [**IDeferredCommand::GetHResult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8e34-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8e34-114">Requirements</span></span>



| <span data-ttu-id="c8e34-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8e34-115">Requirement</span></span> | <span data-ttu-id="c8e34-116">Value</span><span class="sxs-lookup"><span data-stu-id="c8e34-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e34-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8e34-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c8e34-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8e34-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8e34-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8e34-119">Library</span></span><br/> | <dl> <span data-ttu-id="c8e34-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c8e34-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8e34-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8e34-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e34-122">**Clase CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="c8e34-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




