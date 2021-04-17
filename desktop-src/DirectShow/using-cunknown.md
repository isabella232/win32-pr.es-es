---
description: DirectShow implementa IUnknown en una clase base denominada CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Usar CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667859"
---
# <a name="using-cunknown"></a><span data-ttu-id="7c481-103">Usar CUnknown</span><span class="sxs-lookup"><span data-stu-id="7c481-103">Using CUnknown</span></span>

<span data-ttu-id="7c481-104">DirectShow implementa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en una clase base denominada [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7c481-104">DirectShow implements [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in a base class called [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="7c481-105">Puede usar **CUnknown** para derivar otras clases, invalidando solo los métodos que cambian en los componentes.</span><span class="sxs-lookup"><span data-stu-id="7c481-105">You can use **CUnknown** to derive other classes, overriding only the methods that change across components.</span></span> <span data-ttu-id="7c481-106">La mayoría de las otras clases base de DirectShow se derivan de **CUnknown**, por lo que el componente puede heredar directamente de **CUnknown** o de otra clase base.</span><span class="sxs-lookup"><span data-stu-id="7c481-106">Most of the other base classes in DirectShow derive from **CUnknown**, so your component can inherit directly from **CUnknown** or from another base class.</span></span>

## <a name="inondelegatingunknown"></a><span data-ttu-id="7c481-107">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="7c481-107">INonDelegatingUnknown</span></span>

<span data-ttu-id="7c481-108">[**CUnknown**](cunknown.md) implementa [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7c481-108">[**CUnknown**](cunknown.md) implements [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="7c481-109">Administra los recuentos de referencias internamente y, en la mayoría de los casos, la clase derivada puede heredar los dos métodos de recuento de referencias sin ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="7c481-109">It manages reference counts internally, and in most situations your derived class can inherit the two reference-counting methods with no change.</span></span> <span data-ttu-id="7c481-110">Tenga en cuenta que **CUnknown** se elimina a sí mismo cuando el recuento de referencias desciende a cero.</span><span class="sxs-lookup"><span data-stu-id="7c481-110">Be aware that **CUnknown** deletes itself when the reference count drops to zero.</span></span> <span data-ttu-id="7c481-111">Por otro lado, debe invalidar [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), porque el método de la clase base devuelve E \_ nointerface si recibe un IID distinto de IID \_ IUnknown.</span><span class="sxs-lookup"><span data-stu-id="7c481-111">On the other hand, you must override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), because the method in the base class returns E\_NOINTERFACE if it receives any IID other than IID\_IUnknown.</span></span> <span data-ttu-id="7c481-112">En la clase derivada, compruebe los IID de las interfaces que admite, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7c481-112">In your derived class, test for the IIDs of interfaces that you support, as shown in the following example:</span></span>


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="7c481-113">La función de utilidad [**GetInterface**](getinterface.md) (vea [**funciones auxiliares de com**](com-helper-functions.md)) establece el puntero, incrementa el recuento de referencias de una manera segura para subprocesos y devuelve S \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="7c481-113">The utility function [**GetInterface**](getinterface.md) (see [**COM Helper Functions**](com-helper-functions.md)) sets the pointer, increments the reference count in a thread-safe way, and returns S\_OK.</span></span> <span data-ttu-id="7c481-114">En el caso predeterminado, llame al método de la clase base y devuelva el resultado.</span><span class="sxs-lookup"><span data-stu-id="7c481-114">In the default case, call the base class method and return the result.</span></span> <span data-ttu-id="7c481-115">Si deriva de otra clase base, llame a su método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7c481-115">If you derive from another base class, call its [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method instead.</span></span> <span data-ttu-id="7c481-116">Esto le permite admitir todas las interfaces que admite la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="7c481-116">This enables you to support all the interfaces that the parent class supports.</span></span>

## <a name="iunknown"></a><span data-ttu-id="7c481-117">IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c481-117">IUnknown</span></span>

<span data-ttu-id="7c481-118">Como se mencionó anteriormente, la versión de delegación de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) es la misma para todos los componentes, ya que no hace nada más que invocar la instancia correcta de la versión sin delegación.</span><span class="sxs-lookup"><span data-stu-id="7c481-118">As mentioned earlier, the delegating version of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is the same for every component, because it does nothing more than invoke the correct instance of the nondelegating version.</span></span> <span data-ttu-id="7c481-119">Para mayor comodidad, el archivo de encabezado ComBase. h contiene una macro, [**declare \_ IUNKNOWN**](declare-iunknown.md), que declara los tres métodos de delegación como métodos insertados.</span><span class="sxs-lookup"><span data-stu-id="7c481-119">For convenience, the header file Combase.h contains a macro, [**DECLARE\_IUNKNOWN**](declare-iunknown.md), which declares the three delegating methods as inline methods.</span></span> <span data-ttu-id="7c481-120">Se expande al siguiente código:</span><span class="sxs-lookup"><span data-stu-id="7c481-120">It expands to the following code:</span></span>


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



<span data-ttu-id="7c481-121">La función de utilidad [**CUnknown:: GetOwner**](cunknown-getowner.md) recupera un puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del componente que posee este componente.</span><span class="sxs-lookup"><span data-stu-id="7c481-121">The utility function [**CUnknown::GetOwner**](cunknown-getowner.md) retrieves a pointer to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the component that owns this component.</span></span> <span data-ttu-id="7c481-122">Para un componente agregado, el propietario es el componente externo.</span><span class="sxs-lookup"><span data-stu-id="7c481-122">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="7c481-123">De lo contrario, el componente es el propietario.</span><span class="sxs-lookup"><span data-stu-id="7c481-123">Otherwise, the component owns itself.</span></span> <span data-ttu-id="7c481-124">Incluya la macro declare \_ IUNKNOWN en la sección Public de la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="7c481-124">Include the DECLARE\_IUNKNOWN macro in the public section of your class definition.</span></span>

## <a name="class-constructor"></a><span data-ttu-id="7c481-125">Constructor de clase</span><span class="sxs-lookup"><span data-stu-id="7c481-125">Class Constructor</span></span>

<span data-ttu-id="7c481-126">El constructor de clase debe invocar el método de constructor de la clase primaria, además de cualquier cosa que sea específica de la clase.</span><span class="sxs-lookup"><span data-stu-id="7c481-126">Your class constructor should invoke the constructor method for the parent class, in addition to anything it does that is specific to your class.</span></span> <span data-ttu-id="7c481-127">El ejemplo siguiente es un método de constructor típico:</span><span class="sxs-lookup"><span data-stu-id="7c481-127">The following example is a typical constructor method:</span></span>


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



<span data-ttu-id="7c481-128">El método toma los parámetros siguientes, que pasa directamente al método de constructor [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="7c481-128">The method takes the following parameters, which it passes directly to the [**CUnknown**](cunknown.md) constructor method.</span></span>

-   <span data-ttu-id="7c481-129">*tszName* especifica un nombre para el componente.</span><span class="sxs-lookup"><span data-stu-id="7c481-129">*tszName* specifies a name for the component.</span></span>
-   <span data-ttu-id="7c481-130">*pUnk* es un puntero a la [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)de agregación.</span><span class="sxs-lookup"><span data-stu-id="7c481-130">*pUnk* is a pointer to the aggregating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="7c481-131">*pHr* es un puntero a un valor HRESULT que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="7c481-131">*pHr* is a pointer to an HRESULT value, indicating the success or failure of the method.</span></span>

## <a name="summary"></a><span data-ttu-id="7c481-132">Resumen</span><span class="sxs-lookup"><span data-stu-id="7c481-132">Summary</span></span>

<span data-ttu-id="7c481-133">En el ejemplo siguiente se muestra una clase derivada que admite [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y una interfaz hipotética denominada ISomeInterface:</span><span class="sxs-lookup"><span data-stu-id="7c481-133">The following example shows a derived class that supports [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and a hypothetical interface named ISomeInterface:</span></span>


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



<span data-ttu-id="7c481-134">En este ejemplo se muestran los puntos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7c481-134">This example illustrates the following points:</span></span>

-   <span data-ttu-id="7c481-135">La clase [**CUnknown**](cunknown.md) implementa la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7c481-135">The [**CUnknown**](cunknown.md) class implements the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7c481-136">El nuevo componente hereda de **CUnknown** y de cualquier interfaz que el componente admita.</span><span class="sxs-lookup"><span data-stu-id="7c481-136">The new component inherits from **CUnknown** and from any interfaces that the component supports.</span></span> <span data-ttu-id="7c481-137">El componente podría derivar en su lugar de otra clase base que hereda de **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="7c481-137">The component could derive instead from another base class that inherits from **CUnknown**.</span></span>
-   <span data-ttu-id="7c481-138">La macro [**declare \_ IUnknown**](declare-iunknown.md) declara los métodos de delegación de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) como métodos insertados.</span><span class="sxs-lookup"><span data-stu-id="7c481-138">The [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro declares the delegating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) methods as inline methods.</span></span>
-   <span data-ttu-id="7c481-139">La clase [**CUnknown**](cunknown.md) proporciona la implementación de [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7c481-139">The [**CUnknown**](cunknown.md) class provides the implementation for [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>
-   <span data-ttu-id="7c481-140">Para admitir una interfaz que no sea [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), la clase derivada debe reemplazar el método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) y probar el IID de la nueva interfaz.</span><span class="sxs-lookup"><span data-stu-id="7c481-140">To support an interface other than [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), the derived class must override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method and test for the IID of the new interface.</span></span>
-   <span data-ttu-id="7c481-141">El constructor de clase invoca el método de constructor para [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7c481-141">The class constructor invokes the constructor method for [**CUnknown**](cunknown.md).</span></span>

<span data-ttu-id="7c481-142">El paso siguiente para escribir un filtro consiste en permitir que una aplicación cree nuevas instancias del componente.</span><span class="sxs-lookup"><span data-stu-id="7c481-142">The next step in writing a filter is to enable an application to create new instances of the component.</span></span> <span data-ttu-id="7c481-143">Esto requiere un conocimiento de los archivos dll y su relación con los generadores de clases y los métodos de constructor de clase.</span><span class="sxs-lookup"><span data-stu-id="7c481-143">This requires an understanding of DLLs and their relation to class factories and class constructor methods.</span></span> <span data-ttu-id="7c481-144">Para obtener más información, vea [Cómo crear un archivo dll de filtro de DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="7c481-144">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c481-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c481-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c481-146">Cómo implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c481-146">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 
