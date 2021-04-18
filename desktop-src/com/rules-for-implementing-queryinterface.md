---
title: Reglas para implementar QueryInterface
description: Reglas para implementar QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705034"
---
# <a name="rules-for-implementing-queryinterface"></a><span data-ttu-id="537c9-103">Reglas para implementar QueryInterface</span><span class="sxs-lookup"><span data-stu-id="537c9-103">Rules for Implementing QueryInterface</span></span>

<span data-ttu-id="537c9-104">Hay tres reglas principales que rigen la implementación del método [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en un objeto com:</span><span class="sxs-lookup"><span data-stu-id="537c9-104">There are three main rules that govern implementing the [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) method on a COM object:</span></span>

-   <span data-ttu-id="537c9-105">Los objetos deben tener la identidad.</span><span class="sxs-lookup"><span data-stu-id="537c9-105">Objects must have identity.</span></span>
-   <span data-ttu-id="537c9-106">El conjunto de interfaces de una instancia de objeto debe ser estático.</span><span class="sxs-lookup"><span data-stu-id="537c9-106">The set of interfaces on an object instance must be static.</span></span>
-   <span data-ttu-id="537c9-107">Debe ser posible realizar consultas correctamente en cualquier interfaz de un objeto de cualquier otra interfaz.</span><span class="sxs-lookup"><span data-stu-id="537c9-107">It must be possible to query successfully for any interface on an object from any other interface.</span></span>

## <a name="objects-must-have-identity"></a><span data-ttu-id="537c9-108">Los objetos deben tener la identidad</span><span class="sxs-lookup"><span data-stu-id="537c9-108">Objects Must Have Identity</span></span>

<span data-ttu-id="537c9-109">En el caso de una instancia de objeto determinada, una llamada a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) con IID \_ IUnknown siempre debe devolver el mismo valor de puntero físico.</span><span class="sxs-lookup"><span data-stu-id="537c9-109">For any given object instance, a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) with IID\_IUnknown must always return the same physical pointer value.</span></span> <span data-ttu-id="537c9-110">Esto le permite llamar a **QueryInterface** en dos interfaces cualesquiera y comparar los resultados para determinar si señalan a la misma instancia de un objeto.</span><span class="sxs-lookup"><span data-stu-id="537c9-110">This allows you to call **QueryInterface** on any two interfaces and compare the results to determine whether they point to the same instance of an object.</span></span>

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a><span data-ttu-id="537c9-111">El conjunto de interfaces de una instancia de objeto debe ser estático</span><span class="sxs-lookup"><span data-stu-id="537c9-111">The Set of Interfaces on an Object Instance Must Be Static</span></span>

<span data-ttu-id="537c9-112">El conjunto de interfaces accesible en un objeto a través de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) debe ser estático, no dinámico.</span><span class="sxs-lookup"><span data-stu-id="537c9-112">The set of interfaces accessible on an object through [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) must be static, not dynamic.</span></span> <span data-ttu-id="537c9-113">En concreto, si **QueryInterface** devuelve \_ un valor correcto para un IID determinado una vez, nunca debe devolver e \_ nointerface en llamadas posteriores en el mismo objeto; y si **QueryInterface** devuelve e \_ nointerface para un IID determinado, las llamadas subsiguientes para el mismo IID en el mismo objeto nunca deben devolver S \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="537c9-113">Specifically, if **QueryInterface** returns S\_OK for a given IID once, it must never return E\_NOINTERFACE on subsequent calls on the same object; and if **QueryInterface** returns E\_NOINTERFACE for a given IID, subsequent calls for the same IID on the same object must never return S\_OK.</span></span>

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a><span data-ttu-id="537c9-114">Debe ser posible realizar consultas correctamente en cualquier interfaz de un objeto de cualquier otra interfaz.</span><span class="sxs-lookup"><span data-stu-id="537c9-114">It Must Be Possible to Query Successfully for Any Interface on an Object from Any Other Interface</span></span>

<span data-ttu-id="537c9-115">Es decir, según el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="537c9-115">That is, given the following code:</span></span>

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

<span data-ttu-id="537c9-116">se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="537c9-116">the following rules apply:</span></span>

-   <span data-ttu-id="537c9-117">Si tiene un puntero a una interfaz en un objeto, se debe realizar una llamada como la siguiente a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para esa misma interfaz:</span><span class="sxs-lookup"><span data-stu-id="537c9-117">If you have a pointer to an interface on an object, a call like the following to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for that same interface must succeed:</span></span>

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="537c9-118">Si una llamada a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para un segundo puntero de interfaz se realiza correctamente, también se debe realizar una llamada a **QueryInterface** desde ese puntero para la primera interfaz.</span><span class="sxs-lookup"><span data-stu-id="537c9-118">If a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for a second interface pointer succeeds, a call to **QueryInterface** from that pointer for the first interface must also succeed.</span></span> <span data-ttu-id="537c9-119">Si se ha obtenido pB correctamente, también se deben realizar las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="537c9-119">If pB was successfully obtained, the following must also succeed:</span></span>

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="537c9-120">Cualquier interfaz debe ser capaz de consultar cualquier otra interfaz en un objeto.</span><span class="sxs-lookup"><span data-stu-id="537c9-120">Any interface must be able to query for any other interface on an object.</span></span> <span data-ttu-id="537c9-121">Si se ha obtenido pB correctamente y se ha realizado correctamente una consulta para una tercera interfaz (IC) con ese puntero, también debe poder realizar consultas correctamente en el caso de las empresas con el primer puntero, pA.</span><span class="sxs-lookup"><span data-stu-id="537c9-121">If pB was successfully obtained and you successfully query for a third interface (IC) using that pointer, you must also be able to query successfully for IC using the first pointer, pA.</span></span> <span data-ttu-id="537c9-122">En este caso, la siguiente secuencia debe realizarse correctamente:</span><span class="sxs-lookup"><span data-stu-id="537c9-122">In this case, the following sequence must succeed:</span></span>

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

<span data-ttu-id="537c9-123">Las implementaciones de interfaz deben mantener un contador de referencias de puntero pendientes a todas las interfaces de un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="537c9-123">Interface implementations must maintain a counter of outstanding pointer references to all the interfaces on a given object.</span></span> <span data-ttu-id="537c9-124">Debe utilizar un **entero sin signo** para el contador.</span><span class="sxs-lookup"><span data-stu-id="537c9-124">You should use an **unsigned integer** for the counter.</span></span>

<span data-ttu-id="537c9-125">Si un cliente necesita saber que se han liberado recursos, debe usar un método en alguna interfaz en el objeto con una semántica de nivel superior antes de llamar a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="537c9-125">If a client needs to know that resources have been freed, it must use a method in some interface on the object with higher-level semantics before calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

## <a name="related-topics"></a><span data-ttu-id="537c9-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="537c9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="537c9-127">Usar e implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="537c9-127">Using and Implementing IUnknown</span></span>](using-and-implementing-iunknown.md)
</dt> </dl>

 

 