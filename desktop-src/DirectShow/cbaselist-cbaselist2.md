---
description: 'Constructor CBaseList.CBaseList: método constructor.'
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Constructor CBaseList.CBaseList (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096333"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="80ecb-103">Constructor CBaseList.CBaseList</span><span class="sxs-lookup"><span data-stu-id="80ecb-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="80ecb-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="80ecb-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80ecb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80ecb-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="80ecb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80ecb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80ecb-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="80ecb-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="80ecb-108">Puntero al nombre de la lista.</span><span class="sxs-lookup"><span data-stu-id="80ecb-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80ecb-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="80ecb-109">Remarks</span></span>

<span data-ttu-id="80ecb-110">Para mejorar la eficacia, `CBaseList` la clase mantiene una caché de nodos de lista.</span><span class="sxs-lookup"><span data-stu-id="80ecb-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="80ecb-111">Esta versión del constructor usa un tamaño de caché predeterminado.</span><span class="sxs-lookup"><span data-stu-id="80ecb-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="80ecb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80ecb-112">Requirements</span></span>



| <span data-ttu-id="80ecb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="80ecb-113">Requirement</span></span> | <span data-ttu-id="80ecb-114">Value</span><span class="sxs-lookup"><span data-stu-id="80ecb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80ecb-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80ecb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="80ecb-116"><dt>Wxlist.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="80ecb-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="80ecb-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80ecb-117">Library</span></span><br/> | <dl> <span data-ttu-id="80ecb-118"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="80ecb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80ecb-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="80ecb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80ecb-120">**CBaseList (clase)**</span><span class="sxs-lookup"><span data-stu-id="80ecb-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




