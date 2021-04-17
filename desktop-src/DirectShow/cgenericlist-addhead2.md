---
description: El método AddHead agrega una lista al principio de la lista.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: 'Método CGenericList. AddHead (Wxlist. h): parámetro plist'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105670275"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a><span data-ttu-id="de047-103">Método CGenericList. AddHead (Wxlist. h): parámetro plist</span><span class="sxs-lookup"><span data-stu-id="de047-103">CGenericList.AddHead method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="de047-104">El `AddHead` método agrega una lista al principio de la lista.</span><span class="sxs-lookup"><span data-stu-id="de047-104">The `AddHead` method adds a list to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="de047-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de047-105">Syntax</span></span>


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="de047-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de047-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="de047-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="de047-108">Puntero a la lista de elementos que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="de047-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de047-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de047-109">Return value</span></span>

<span data-ttu-id="de047-110">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="de047-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="de047-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de047-111">Requirements</span></span>

| <span data-ttu-id="de047-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="de047-112">Requirement</span></span> | <span data-ttu-id="de047-113">Value</span><span class="sxs-lookup"><span data-stu-id="de047-113">Value</span></span> |
|-|-|
| <span data-ttu-id="de047-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de047-114">Header</span></span> | <span data-ttu-id="de047-115">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="de047-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="de047-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de047-116">Library</span></span>| <span data-ttu-id="de047-117">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="de047-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="de047-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="de047-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de047-119">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="de047-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




