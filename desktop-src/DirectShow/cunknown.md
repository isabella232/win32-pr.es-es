---
description: La clase CUnknown implementa la interfaz IUnknown. La mayoría de los objetos del modelo de objetos componentes (COM) de DirectShow se derivan de CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Clase CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680875"
---
# <a name="cunknown-class"></a><span data-ttu-id="cd74b-104">Clase CUnknown</span><span class="sxs-lookup"><span data-stu-id="cd74b-104">CUnknown class</span></span>

![jerarquía de clases cunknown](images/cbase01.png)

<span data-ttu-id="cd74b-106">La clase **CUnknown** implementa la interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="cd74b-106">The **CUnknown** class implements the **IUnknown** interface.</span></span> <span data-ttu-id="cd74b-107">La mayoría de los objetos del modelo de objetos componentes (COM) de DirectShow se derivan de **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cd74b-107">Most Component Object Model (COM) objects in DirectShow derive from **CUnknown**.</span></span>

<span data-ttu-id="cd74b-108">Si implementa un objeto COM, puede que desee derivarlo de **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cd74b-108">If you implement a COM object, you might want to derive it from **CUnknown**.</span></span> <span data-ttu-id="cd74b-109">La derivación de **CUnknown** proporciona una implementación segura para subprocesos y evita el problema de implementar **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cd74b-109">Deriving from **CUnknown** provides a thread-safe implementation, and saves you the trouble of implementing **IUnknown**.</span></span>

<span data-ttu-id="cd74b-110">Para obtener una explicación detallada sobre cómo usar esta clase base, vea [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="cd74b-110">For a detailed discussion of how to use this base class, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span> <span data-ttu-id="cd74b-111">A continuación se muestra un breve resumen:</span><span class="sxs-lookup"><span data-stu-id="cd74b-111">What follows is a brief summary:</span></span>

-   <span data-ttu-id="cd74b-112">Incluya la macro [**declare \_ IUNKNOWN**](declare-iunknown.md) en la sección Public de la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="cd74b-112">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public section of your class definition.</span></span> <span data-ttu-id="cd74b-113">Esta macro declara los tres métodos de la interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="cd74b-113">This macro declares the three methods of the **IUnknown** interface.</span></span>
-   <span data-ttu-id="cd74b-114">Invalide el método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para admitir interfaces que no sean **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cd74b-114">Override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method to support interfaces other than **IUnknown**.</span></span> <span data-ttu-id="cd74b-115">Dentro de este método, llame a la función [**GetInterface**](getinterface.md) para recuperar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="cd74b-115">Within this method, call the [**GetInterface**](getinterface.md) function to retrieve interface pointers.</span></span>
-   <span data-ttu-id="cd74b-116">En el constructor de clase, invoque el método de constructor **CUnknown** .</span><span class="sxs-lookup"><span data-stu-id="cd74b-116">In your class constructor, invoke the **CUnknown** constructor method.</span></span>



| <span data-ttu-id="cd74b-117">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="cd74b-117">Protected Member Variables</span></span>                                                  | <span data-ttu-id="cd74b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd74b-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="cd74b-119">**m \_ cRef**</span><span class="sxs-lookup"><span data-stu-id="cd74b-119">**m\_cRef**</span></span>](cunknown-m-cref.md)                                          | <span data-ttu-id="cd74b-120">Recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="cd74b-120">Reference count.</span></span>                                                   |
| <span data-ttu-id="cd74b-121">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="cd74b-121">Public Methods</span></span>                                                              | <span data-ttu-id="cd74b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd74b-122">Description</span></span>                                                        |
| [<span data-ttu-id="cd74b-123">**CUnknown**</span><span class="sxs-lookup"><span data-stu-id="cd74b-123">**CUnknown**</span></span>](cunknown-cunknown.md)                                       | <span data-ttu-id="cd74b-124">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="cd74b-124">Constructor method.</span></span>                                                |
| [<span data-ttu-id="cd74b-125">**~ CUnknown**</span><span class="sxs-lookup"><span data-stu-id="cd74b-125">**~ CUnknown**</span></span>](cunknown--cunknown.md)                                    | <span data-ttu-id="cd74b-126">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="cd74b-126">Destructor method.</span></span> <span data-ttu-id="cd74b-127">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="cd74b-127">Virtual.</span></span>                                        |
| [<span data-ttu-id="cd74b-128">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="cd74b-128">**GetOwner**</span></span>](cunknown-getowner.md)                                       | <span data-ttu-id="cd74b-129">Obtiene un puntero al **IUnknown** de control.</span><span class="sxs-lookup"><span data-stu-id="cd74b-129">Gets a pointer to the controlling **IUnknown**.</span></span>                    |
| <span data-ttu-id="cd74b-130">Métodos INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="cd74b-130">INonDelegatingUnknown Methods</span></span>                                               | <span data-ttu-id="cd74b-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd74b-131">Description</span></span>                                                        |
| [<span data-ttu-id="cd74b-132">**NonDelegatingAddRef**</span><span class="sxs-lookup"><span data-stu-id="cd74b-132">**NonDelegatingAddRef**</span></span>](cunknown-nondelegatingaddref.md)                 | <span data-ttu-id="cd74b-133">Incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="cd74b-133">Increments the reference count.</span></span>                                    |
| [<span data-ttu-id="cd74b-134">**NonDelegatingQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="cd74b-134">**NonDelegatingQueryInterface**</span></span>](cunknown-nondelegatingqueryinterface.md) | <span data-ttu-id="cd74b-135">Recupera un puntero de interfaz e incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="cd74b-135">Retrieves an interface pointer and increments the reference count.</span></span> |
| [<span data-ttu-id="cd74b-136">**NonDelegatingRelease**</span><span class="sxs-lookup"><span data-stu-id="cd74b-136">**NonDelegatingRelease**</span></span>](cunknown-nondelegatingrelease.md)               | <span data-ttu-id="cd74b-137">Disminuye el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="cd74b-137">Decrements the reference count.</span></span>                                    |



 

## <a name="requirements"></a><span data-ttu-id="cd74b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd74b-138">Requirements</span></span>



| <span data-ttu-id="cd74b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd74b-139">Requirement</span></span> | <span data-ttu-id="cd74b-140">Value</span><span class="sxs-lookup"><span data-stu-id="cd74b-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd74b-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd74b-141">Header</span></span><br/>  | <dl> <span data-ttu-id="cd74b-142"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd74b-142"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cd74b-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd74b-143">Library</span></span><br/> | <dl> <span data-ttu-id="cd74b-144"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cd74b-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd74b-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd74b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd74b-146">Clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="cd74b-146">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




