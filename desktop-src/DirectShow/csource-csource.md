---
description: Método de constructor.
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: Constructor CSource. CSource (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 992775659d5f9838ef63b15c5395998f1faf6200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689998"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="5442f-103">Constructor CSource. CSource</span><span class="sxs-lookup"><span data-stu-id="5442f-103">CSource.CSource constructor</span></span>

<span data-ttu-id="5442f-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="5442f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5442f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5442f-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="5442f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5442f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5442f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="5442f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5442f-108">Puntero a una cadena que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="5442f-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="5442f-109">Para obtener más información, vea [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="5442f-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="5442f-110">*lpunk*</span><span class="sxs-lookup"><span data-stu-id="5442f-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="5442f-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="5442f-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="5442f-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="5442f-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="5442f-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="5442f-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5442f-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="5442f-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="5442f-115">Identificador de clase del filtro.</span><span class="sxs-lookup"><span data-stu-id="5442f-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5442f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5442f-116">Requirements</span></span>



| <span data-ttu-id="5442f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5442f-117">Requirement</span></span> | <span data-ttu-id="5442f-118">Value</span><span class="sxs-lookup"><span data-stu-id="5442f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5442f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5442f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5442f-120"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5442f-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5442f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5442f-121">Library</span></span><br/> | <dl> <span data-ttu-id="5442f-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5442f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5442f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5442f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5442f-124">**Clase CSource**</span><span class="sxs-lookup"><span data-stu-id="5442f-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




