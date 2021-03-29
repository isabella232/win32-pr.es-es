---
description: El método DecideAllocator negocia un asignador con el PIN de salida.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Método CPullPin. DecideAllocator (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680836"
---
# <a name="cpullpindecideallocator-method"></a><span data-ttu-id="d86b6-103">CPullPin. DecideAllocator, método</span><span class="sxs-lookup"><span data-stu-id="d86b6-103">CPullPin.DecideAllocator method</span></span>

<span data-ttu-id="d86b6-104">El `DecideAllocator` método negocia un asignador con el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="d86b6-104">The `DecideAllocator` method negotiates an allocator with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d86b6-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="d86b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d86b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d86b6-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="d86b6-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="d86b6-108">Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador preferido del PIN de entrada o **null**.</span><span class="sxs-lookup"><span data-stu-id="d86b6-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d86b6-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="d86b6-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="d86b6-110">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) opcional que contiene los requisitos de búfer del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d86b6-110">Pointer to an optional [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d86b6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d86b6-111">Return value</span></span>

<span data-ttu-id="d86b6-112">Devuelve \_ si es correcto, o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d86b6-112">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d86b6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d86b6-113">Remarks</span></span>

<span data-ttu-id="d86b6-114">Este método llama al método [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) para negociar un asignador.</span><span class="sxs-lookup"><span data-stu-id="d86b6-114">This method calls the [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method to negotiate an allocator.</span></span> <span data-ttu-id="d86b6-115">Pasa el parámetro *pAlloc* directamente al método **RequestAllocator** .</span><span class="sxs-lookup"><span data-stu-id="d86b6-115">It passes the *pAlloc* parameter directly to the **RequestAllocator** method.</span></span> <span data-ttu-id="d86b6-116">Pasa el parámetro *pProps* a **RequestAllocator** si *pProps* no es **null**; de lo contrario, crea una estructura de **\_ propiedades de asignador** con una solicitud predeterminada de tres búferes de 64 k.</span><span class="sxs-lookup"><span data-stu-id="d86b6-116">It passes the *pProps* parameter to **RequestAllocator** if *pProps* is non-**NULL**; otherwise, it creates an **ALLOCATOR\_PROPERTIES** structure with a default request of three 64K buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d86b6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d86b6-117">Requirements</span></span>



| <span data-ttu-id="d86b6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d86b6-118">Requirement</span></span> | <span data-ttu-id="d86b6-119">Value</span><span class="sxs-lookup"><span data-stu-id="d86b6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86b6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d86b6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d86b6-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="d86b6-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="d86b6-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d86b6-122">Library</span></span><br/> | <dl> <span data-ttu-id="d86b6-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d86b6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d86b6-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d86b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86b6-125">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="d86b6-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> <dt>

[<span data-ttu-id="d86b6-126">**CPullPin:: Connect**</span><span class="sxs-lookup"><span data-stu-id="d86b6-126">**CPullPin::Connect**</span></span>](cpullpin-connect.md)
</dt> </dl>

 

 




