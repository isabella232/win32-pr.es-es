---
description: El método CBaseList implementa una lista abtract. La plantilla de clase CGenericList, que se deriva de CBaseList, proporciona comprobación de tipos y una interfaz más sencilla que la clase CBaseList.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: Clase CBaseList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670586"
---
# <a name="cbaselist-class"></a><span data-ttu-id="07d39-104">Clase CBaseList</span><span class="sxs-lookup"><span data-stu-id="07d39-104">CBaseList class</span></span>

![jerarquía de clases cbaselist](images/list01.png)

<span data-ttu-id="07d39-106">El método **CBaseList** implementa una lista abtract.</span><span class="sxs-lookup"><span data-stu-id="07d39-106">The **CBaseList** method implements an abtract list.</span></span> <span data-ttu-id="07d39-107">La plantilla de clase [**CGenericList**](cgenericlist.md) , que se deriva de **CBaseList**, proporciona comprobación de tipos y una interfaz más sencilla que la clase **CBaseList** .</span><span class="sxs-lookup"><span data-stu-id="07d39-107">The [**CGenericList**](cgenericlist.md) class template, which derives from **CBaseList**, provides type checking and a simpler interface than the **CBaseList** class.</span></span>

<span data-ttu-id="07d39-108">La clase **CBaseList** se modela después de la clase **CObList** en la biblioteca Microsoft Foundation Classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="07d39-108">The **CBaseList** class is modeled after the **CObList** class in the Microsoft Foundation Classes (MFC) library.</span></span> <span data-ttu-id="07d39-109">Las posiciones dentro de la lista se representan mediante una estructura de posición.</span><span class="sxs-lookup"><span data-stu-id="07d39-109">Positions within the list are represented by a POSITION structure.</span></span> <span data-ttu-id="07d39-110">El llamador no debe tener acceso a los miembros internos de la estructura de la posición; se trata como un puntero a un nodo de lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-110">The caller should not access the internal members of the POSITION structure; treat it as a pointer to a list node.</span></span> <span data-ttu-id="07d39-111">La posición de un objeto en la lista sigue siendo válida hasta que se elimina el objeto.</span><span class="sxs-lookup"><span data-stu-id="07d39-111">The position of an object in the list remains valid until the object is deleted.</span></span>

<span data-ttu-id="07d39-112">La lista no requiere compatibilidad con los objetos que contiene.</span><span class="sxs-lookup"><span data-stu-id="07d39-112">The list does not require any support by the objects it contains.</span></span> <span data-ttu-id="07d39-113">No realiza ninguna administración de almacenamiento ni copia de los objetos.</span><span class="sxs-lookup"><span data-stu-id="07d39-113">It performs no storage management or copying on the objects.</span></span> <span data-ttu-id="07d39-114">Los objetos pueden estar en varias listas.</span><span class="sxs-lookup"><span data-stu-id="07d39-114">Objects can be in multiple lists.</span></span>

<span data-ttu-id="07d39-115">Aproximadamente la mitad de los métodos de esta clase actúan en objetos únicos.</span><span class="sxs-lookup"><span data-stu-id="07d39-115">Roughly half of the methods in this class act on single objects.</span></span> <span data-ttu-id="07d39-116">Estos métodos tienen el sufijo-I en el nombre del método.</span><span class="sxs-lookup"><span data-stu-id="07d39-116">These methods have the suffix - I in the method name.</span></span> <span data-ttu-id="07d39-117">Los otros métodos actúan en listas completas.</span><span class="sxs-lookup"><span data-stu-id="07d39-117">The other methods act on entire lists.</span></span> <span data-ttu-id="07d39-118">Por ejemplo, el método [**CBaseList:: AddAfter**](cbaselist-addafter.md) anexa una lista a otra lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-118">For example, the [**CBaseList::AddAfter**](cbaselist-addafter.md) method appends a list to another list.</span></span> <span data-ttu-id="07d39-119">Las operaciones de un solo objeto devuelven valores de posición o **null** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="07d39-119">Single-object operations return POSITION values, or **NULL** on failure.</span></span> <span data-ttu-id="07d39-120">Las operaciones de lista devuelven **true** si se realizan correctamente o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="07d39-120">List operations return **TRUE** if successful or **FALSE** otherwise.</span></span>



| <span data-ttu-id="07d39-121">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="07d39-121">Protected Member Variables</span></span>                             | <span data-ttu-id="07d39-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="07d39-122">Description</span></span>                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="07d39-123">**recuento de m \_**</span><span class="sxs-lookup"><span data-stu-id="07d39-123">**m\_Count**</span></span>](cbaselist-m-count.md)                  | <span data-ttu-id="07d39-124">Número de elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-124">Number of items in the list.</span></span>                                              |
| [<span data-ttu-id="07d39-125">**m \_ pFirst**</span><span class="sxs-lookup"><span data-stu-id="07d39-125">**m\_pFirst**</span></span>](cbaselist-m-pfirst.md)                | <span data-ttu-id="07d39-126">Puntero al primer nodo de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-126">Pointer to the first node in the list.</span></span>                                    |
| [<span data-ttu-id="07d39-127">**m \_ pLast**</span><span class="sxs-lookup"><span data-stu-id="07d39-127">**m\_pLast**</span></span>](cbaselist-m-plast.md)                  | <span data-ttu-id="07d39-128">Puntero al último nodo de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-128">Pointer to the last node in the list.</span></span>                                     |
| <span data-ttu-id="07d39-129">Métodos protegidos</span><span class="sxs-lookup"><span data-stu-id="07d39-129">Protected Methods</span></span>                                      | <span data-ttu-id="07d39-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="07d39-130">Description</span></span>                                                               |
| [<span data-ttu-id="07d39-131">**GetNextI**</span><span class="sxs-lookup"><span data-stu-id="07d39-131">**GetNextI**</span></span>](cbaselist-getnexti.md)                 | <span data-ttu-id="07d39-132">Recupera el elemento en la posición especificada y hace avanzar la posición.</span><span class="sxs-lookup"><span data-stu-id="07d39-132">Retrieves the item at the specified position, and advances the position.</span></span>  |
| [<span data-ttu-id="07d39-133">**GetI**</span><span class="sxs-lookup"><span data-stu-id="07d39-133">**GetI**</span></span>](cbaselist-geti.md)                         | <span data-ttu-id="07d39-134">Recupera el elemento en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="07d39-134">Retrieves the item at the specified position.</span></span>                             |
| [<span data-ttu-id="07d39-135">**Buscar**</span><span class="sxs-lookup"><span data-stu-id="07d39-135">**FindI**</span></span>](cbaselist-findi.md)                       | <span data-ttu-id="07d39-136">Recupera la primera posición que contiene el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="07d39-136">Retrieves the first position that holds the specified item.</span></span>               |
| [<span data-ttu-id="07d39-137">**RemoveHeadI**</span><span class="sxs-lookup"><span data-stu-id="07d39-137">**RemoveHeadI**</span></span>](cbaselist-removeheadi.md)           | <span data-ttu-id="07d39-138">Quita el primer elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-138">Removes the first item in the list.</span></span>                                       |
| [<span data-ttu-id="07d39-139">**RemoveTailI**</span><span class="sxs-lookup"><span data-stu-id="07d39-139">**RemoveTailI**</span></span>](cbaselist-removetaili.md)           | <span data-ttu-id="07d39-140">Quita el último elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-140">Removes the last item in the list.</span></span>                                        |
| [<span data-ttu-id="07d39-141">**Cambiar movimiento**</span><span class="sxs-lookup"><span data-stu-id="07d39-141">**RemoveI**</span></span>](cbaselist-removei.md)                   | <span data-ttu-id="07d39-142">Quita el elemento de en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="07d39-142">Removes the item at the specified position.</span></span>                               |
| [<span data-ttu-id="07d39-143">**AddTailI**</span><span class="sxs-lookup"><span data-stu-id="07d39-143">**AddTailI**</span></span>](cbaselist-addtaili.md)                 | <span data-ttu-id="07d39-144">Agrega un elemento al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-144">Adds an item to the end of the list.</span></span>                                      |
| [<span data-ttu-id="07d39-145">**AddHeadI**</span><span class="sxs-lookup"><span data-stu-id="07d39-145">**AddHeadI**</span></span>](cbaselist-addheadi.md)                 | <span data-ttu-id="07d39-146">Agrega un elemento al principio de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-146">Adds an item to the front of the list.</span></span>                                    |
| [<span data-ttu-id="07d39-147">**AddAfterI**</span><span class="sxs-lookup"><span data-stu-id="07d39-147">**AddAfterI**</span></span>](cbaselist-addafteri.md)               | <span data-ttu-id="07d39-148">Inserta un elemento después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="07d39-148">Inserts an item after the specified position.</span></span>                             |
| [<span data-ttu-id="07d39-149">**AddBeforeI**</span><span class="sxs-lookup"><span data-stu-id="07d39-149">**AddBeforeI**</span></span>](cbaselist-addbeforei.md)             | <span data-ttu-id="07d39-150">Inserta un elemento antes de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="07d39-150">Inserts an item before the specified position.</span></span>                            |
| <span data-ttu-id="07d39-151">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="07d39-151">Public Methods</span></span>                                         | <span data-ttu-id="07d39-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="07d39-152">Description</span></span>                                                               |
| [<span data-ttu-id="07d39-153">**CBaseList**</span><span class="sxs-lookup"><span data-stu-id="07d39-153">**CBaseList**</span></span>](cbaselist-cbaselist.md)               | <span data-ttu-id="07d39-154">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="07d39-154">Constructor method.</span></span>                                                       |
| [<span data-ttu-id="07d39-155">**~ CBaseList**</span><span class="sxs-lookup"><span data-stu-id="07d39-155">**~ CBaseList**</span></span>](cbaselist--cbaselist.md)            | <span data-ttu-id="07d39-156">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="07d39-156">Destructor method.</span></span>                                                        |
| [<span data-ttu-id="07d39-157">**RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="07d39-157">**RemoveAll**</span></span>](cbaselist-removeall.md)               | <span data-ttu-id="07d39-158">Quita todos los nodos de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-158">Removes all nodes from the list.</span></span>                                          |
| [<span data-ttu-id="07d39-159">**GetHeadPositionI**</span><span class="sxs-lookup"><span data-stu-id="07d39-159">**GetHeadPositionI**</span></span>](cbaselist-getheadpositioni.md) | <span data-ttu-id="07d39-160">Recupera la posición del primer elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-160">Retrieves the position of the first item in the list.</span></span>                     |
| [<span data-ttu-id="07d39-161">**GetTailPositionI**</span><span class="sxs-lookup"><span data-stu-id="07d39-161">**GetTailPositionI**</span></span>](cbaselist-gettailpositioni.md) | <span data-ttu-id="07d39-162">Recupera la posición del último elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-162">Retrieves the position of the last item of the list.</span></span>                      |
| [<span data-ttu-id="07d39-163">**GetCountI**</span><span class="sxs-lookup"><span data-stu-id="07d39-163">**GetCountI**</span></span>](cbaselist-getcounti.md)               | <span data-ttu-id="07d39-164">Recupera el número de elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-164">Retrieves the number of items in the list.</span></span>                                |
| [<span data-ttu-id="07d39-165">**Next**</span><span class="sxs-lookup"><span data-stu-id="07d39-165">**Next**</span></span>](cbaselist-next.md)                         | <span data-ttu-id="07d39-166">Recupera la posición siguiente en la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-166">Retrieves the next position in the list.</span></span>                                  |
| [<span data-ttu-id="07d39-167">**Anterior**</span><span class="sxs-lookup"><span data-stu-id="07d39-167">**Prev**</span></span>](cbaselist-prev.md)                         | <span data-ttu-id="07d39-168">Recupera la posición anterior en la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-168">Retrieves the previous position in the list.</span></span>                              |
| [<span data-ttu-id="07d39-169">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="07d39-169">**AddHead**</span></span>](cbaselist-addhead.md)                   | <span data-ttu-id="07d39-170">Inserta otra lista al principio de esta lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-170">Inserts another list at the front of this list.</span></span>                           |
| [<span data-ttu-id="07d39-171">**Addtail (**</span><span class="sxs-lookup"><span data-stu-id="07d39-171">**AddTail**</span></span>](cbaselist-addtail.md)                   | <span data-ttu-id="07d39-172">Anexa otra lista al final de esta lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-172">Appends another list to the end of this list.</span></span>                             |
| [<span data-ttu-id="07d39-173">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="07d39-173">**AddAfter**</span></span>](cbaselist-addafter.md)                 | <span data-ttu-id="07d39-174">Inserta una lista después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="07d39-174">Inserts a list after the specified position.</span></span>                              |
| [<span data-ttu-id="07d39-175">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="07d39-175">**AddBefore**</span></span>](cbaselist-addbefore.md)               | <span data-ttu-id="07d39-176">Inserta una lista antes de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="07d39-176">Inserts a list before the specified position.</span></span>                             |
| [<span data-ttu-id="07d39-177">**MoveToTail**</span><span class="sxs-lookup"><span data-stu-id="07d39-177">**MoveToTail**</span></span>](cbaselist-movetotail.md)             | <span data-ttu-id="07d39-178">Divide la lista y anexa la parte del encabezado a la cola de otra lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-178">Splits the list and appends the head portion to the tail of another list.</span></span> |
| [<span data-ttu-id="07d39-179">**MoveToHead**</span><span class="sxs-lookup"><span data-stu-id="07d39-179">**MoveToHead**</span></span>](cbaselist-movetohead.md)             | <span data-ttu-id="07d39-180">Divide la lista e inserta la parte del final en el encabezado de otra lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-180">Splits the list and inserts the tail portion at the head of another list.</span></span> |
| [<span data-ttu-id="07d39-181">**Viceversa**</span><span class="sxs-lookup"><span data-stu-id="07d39-181">**Reverse**</span></span>](cbaselist-reverse.md)                   | <span data-ttu-id="07d39-182">Invierte el orden de la lista.</span><span class="sxs-lookup"><span data-stu-id="07d39-182">Reverses the order of the list.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="07d39-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07d39-183">Requirements</span></span>



| <span data-ttu-id="07d39-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d39-184">Requirement</span></span> | <span data-ttu-id="07d39-185">Value</span><span class="sxs-lookup"><span data-stu-id="07d39-185">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d39-186">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07d39-186">Header</span></span><br/>  | <dl> <span data-ttu-id="07d39-187"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07d39-187"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="07d39-188">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07d39-188">Library</span></span><br/> | <dl> <span data-ttu-id="07d39-189"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="07d39-189"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d39-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="07d39-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d39-191">Clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="07d39-191">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




