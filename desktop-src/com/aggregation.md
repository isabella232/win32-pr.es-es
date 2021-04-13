---
title: Agregación
description: La agregación es el mecanismo de reutilización de objetos en el que el objeto externo expone interfaces del objeto interno como si se hubieran implementado en el propio objeto externo.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4f11f69f5d7b14047a8138cba93bd503b645a3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359440"
---
# <a name="aggregation"></a><span data-ttu-id="fd656-103">Agregación</span><span class="sxs-lookup"><span data-stu-id="fd656-103">Aggregation</span></span>

<span data-ttu-id="fd656-104">La agregación es el mecanismo de reutilización de objetos en el que el objeto externo expone interfaces del objeto interno como si se hubieran implementado en el propio objeto externo.</span><span class="sxs-lookup"><span data-stu-id="fd656-104">Aggregation is the object reuse mechanism in which the outer object exposes interfaces from the inner object as if they were implemented on the outer object itself.</span></span> <span data-ttu-id="fd656-105">Esto resulta útil cuando el objeto externo delega cada llamada a una de sus interfaces a la misma interfaz en el objeto interno.</span><span class="sxs-lookup"><span data-stu-id="fd656-105">This is useful when the outer object delegates every call to one of its interfaces to the same interface in the inner object.</span></span> <span data-ttu-id="fd656-106">La agregación está disponible por comodidad para evitar la sobrecarga de implementación adicional en el objeto externo en este caso.</span><span class="sxs-lookup"><span data-stu-id="fd656-106">Aggregation is available as a convenience to avoid extra implementation overhead in the outer object in this case.</span></span> <span data-ttu-id="fd656-107">En realidad, la agregación es un caso especializado de [contención o delegación](containment-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="fd656-107">Aggregation is actually a specialized case of [containment/delegation](containment-delegation.md).</span></span>

<span data-ttu-id="fd656-108">La agregación es casi tan sencilla de implementar como contención es, excepto para las tres funciones [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) : [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="fd656-108">Aggregation is almost as simple to implement as containment is, except for the three [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) functions: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="fd656-109">La instrucción Catch es que, desde la perspectiva del cliente, cualquier función **IUnknown** en el objeto externo debe afectar al objeto externo.</span><span class="sxs-lookup"><span data-stu-id="fd656-109">The catch is that from the client's perspective, any **IUnknown** function on the outer object must affect the outer object.</span></span> <span data-ttu-id="fd656-110">Es decir, **AddRef** y **Release** afectan al objeto externo y **QueryInterface** expone todas las interfaces disponibles en el objeto externo.</span><span class="sxs-lookup"><span data-stu-id="fd656-110">That is, **AddRef** and **Release** affect the outer object and **QueryInterface** exposes all the interfaces available on the outer object.</span></span> <span data-ttu-id="fd656-111">Sin embargo, si el objeto externo simplemente expone la interfaz de un objeto interno por su cuenta, los miembros **IUnknown** del objeto interno a los que se llama a través de esa interfaz se comportarán de forma diferente a los miembros **IUnknown** de las interfaces del objeto externo, una infracción absoluta de las reglas y propiedades que rigen **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="fd656-111">However, if the outer object simply exposes an inner object's interface as its own, that inner object's **IUnknown** members called through that interface will behave differently than those **IUnknown** members on the outer object's interfaces, an absolute violation of the rules and properties governing **IUnknown**.</span></span>

<span data-ttu-id="fd656-112">La solución es que la agregación requiere una implementación explícita de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) en el objeto interno y la delegación de los métodos **IUnknown** de cualquier otra interfaz a los métodos **IUnknown** del objeto externo.</span><span class="sxs-lookup"><span data-stu-id="fd656-112">The solution is that aggregation requires an explicit implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) on the inner object and delegation of the **IUnknown** methods of any other interface to the outer object's **IUnknown** methods.</span></span>

## <a name="creating-aggregable-objects"></a><span data-ttu-id="fd656-113">Crear objetos Aggregable</span><span class="sxs-lookup"><span data-stu-id="fd656-113">Creating Aggregable Objects</span></span>

<span data-ttu-id="fd656-114">La creación de objetos que se pueden agregar es opcional; sin embargo, es fácil de hacer y proporciona importantes ventajas.</span><span class="sxs-lookup"><span data-stu-id="fd656-114">Creating objects that can be aggregated is optional; however, it is simple to do and provides significant benefits.</span></span> <span data-ttu-id="fd656-115">Las siguientes reglas se aplican a la creación de un objeto aggregable:</span><span class="sxs-lookup"><span data-stu-id="fd656-115">The following rules apply to creating an aggregable object:</span></span>

-   <span data-ttu-id="fd656-116">La implementación del objeto aggregable (o interno) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para su interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) controla el recuento de referencias del objeto interno, y esta implementación no debe delegar en el desconocido del objeto externo (control **IUnknown**).</span><span class="sxs-lookup"><span data-stu-id="fd656-116">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface controls the inner object's reference count, and this implementation must not delegate to the outer object's unknown (the controlling **IUnknown**).</span></span>
-   <span data-ttu-id="fd656-117">La implementación del objeto aggregable (o interno) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para sus otras interfaces debe delegar al [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control y no debe afectar directamente al recuento de referencias del objeto interno.</span><span class="sxs-lookup"><span data-stu-id="fd656-117">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its other interfaces must delegate to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and must not directly affect the inner object's reference count.</span></span>
-   <span data-ttu-id="fd656-118">[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interno debe implementar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) solo para el objeto interno.</span><span class="sxs-lookup"><span data-stu-id="fd656-118">The inner [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) must implement [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) only for the inner object.</span></span>
-   <span data-ttu-id="fd656-119">El objeto aggregable no debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) cuando contiene una referencia al puntero de control [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fd656-119">The aggregable object must not call [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) when holding a reference to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="fd656-120">Cuando se crea el objeto, si se solicita una interfaz que no sea [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , se debe producir un error en la creación con E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="fd656-120">When the object is created, if any interface other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) is requested, the creation must fail with E\_NOINTERFACE.</span></span>

<span data-ttu-id="fd656-121">En el fragmento de código siguiente se muestra una implementación correcta de un objeto aggregable mediante el método de clase anidada de implementación de interfaces:</span><span class="sxs-lookup"><span data-stu-id="fd656-121">The following code fragment illustrates a correct implementation of an aggregable object by using the nested class method of implementing interfaces:</span></span>


```C++
// CSomeObject is an aggregable object that implements 
// IUnknown and ISomeInterface 
class CSomeObject : public IUnknown 
{ 
    private: 
        DWORD        m_cRef;         // Object reference count 
        IUnknown*    m_pUnkOuter;    // Controlling IUnknown, no AddRef 
 
        // Nested class to implement the ISomeInterface interface 
        class CImpSomeInterface : public ISomeInterface 
        { 
            friend class CSomeObject ; 
            private: 
                DWORD    m_cRef;    // Interface ref-count, for debugging 
                IUnknown*    m_pUnkOuter;    // Controlling IUnknown 
            public: 
                CImpSomeInterface() { m_cRef = 0;   }; 
                ~ CImpSomeInterface(void) {}; 
 
                // IUnknown members delegate to the outer unknown 
                // IUnknown members do not control lifetime of object 
                STDMETHODIMP     QueryInterface(REFIID riid, void** ppv) 
                {    return m_pUnkOuter->QueryInterface(riid,ppv);   }; 
 
                STDMETHODIMP_(DWORD) AddRef(void) 
                {    return m_pUnkOuter->AddRef();   }; 
 
                STDMETHODIMP_(DWORD) Release(void) 
                {    return m_pUnkOuter->Release();   }; 
 
                // ISomeInterface members 
                STDMETHODIMP SomeMethod(void) 
                {    return S_OK;   }; 
        } ; 
        CImpSomeInterface m_ImpSomeInterface ; 
    public: 
        CSomeObject(IUnknown * pUnkOuter) 
        { 
            m_cRef=0; 
            // No AddRef necessary if non-NULL as we're aggregated. 
            m_pUnkOuter=pUnkOuter; 
            m_ImpSomeInterface.m_pUnkOuter=pUnkOuter; 
        } ; 
        ~CSomeObject(void) {} ; 
 
        // Static member function for creating new instances (don't use 
        // new directly). Protects against outer objects asking for 
        // interfaces other than Iunknown. 
        static HRESULT Create(IUnknown* pUnkOuter, REFIID riid, void **ppv) 
        { 
            CSomeObject*        pObj; 
            if (pUnkOuter != NULL && riid != IID_IUnknown) 
                return CLASS_E_NOAGGREGATION; 
            pObj = new CSomeObject(pUnkOuter); 
            if (pObj == NULL) 
                return E_OUTOFMEMORY; 
            // Set up the right unknown for delegation (the non-
            // aggregation case) 
            if (pUnkOuter == NULL) 
            {
                pObj->m_pUnkOuter = (IUnknown*)pObj ; 
                pObj->m_ImpSomeInterface.m_pUnkOuter = (IUnknown*)pObj;
            }
            HRESULT hr; 
            if (FAILED(hr = pObj->QueryInterface(riid, (void**)ppv))) 
                delete pObj ; 
            return hr; 
        } 
 
        // Inner IUnknown members, non-delegating 
        // Inner QueryInterface only controls inner object 
        STDMETHODIMP QueryInterface(REFIID riid, void** ppv) 
        { 
            *ppv=NULL; 
            if (riid == IID_IUnknown) 
                *ppv=this; 
            if (riid == IID_ISomeInterface) 
                *ppv=&m_ImpSomeInterface; 
            if (NULL==*ppv) 
                return ResultFromScode(E_NOINTERFACE); 
            ((IUnknown*)*ppv)->AddRef(); 
            return NOERROR; 
        } ; 
        STDMETHODIMP_(DWORD) AddRef(void) 
        {    return ++m_cRef; }; 
        STDMETHODIMP_(DWORD) Release(void) 
        { 
            if (--m_cRef != 0) 
                return m_cRef; 
            delete this; 
            return 0; 
        }; 
}; 
 
```



## <a name="aggregating-objects"></a><span data-ttu-id="fd656-122">Agregar objetos</span><span class="sxs-lookup"><span data-stu-id="fd656-122">Aggregating Objects</span></span>

<span data-ttu-id="fd656-123">Al desarrollar un objeto aggregable, se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="fd656-123">When developing an aggregable object, the following rules apply:</span></span>

-   <span data-ttu-id="fd656-124">Al crear el objeto interno, el objeto externo debe solicitar explícitamente su [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="fd656-124">When creating the inner object, the outer object must explicitly ask for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="fd656-125">El objeto externo debe proteger su implementación de [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) de la reentrada con un recuento de referencias artificial en torno a su código de destrucción.</span><span class="sxs-lookup"><span data-stu-id="fd656-125">The outer object must protect its implementation of [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) from reentrancy with an artificial reference count around its destruction code.</span></span>
-   <span data-ttu-id="fd656-126">El objeto externo debe llamar al método de  [**liberación**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) de control **IUnknown** si consulta un puntero a cualquiera de las interfaces del objeto interno.</span><span class="sxs-lookup"><span data-stu-id="fd656-126">The outer object must call its controlling **IUnknown** [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method if it queries for a pointer to any of the inner object's interfaces.</span></span> <span data-ttu-id="fd656-127">Para liberar este puntero, el objeto externo llama al método de control **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) , seguido de **Release** en el puntero del objeto interno.</span><span class="sxs-lookup"><span data-stu-id="fd656-127">To free this pointer, the outer object calls its controlling **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method, followed by **Release** on the inner object's pointer.</span></span>
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   <span data-ttu-id="fd656-128">El objeto externo no debe delegar ciegamente una consulta para ninguna interfaz no reconocida en el objeto interno, a menos que ese comportamiento sea específicamente el objetivo del objeto externo.</span><span class="sxs-lookup"><span data-stu-id="fd656-128">The outer object must not blindly delegate a query for any unrecognized interface to the inner object, unless that behavior is specifically the intention of the outer object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd656-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd656-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd656-130">Contención/delegación</span><span class="sxs-lookup"><span data-stu-id="fd656-130">Containment/Delegation</span></span>](containment-delegation.md)
</dt> </dl>

 

 