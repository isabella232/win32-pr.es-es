---
description: 'Constructor CMemAllocator.CMemAllocator: método constructor.'
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Constructor CMemAllocator.CMemAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1151572c32efe69cceb89e7a5ea5a045955b5f43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095403"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="b9e19-103">Constructor CMemAllocator.CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="b9e19-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="b9e19-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="b9e19-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e19-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9e19-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b9e19-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9e19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e19-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="b9e19-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b9e19-108">Puntero a una cadena que contiene el nombre del asignador.</span><span class="sxs-lookup"><span data-stu-id="b9e19-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="b9e19-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="b9e19-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b9e19-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="b9e19-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="b9e19-111">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="b9e19-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="b9e19-112">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="b9e19-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b9e19-113">*Phr*</span><span class="sxs-lookup"><span data-stu-id="b9e19-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b9e19-114">Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o el error del método.</span><span class="sxs-lookup"><span data-stu-id="b9e19-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9e19-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9e19-115">Requirements</span></span>



| <span data-ttu-id="b9e19-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9e19-116">Requirement</span></span> | <span data-ttu-id="b9e19-117">Value</span><span class="sxs-lookup"><span data-stu-id="b9e19-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e19-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9e19-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b9e19-119"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9e19-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b9e19-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9e19-120">Library</span></span><br/> | <dl> <span data-ttu-id="b9e19-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b9e19-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9e19-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b9e19-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e19-123">**CMemAllocator (clase)**</span><span class="sxs-lookup"><span data-stu-id="b9e19-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




