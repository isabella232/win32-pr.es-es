---
description: La clase CBaseObject es una clase abstracta para implementar objetos de DirectShow. Para implementar objetos del modelo de objetos componentes (COM), use la clase CUnknown, que se deriva de CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Clase CBaseObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670668"
---
# <a name="cbaseobject-class"></a><span data-ttu-id="4e824-104">Clase CBaseObject</span><span class="sxs-lookup"><span data-stu-id="4e824-104">CBaseObject class</span></span>

<span data-ttu-id="4e824-105">La clase **CBaseObject** es una clase abstracta para implementar objetos de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4e824-105">The **CBaseObject** class is an abstract class for implementing DirectShow objects.</span></span> <span data-ttu-id="4e824-106">Para implementar objetos del modelo de objetos componentes (COM), use la clase [**CUnknown**](cunknown.md) , que se deriva de **CBaseObject**.</span><span class="sxs-lookup"><span data-stu-id="4e824-106">To implement Component Object Model (COM) objects, use the [**CUnknown**](cunknown.md) class, which derives from **CBaseObject**.</span></span>



| <span data-ttu-id="4e824-107">Métodos de clase</span><span class="sxs-lookup"><span data-stu-id="4e824-107">Class Methods</span></span>                                      | <span data-ttu-id="4e824-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e824-108">Description</span></span>                            |
|----------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="4e824-109">**CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="4e824-109">**CBaseObject**</span></span>](cbaseobject-cbaseobject.md)     | <span data-ttu-id="4e824-110">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="4e824-110">Constructor method.</span></span>                    |
| [<span data-ttu-id="4e824-111">**~ CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="4e824-111">**~CBaseObject**</span></span>](cbaseobject--cbaseobject.md)   | <span data-ttu-id="4e824-112">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="4e824-112">Destructor method.</span></span>                     |
| [<span data-ttu-id="4e824-113">**ObjectsActive**</span><span class="sxs-lookup"><span data-stu-id="4e824-113">**ObjectsActive**</span></span>](cbaseobject-objectsactive.md) | <span data-ttu-id="4e824-114">Recupera el recuento de objetos activos.</span><span class="sxs-lookup"><span data-stu-id="4e824-114">Retrieves the count of active objects.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4e824-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e824-115">Remarks</span></span>

<span data-ttu-id="4e824-116">La mayoría de las clases base de DirectShow derivan de **CBaseObject**.</span><span class="sxs-lookup"><span data-stu-id="4e824-116">Most of the DirectShow base classes derive from **CBaseObject**.</span></span> <span data-ttu-id="4e824-117">Esta clase proporciona ayuda para la depuración manteniendo un recuento de todos los objetos de DirectShow activos durante el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4e824-117">This class provides debugging assistance by keeping a count of all the DirectShow objects active during run time.</span></span> <span data-ttu-id="4e824-118">El recuento de objetos se almacena en una variable miembro de clase estática:</span><span class="sxs-lookup"><span data-stu-id="4e824-118">The object count is stored in a class-static member variable:</span></span>


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



<span data-ttu-id="4e824-119">En las compilaciones de depuración, el archivo DLL validará si se descarga mientras el recuento de objetos es mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="4e824-119">In debug builds, the DLL will assert if it is unloaded while the object count is greater than zero.</span></span> <span data-ttu-id="4e824-120">Esto facilita el seguimiento de las fugas producidas por problemas de recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="4e824-120">This makes it easier to track down leaks caused by reference-counting problems.</span></span>

<span data-ttu-id="4e824-121">El constructor **CBaseObject** toma un argumento, un nombre de depuración para el objeto.</span><span class="sxs-lookup"><span data-stu-id="4e824-121">The **CBaseObject** constructor takes one argument, a debugging name for the object.</span></span> <span data-ttu-id="4e824-122">Este nombre se almacena en una tabla global en el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="4e824-122">This name is stored in a global table in the DLL.</span></span> <span data-ttu-id="4e824-123">La función [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) da formato a una lista de los objetos activos en el archivo dll y lo envía a la salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="4e824-123">The [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function formats a list of the objects active in the DLL, and sends it to the debug output.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e824-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e824-124">Requirements</span></span>



| <span data-ttu-id="4e824-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e824-125">Requirement</span></span> | <span data-ttu-id="4e824-126">Value</span><span class="sxs-lookup"><span data-stu-id="4e824-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e824-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e824-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4e824-128"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e824-128"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4e824-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e824-129">Library</span></span><br/> | <dl> <span data-ttu-id="4e824-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4e824-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e824-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e824-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e824-132">Clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4e824-132">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




