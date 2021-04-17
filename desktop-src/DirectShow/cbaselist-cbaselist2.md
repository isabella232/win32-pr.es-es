---
description: Método de constructor.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Constructor CBaseList. CBaseList (Wxlist. h)
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
ms.openlocfilehash: 3afc0a4acf54e186e122f676ac14e9e80aaeafdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660675"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="35db0-103">Constructor CBaseList. CBaseList</span><span class="sxs-lookup"><span data-stu-id="35db0-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="35db0-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="35db0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="35db0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35db0-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="35db0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35db0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35db0-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="35db0-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="35db0-108">Puntero al nombre de la lista.</span><span class="sxs-lookup"><span data-stu-id="35db0-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35db0-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35db0-109">Remarks</span></span>

<span data-ttu-id="35db0-110">Por motivos de eficacia, la `CBaseList` clase mantiene una memoria caché de nodos de lista.</span><span class="sxs-lookup"><span data-stu-id="35db0-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="35db0-111">Esta versión del constructor utiliza un tamaño de caché predeterminado.</span><span class="sxs-lookup"><span data-stu-id="35db0-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="35db0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35db0-112">Requirements</span></span>



| <span data-ttu-id="35db0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="35db0-113">Requirement</span></span> | <span data-ttu-id="35db0-114">Value</span><span class="sxs-lookup"><span data-stu-id="35db0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35db0-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35db0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="35db0-116"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35db0-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="35db0-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35db0-117">Library</span></span><br/> | <dl> <span data-ttu-id="35db0-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="35db0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35db0-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="35db0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35db0-120">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="35db0-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




