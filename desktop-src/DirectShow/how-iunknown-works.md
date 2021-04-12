---
description: Cómo funciona IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Cómo funciona IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151981"
---
# <a name="how-iunknown-works"></a><span data-ttu-id="c9147-103">Cómo funciona IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9147-103">How IUnknown Works</span></span>

<span data-ttu-id="c9147-104">Los métodos de **IUnknown** permiten que una aplicación consulte las interfaces del componente y administre el recuento de referencias del componente.</span><span class="sxs-lookup"><span data-stu-id="c9147-104">The methods in **IUnknown** enable an application to query for interfaces on the component and manage the component's reference count.</span></span>

<span data-ttu-id="c9147-105">**Recuento de referencias**</span><span class="sxs-lookup"><span data-stu-id="c9147-105">**Reference Count**</span></span>

<span data-ttu-id="c9147-106">El recuento de referencias es una variable interna, incrementada en el método **AddRef** y disminuida en el método **Release** .</span><span class="sxs-lookup"><span data-stu-id="c9147-106">The reference count is an internal variable, incremented in the **AddRef** method and decremented in the **Release** method.</span></span> <span data-ttu-id="c9147-107">Las clases base administran el recuento de referencias y sincronizan el acceso al recuento de referencias entre varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c9147-107">The base classes manage the reference count and synchronize access to the reference count among multiple threads.</span></span>

<span data-ttu-id="c9147-108">**Consultas de interfaz**</span><span class="sxs-lookup"><span data-stu-id="c9147-108">**Interface Queries**</span></span>

<span data-ttu-id="c9147-109">La consulta de una interfaz también es sencilla.</span><span class="sxs-lookup"><span data-stu-id="c9147-109">Querying for an interface is also straightforward.</span></span> <span data-ttu-id="c9147-110">El autor de la llamada pasa dos parámetros: un identificador de interfaz (IID) y la dirección de un puntero.</span><span class="sxs-lookup"><span data-stu-id="c9147-110">The caller passes two parameters: an interface identifier (IID), and the address of a pointer.</span></span> <span data-ttu-id="c9147-111">Si el componente admite la interfaz solicitada, establece el puntero en la interfaz, incrementa su propio recuento de referencias y devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c9147-111">If the component supports the requested interface, it sets the pointer to the interface, increments its own reference count, and returns S\_OK.</span></span> <span data-ttu-id="c9147-112">De lo contrario, establece el puntero en **null** y devuelve e \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="c9147-112">Otherwise, it sets the pointer to **NULL** and returns E\_NOINTERFACE.</span></span> <span data-ttu-id="c9147-113">En el siguiente pseudocódigo se muestra el esquema general del método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="c9147-113">The following pseudocode shows the general outline of the **QueryInterface** method.</span></span> <span data-ttu-id="c9147-114">La agregación de componentes, que se describe en la sección siguiente, presenta cierta complejidad adicional.</span><span class="sxs-lookup"><span data-stu-id="c9147-114">Component aggregation, described in the next section, introduces some additional complexity.</span></span>


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



<span data-ttu-id="c9147-115">La única diferencia entre el método **QueryInterface** de un componente y el método **QueryInterface** de otro es la lista de IID que prueba cada componente.</span><span class="sxs-lookup"><span data-stu-id="c9147-115">The only difference between the **QueryInterface** method of one component and the **QueryInterface** method of another is the list of IIDs that each component tests.</span></span> <span data-ttu-id="c9147-116">Para cada interfaz que admite el componente, el componente debe probar el IID de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="c9147-116">For every interface that the component supports, the component must test for the IID of that interface.</span></span>

<span data-ttu-id="c9147-117">**Agregación y delegación**</span><span class="sxs-lookup"><span data-stu-id="c9147-117">**Aggregation and Delegation**</span></span>

<span data-ttu-id="c9147-118">La agregación de componentes debe ser transparente para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c9147-118">Component aggregation must be transparent to the caller.</span></span> <span data-ttu-id="c9147-119">Por lo tanto, el agregado debe exponer una única interfaz **IUnknown** , con el componente agregado que aplaza la implementación del componente externo.</span><span class="sxs-lookup"><span data-stu-id="c9147-119">Therefore, the aggregate must expose a single **IUnknown** interface, with the aggregated component deferring to the outer component's implementation.</span></span> <span data-ttu-id="c9147-120">De lo contrario, el autor de la llamada verá dos interfaces **IUnknown** diferentes en el mismo agregado.</span><span class="sxs-lookup"><span data-stu-id="c9147-120">Otherwise, the caller would see two different **IUnknown** interfaces in the same aggregate.</span></span> <span data-ttu-id="c9147-121">Si no se agrega el componente, utiliza su propia implementación.</span><span class="sxs-lookup"><span data-stu-id="c9147-121">If the component is not aggregated, it uses its own implementation.</span></span>

<span data-ttu-id="c9147-122">Para admitir este comportamiento, el componente debe agregar un nivel de direccionamiento indirecto.</span><span class="sxs-lookup"><span data-stu-id="c9147-122">To support this behavior, the component must add a level of indirection.</span></span> <span data-ttu-id="c9147-123">La *delegación de IUnknown* delega el trabajo en el lugar adecuado: para el componente externo, si hay alguno, o para la versión interna del componente.</span><span class="sxs-lookup"><span data-stu-id="c9147-123">A *delegating IUnknown* delegates the work to the appropriate place: to the outer component, if there is one, or to the component's internal version.</span></span> <span data-ttu-id="c9147-124">Un *IUnknown sin delegación* realiza el trabajo, tal como se describe en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="c9147-124">A *nondelegating IUnknown* does the work, as described in the previous section.</span></span>

<span data-ttu-id="c9147-125">La versión de delegación es pública y mantiene el nombre **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="c9147-125">The delegating version is public and keeps the name **IUnknown**.</span></span> <span data-ttu-id="c9147-126">Se cambia el nombre de la versión no delegada [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c9147-126">The nondelegating version is renamed [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="c9147-127">Este nombre no forma parte de la especificación COM, porque no es una interfaz pública.</span><span class="sxs-lookup"><span data-stu-id="c9147-127">This name is not part of the COM specification, because it is not a public interface.</span></span>

<span data-ttu-id="c9147-128">Cuando el cliente crea una instancia del componente, llama al método **IClassFactory:: CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="c9147-128">When the client creates an instance of the component, it calls the **IClassFactory::CreateInstance** method.</span></span> <span data-ttu-id="c9147-129">Un parámetro es un puntero a la interfaz **IUnknown** del componente de agregado, o **null** si no se agrega la nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="c9147-129">One parameter is a pointer to the aggregating component's **IUnknown** interface, or **NULL** if the new instance is not aggregated.</span></span> <span data-ttu-id="c9147-130">El componente utiliza este parámetro para almacenar una variable miembro que indica qué interfaz **IUnknown** se va a usar, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c9147-130">The component uses this parameter to store a member variable indicating which **IUnknown** interface to use, as shown in the following example:</span></span>


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



<span data-ttu-id="c9147-131">Cada método en el **IUnknown** de delegación llama a su homólogo no delegado, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c9147-131">Each method in the delegating **IUnknown** calls its nondelegating counterpart, as shown in the following example:</span></span>


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



<span data-ttu-id="c9147-132">Según la naturaleza de la delegación, los métodos de delegación son idénticos en todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="c9147-132">By the nature of delegation, the delegating methods look identical in every component.</span></span> <span data-ttu-id="c9147-133">Solo cambian las versiones sin delegación.</span><span class="sxs-lookup"><span data-stu-id="c9147-133">Only the nondelegating versions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9147-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9147-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9147-135">Cómo implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9147-135">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



