---
description: 'Constructor CImageAllocator.CImageAllocator: método constructor.'
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Constructor CImageAllocator.CImageAllocator (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085763"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="0a2f5-103">Constructor CImageAllocator.CImageAllocator</span><span class="sxs-lookup"><span data-stu-id="0a2f5-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="0a2f5-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="0a2f5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a2f5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a2f5-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="0a2f5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a2f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a2f5-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="0a2f5-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="0a2f5-108">Puntero al filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="0a2f5-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="0a2f5-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="0a2f5-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0a2f5-110">Puntero a una cadena que contiene el nombre de depuración del asignador.</span><span class="sxs-lookup"><span data-stu-id="0a2f5-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="0a2f5-111">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0a2f5-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a2f5-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="0a2f5-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0a2f5-113">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0a2f5-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="0a2f5-114">Establezca el valor en S \_ OK antes de crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="0a2f5-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="0a2f5-115">Si se produce un error en el constructor, el valor se establece en un código de error.</span><span class="sxs-lookup"><span data-stu-id="0a2f5-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a2f5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a2f5-116">Requirements</span></span>



| <span data-ttu-id="0a2f5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a2f5-117">Requirement</span></span> | <span data-ttu-id="0a2f5-118">Value</span><span class="sxs-lookup"><span data-stu-id="0a2f5-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a2f5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a2f5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0a2f5-120"><dt>Winutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a2f5-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a2f5-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a2f5-121">Library</span></span><br/> | <dl> <span data-ttu-id="0a2f5-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0a2f5-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a2f5-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a2f5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a2f5-124">**CImageAllocator (clase)**</span><span class="sxs-lookup"><span data-stu-id="0a2f5-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




