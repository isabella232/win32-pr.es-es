---
description: Obtenga información sobre el método de constructor para CGenericList. CGenericList (Wxlist. h). Este método usa el parámetro ' pName '.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: 'Constructor CGenericList. CGenericList (Wxlist. h): parámetro pName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103914834"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a><span data-ttu-id="92b00-104">Constructor CGenericList. CGenericList (Wxlist. h): parámetro pName</span><span class="sxs-lookup"><span data-stu-id="92b00-104">CGenericList.CGenericList constructor (Wxlist.h) - pName parameter</span></span>

<span data-ttu-id="92b00-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="92b00-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b00-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92b00-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="92b00-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92b00-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b00-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="92b00-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="92b00-109">Puntero al nombre de la lista.</span><span class="sxs-lookup"><span data-stu-id="92b00-109">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92b00-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92b00-110">Remarks</span></span>

<span data-ttu-id="92b00-111">Por motivos de eficacia, la `CGenericList` clase mantiene una memoria caché de nodos de lista.</span><span class="sxs-lookup"><span data-stu-id="92b00-111">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="92b00-112">Esta versión del constructor utiliza un tamaño de caché predeterminado.</span><span class="sxs-lookup"><span data-stu-id="92b00-112">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b00-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92b00-113">Requirements</span></span>

| <span data-ttu-id="92b00-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b00-114">Requirement</span></span> | <span data-ttu-id="92b00-115">Value</span><span class="sxs-lookup"><span data-stu-id="92b00-115">Value</span></span> |
|-|-|
| <span data-ttu-id="92b00-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92b00-116">Header</span></span> | <span data-ttu-id="92b00-117">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="92b00-117">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="92b00-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92b00-118">Library</span></span>| <span data-ttu-id="92b00-119">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="92b00-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="92b00-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="92b00-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b00-121">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="92b00-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




