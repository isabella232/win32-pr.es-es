---
description: El método CheckSizes comprueba las propiedades de asignador con el tipo de medio actual.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Método CImageAllocator. CheckSizes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680516"
---
# <a name="cimageallocatorchecksizes-method"></a><span data-ttu-id="a89cc-103">CImageAllocator. CheckSizes, método</span><span class="sxs-lookup"><span data-stu-id="a89cc-103">CImageAllocator.CheckSizes method</span></span>

<span data-ttu-id="a89cc-104">El `CheckSizes` método comprueba las propiedades de asignador con el tipo de medio actual.</span><span class="sxs-lookup"><span data-stu-id="a89cc-104">The `CheckSizes` method checks allocator properties against the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a89cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a89cc-105">Syntax</span></span>


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a><span data-ttu-id="a89cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a89cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a89cc-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="a89cc-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="a89cc-108">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que describe las propiedades de asignador solicitadas.</span><span class="sxs-lookup"><span data-stu-id="a89cc-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that describes the requested allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a89cc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a89cc-109">Return value</span></span>

<span data-ttu-id="a89cc-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a89cc-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a89cc-111">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a89cc-111">Possible values include the following.</span></span>



| <span data-ttu-id="a89cc-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a89cc-112">Return code</span></span>                                                                                           | <span data-ttu-id="a89cc-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a89cc-113">Description</span></span>                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a89cc-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a89cc-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a89cc-115">Las propiedades solicitadas son compatibles con el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a89cc-115">The requested properties are compatible with the media type.</span></span><br/>     |
| <dl> <span data-ttu-id="a89cc-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a89cc-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="a89cc-117">Las propiedades solicitadas no son compatibles con el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a89cc-117">The requested properties are not compatible with the media type.</span></span><br/> |
| <dl> <span data-ttu-id="a89cc-118"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="a89cc-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a89cc-119">El PIN propietario no está conectado.</span><span class="sxs-lookup"><span data-stu-id="a89cc-119">The owning pin is not connected.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="a89cc-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a89cc-120">Remarks</span></span>

<span data-ttu-id="a89cc-121">Cuando el método devuelve, si el valor devuelto es S \_ OK, el miembro **cbBuffer** de *pRequest* contiene el tamaño de búfer real.</span><span class="sxs-lookup"><span data-stu-id="a89cc-121">When the method returns, if the return value is S\_OK, the **cbBuffer** member of *pRequest* contains the actual buffer size.</span></span> <span data-ttu-id="a89cc-122">Esto puede ser mayor que el tamaño solicitado, pero nunca será menor.</span><span class="sxs-lookup"><span data-stu-id="a89cc-122">This might be larger than the requested size, but will never be smaller.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89cc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a89cc-123">Requirements</span></span>



| <span data-ttu-id="a89cc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a89cc-124">Requirement</span></span> | <span data-ttu-id="a89cc-125">Value</span><span class="sxs-lookup"><span data-stu-id="a89cc-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a89cc-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a89cc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a89cc-127"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a89cc-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a89cc-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a89cc-128">Library</span></span><br/> | <dl> <span data-ttu-id="a89cc-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a89cc-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a89cc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a89cc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a89cc-131">**Clase CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="a89cc-131">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




