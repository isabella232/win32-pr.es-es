---
description: La plantilla de clase CGenericList que implementa una lista específica del tipo. Para obtener más información, vea CBaseList.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: Clase CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660833"
---
# <a name="cgenericlist-class"></a><span data-ttu-id="23d5b-104">Clase CGenericList</span><span class="sxs-lookup"><span data-stu-id="23d5b-104">CGenericList class</span></span>

![jerarquía de clases cgenericlist](images/list01.png)

<span data-ttu-id="23d5b-106">La `CGenericList` plantilla de clase que implementa una lista específica del tipo.</span><span class="sxs-lookup"><span data-stu-id="23d5b-106">The `CGenericList` class template that implements a type-specific list.</span></span> <span data-ttu-id="23d5b-107">Para obtener más información, vea [**CBaseList**](cbaselist.md).</span><span class="sxs-lookup"><span data-stu-id="23d5b-107">For more information, see [**CBaseList**](cbaselist.md).</span></span>

<span data-ttu-id="23d5b-108">Para usar esta plantilla, declare una variable de tipo `CGenericList` con un argumento de plantilla que defina el tipo de objeto de la lista.</span><span class="sxs-lookup"><span data-stu-id="23d5b-108">To use this template, declare a variable of type `CGenericList` with a template argument that defines the type of object in the list.</span></span> <span data-ttu-id="23d5b-109">Por ejemplo, la siguiente instrucción declara una lista de objetos [**CBaseFilter**](cbasefilter.md) :</span><span class="sxs-lookup"><span data-stu-id="23d5b-109">For example, the following statement declares a list of [**CBaseFilter**](cbasefilter.md) objects:</span></span>


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



<span data-ttu-id="23d5b-110">Por comodidad, Wxlist. h define los siguientes tipos de lista:</span><span class="sxs-lookup"><span data-stu-id="23d5b-110">For convenience, Wxlist.h defines the following list types:</span></span>

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| <span data-ttu-id="23d5b-111">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="23d5b-111">Public Methods</span></span>                                          | <span data-ttu-id="23d5b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="23d5b-112">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="23d5b-113">**CGenericList**</span><span class="sxs-lookup"><span data-stu-id="23d5b-113">**CGenericList**</span></span>](cgenericlist-cgenericlist.md)       | <span data-ttu-id="23d5b-114">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="23d5b-114">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="23d5b-115">**~ CGenericList**</span><span class="sxs-lookup"><span data-stu-id="23d5b-115">**~CGenericList**</span></span>](cgenericlist--cgenericlist.md)     | <span data-ttu-id="23d5b-116">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="23d5b-116">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="23d5b-117">**GetHeadPosition**</span><span class="sxs-lookup"><span data-stu-id="23d5b-117">**GetHeadPosition**</span></span>](cgenericlist-getheadposition.md) | <span data-ttu-id="23d5b-118">Recupera la posición del primer elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="23d5b-118">Retrieves the position of the first item in the list.</span></span>                    |
| [<span data-ttu-id="23d5b-119">**GetTailPosition**</span><span class="sxs-lookup"><span data-stu-id="23d5b-119">**GetTailPosition**</span></span>](cgenericlist-gettailposition.md) | <span data-ttu-id="23d5b-120">Recupera la posición del último elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="23d5b-120">Retrieves the position of the last item of the list.</span></span>                     |
| [<span data-ttu-id="23d5b-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="23d5b-121">**GetCount**</span></span>](cgenericlist-getcount.md)               | <span data-ttu-id="23d5b-122">Recupera el número de elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="23d5b-122">Retrieves the number of items in the list.</span></span>                               |
| [<span data-ttu-id="23d5b-123">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="23d5b-123">**GetNext**</span></span>](cgenericlist-getnext.md)                 | <span data-ttu-id="23d5b-124">Recupera el elemento en la posición especificada y hace avanzar la posición.</span><span class="sxs-lookup"><span data-stu-id="23d5b-124">Retrieves the item at the specified position, and advances the position.</span></span> |
| [<span data-ttu-id="23d5b-125">**Obtener**</span><span class="sxs-lookup"><span data-stu-id="23d5b-125">**Get**</span></span>](cgenericlist-get.md)                         | <span data-ttu-id="23d5b-126">Recupera el elemento en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="23d5b-126">Retrieves the item at the specified position.</span></span>                            |
| [<span data-ttu-id="23d5b-127">**GetHead**</span><span class="sxs-lookup"><span data-stu-id="23d5b-127">**GetHead**</span></span>](cgenericlist-gethead.md)                 | <span data-ttu-id="23d5b-128">Recupera el elemento situado en el encabezado de la lista.</span><span class="sxs-lookup"><span data-stu-id="23d5b-128">Retrieves the item at the head of the list.</span></span>                              |
| [<span data-ttu-id="23d5b-129">**RemoveHead**</span><span class="sxs-lookup"><span data-stu-id="23d5b-129">**RemoveHead**</span></span>](cgenericlist-removehead.md)           | <span data-ttu-id="23d5b-130">Quita el primer elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="23d5b-130">Removes the first item in the list.</span></span>                                      |
| [<span data-ttu-id="23d5b-131">**RemoveTail**</span><span class="sxs-lookup"><span data-stu-id="23d5b-131">**RemoveTail**</span></span>](cgenericlist-removetail.md)           | <span data-ttu-id="23d5b-132">Quita el último elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="23d5b-132">Removes the last item in the list.</span></span>                                       |
| [<span data-ttu-id="23d5b-133">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="23d5b-133">**Remove**</span></span>](cgenericlist-remove.md)                   | <span data-ttu-id="23d5b-134">Quita el elemento de en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="23d5b-134">Removes the item at the specified position.</span></span>                              |
| [<span data-ttu-id="23d5b-135">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="23d5b-135">**AddBefore**</span></span>](cgenericlist-addbefore.md)             | <span data-ttu-id="23d5b-136">Inserta un elemento o una lista antes de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="23d5b-136">Inserts an item or list before the specified position.</span></span>                   |
| [<span data-ttu-id="23d5b-137">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="23d5b-137">**AddAfter**</span></span>](cgenericlist-addafter.md)               | <span data-ttu-id="23d5b-138">Inserta un elemento o una lista después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="23d5b-138">Inserts an item or list after the specified position.</span></span>                    |
| [<span data-ttu-id="23d5b-139">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="23d5b-139">**AddHead**</span></span>](cgenericlist-addhead.md)                 | <span data-ttu-id="23d5b-140">Agrega un elemento o una lista al principio de la lista.</span><span class="sxs-lookup"><span data-stu-id="23d5b-140">Adds an item or list to the front of the list.</span></span>                           |
| [<span data-ttu-id="23d5b-141">**Addtail (**</span><span class="sxs-lookup"><span data-stu-id="23d5b-141">**AddTail**</span></span>](cgenericlist-addtail.md)                 | <span data-ttu-id="23d5b-142">Anexa un elemento o una lista al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="23d5b-142">Appends an item or list to the end of the list.</span></span>                          |
| [<span data-ttu-id="23d5b-143">**Buscar**</span><span class="sxs-lookup"><span data-stu-id="23d5b-143">**Find**</span></span>](cgenericlist-find.md)                       | <span data-ttu-id="23d5b-144">Recupera la primera posición que contiene el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="23d5b-144">Retrieves the first position that holds the specified item.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="23d5b-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23d5b-145">Requirements</span></span>



| <span data-ttu-id="23d5b-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="23d5b-146">Requirement</span></span> | <span data-ttu-id="23d5b-147">Value</span><span class="sxs-lookup"><span data-stu-id="23d5b-147">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23d5b-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23d5b-148">Header</span></span><br/>  | <dl> <span data-ttu-id="23d5b-149"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23d5b-149"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="23d5b-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23d5b-150">Library</span></span><br/> | <dl> <span data-ttu-id="23d5b-151"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="23d5b-151"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




