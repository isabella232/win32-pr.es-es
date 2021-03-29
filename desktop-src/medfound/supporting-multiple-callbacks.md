---
description: Admitir varias devoluciones de llamada
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: Admitir varias devoluciones de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77a15899488e44ea3c1499b11af65894d47483c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812596"
---
# <a name="supporting-multiple-callbacks"></a><span data-ttu-id="43020-103">Admitir varias devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="43020-103">Supporting Multiple Callbacks</span></span>

<span data-ttu-id="43020-104">Si llama a más de un método asincrónico, cada uno de ellos requiere una implementación independiente de [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="43020-104">If you call more than one asynchronous method, each one requires a separate implementation of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="43020-105">Sin embargo, es posible que desee implementar las devoluciones de llamada en una sola clase de C++.</span><span class="sxs-lookup"><span data-stu-id="43020-105">However, you might want to implement the callbacks inside a single C++ class.</span></span> <span data-ttu-id="43020-106">La clase solo puede tener un método de **invocación** , por lo que una solución consiste en proporcionar una clase auxiliar que delegue las llamadas de **invocación** a otro método en una clase contenedora.</span><span class="sxs-lookup"><span data-stu-id="43020-106">The class can have only one **Invoke** method, so one solution is to provide a helper class that delegates **Invoke** calls to another method on a container class.</span></span>

<span data-ttu-id="43020-107">En el código siguiente se muestra una plantilla de clase denominada `AsyncCallback` , que muestra este enfoque.</span><span class="sxs-lookup"><span data-stu-id="43020-107">The following code shows a class template named `AsyncCallback`, which demonstrates this approach.</span></span>


```C++
//////////////////////////////////////////////////////////////////////////
//  AsyncCallback [template]
//
//  Description:
//  Helper class that routes IMFAsyncCallback::Invoke calls to a class
//  method on the parent class.
//
//  Usage:
//  Add this class as a member variable. In the parent class constructor,
//  initialize the AsyncCallback class like this:
//      m_cb(this, &CYourClass::OnInvoke)
//  where
//      m_cb       = AsyncCallback object
//      CYourClass = parent class
//      OnInvoke   = Method in the parent class to receive Invoke calls.
//
//  The parent's OnInvoke method (you can name it anything you like) must
//  have a signature that matches the InvokeFn typedef below.
//////////////////////////////////////////////////////////////////////////

// T: Type of the parent object
template<class T>
class AsyncCallback : public IMFAsyncCallback
{
public:
    typedef HRESULT (T::*InvokeFn)(IMFAsyncResult *pAsyncResult);

    AsyncCallback(T *pParent, InvokeFn fn) : m_pParent(pParent), m_pInvokeFn(fn)
    {
    }

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(AsyncCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef() {
        // Delegate to parent class.
        return m_pParent->AddRef();
    }
    STDMETHODIMP_(ULONG) Release() {
        // Delegate to parent class.
        return m_pParent->Release();
    }

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult)
    {
        return (m_pParent->*m_pInvokeFn)(pAsyncResult);
    }

    T *m_pParent;
    InvokeFn m_pInvokeFn;
};
```



<span data-ttu-id="43020-108">El parámetro de plantilla es el nombre de la clase contenedora.</span><span class="sxs-lookup"><span data-stu-id="43020-108">The template parameter is the name of container class.</span></span> <span data-ttu-id="43020-109">El `AsyncCallback` constructor tiene dos parámetros: un puntero a la clase de contenedor y la dirección de un método de devolución de llamada en la clase contenedora.</span><span class="sxs-lookup"><span data-stu-id="43020-109">The `AsyncCallback` constructor has two parameters: a pointer to the container class, and the address of a callback method on the container class.</span></span> <span data-ttu-id="43020-110">La clase contenedora puede tener varias instancias de la `AsyncCallback` clase como variables miembro, una para cada método asincrónico.</span><span class="sxs-lookup"><span data-stu-id="43020-110">The container class can have multiple instances of the `AsyncCallback` class as member variables, one for each asynchronous method.</span></span> <span data-ttu-id="43020-111">Cuando la clase de contenedor llama a un método asincrónico, se usa la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del `AsyncCallback` objeto adecuado.</span><span class="sxs-lookup"><span data-stu-id="43020-111">When the container class calls an asynchronous method, it use the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface of the appropriate `AsyncCallback` object.</span></span> <span data-ttu-id="43020-112">Cuando `AsyncCallback` se llama al método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) del objeto, la llamada se delega al método correcto en la clase contenedora.</span><span class="sxs-lookup"><span data-stu-id="43020-112">When the `AsyncCallback` object's [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called, the call is delegated to the correct method on the container class.</span></span>

<span data-ttu-id="43020-113">El `AsyncCallback` objeto también delega las llamadas **AddRef** y **Release** a la clase de contenedor, por lo que la clase contenedora administra la duración del `AsyncCallback` objeto.</span><span class="sxs-lookup"><span data-stu-id="43020-113">The `AsyncCallback` object also delegates **AddRef** and **Release** calls to the container class, so the container class manages the lifetime of the `AsyncCallback` object.</span></span> <span data-ttu-id="43020-114">Esto garantiza que el `AsyncCallback` objeto no se eliminará hasta que se elimine el propio objeto contenedor.</span><span class="sxs-lookup"><span data-stu-id="43020-114">This guarantees that the `AsyncCallback` object will not be deleted until the container object itself is deleted.</span></span>

<span data-ttu-id="43020-115">En el código siguiente se muestra cómo usar esta plantilla:</span><span class="sxs-lookup"><span data-stu-id="43020-115">The following code shows how to use this template:</span></span>


```C++
#pragma warning( push )
#pragma warning( disable : 4355 )  // 'this' used in base member initializer list

class CMyObject : public IUnknown
{
public:

    CMyObject() : m_CB(this, &CMyObject::OnInvoke)
    {
        // Other initialization here.
    }

    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);


private:

    AsyncCallback<CMyObject>   m_CB;

    HRESULT OnInvoke(IMFAsyncResult *pAsyncResult);
};

#pragma warning( pop )
```



<span data-ttu-id="43020-116">En este ejemplo, la clase de contenedor se denomina `CMyObject` .</span><span class="sxs-lookup"><span data-stu-id="43020-116">In this example, the container class is named `CMyObject`.</span></span> <span data-ttu-id="43020-117">La variable miembro *m \_ CB* es un `AsyncCallback` objeto.</span><span class="sxs-lookup"><span data-stu-id="43020-117">The *m\_CB* member variable is a `AsyncCallback` object.</span></span> <span data-ttu-id="43020-118">En el `CMyObject` constructor, la variable miembro *m \_ CB* se inicializa con la dirección del `CMyObject::OnInvoke` método.</span><span class="sxs-lookup"><span data-stu-id="43020-118">In the `CMyObject` constructor, the *m\_CB* member variable is initialized with the address of the `CMyObject::OnInvoke` method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43020-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43020-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43020-120">Métodos de devolución de llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="43020-120">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



