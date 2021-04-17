---
description: Método de constructor.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Constructor CMemAllocator. CMemAllocator (Amfilter. h)
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
ms.openlocfilehash: b650e23761c3fe5b3f5014666f90c679f088c4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670757"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="27c57-103">Constructor CMemAllocator. CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="27c57-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="27c57-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="27c57-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c57-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27c57-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="27c57-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27c57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c57-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="27c57-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="27c57-108">Puntero a una cadena que contiene el nombre del asignador.</span><span class="sxs-lookup"><span data-stu-id="27c57-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="27c57-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="27c57-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="27c57-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="27c57-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="27c57-111">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="27c57-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="27c57-112">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="27c57-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="27c57-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="27c57-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="27c57-114">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="27c57-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27c57-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27c57-115">Requirements</span></span>



| <span data-ttu-id="27c57-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c57-116">Requirement</span></span> | <span data-ttu-id="27c57-117">Value</span><span class="sxs-lookup"><span data-stu-id="27c57-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27c57-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27c57-118">Header</span></span><br/>  | <dl> <span data-ttu-id="27c57-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27c57-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="27c57-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27c57-120">Library</span></span><br/> | <dl> <span data-ttu-id="27c57-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="27c57-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c57-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="27c57-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c57-123">**Clase CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="27c57-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




