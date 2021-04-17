---
description: En este tema se describe cómo implementar el registro de errores en los servicios de edición de DirectShow.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Crear una clase de registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db08971c7bf1a0024669935079b7a9403c429327
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659301"
---
# <a name="creating-an-error-logging-class"></a><span data-ttu-id="14793-103">Crear una clase de registro de errores</span><span class="sxs-lookup"><span data-stu-id="14793-103">Creating an Error Logging Class</span></span>

<span data-ttu-id="14793-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="14793-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="14793-105">En este tema se describe cómo implementar el registro de errores en los [servicios de edición de DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="14793-105">This topic describes how to implement error logging in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="14793-106">En primer lugar, declare una clase que implementará el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="14793-106">First, declare a class that will implement error logging.</span></span> <span data-ttu-id="14793-107">La clase hereda la interfaz [**IAMErrorLog**](iamerrorlog.md) .</span><span class="sxs-lookup"><span data-stu-id="14793-107">The class inherits the [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="14793-108">Contiene declaraciones para los tres métodos **IUnknown** y para el método único en [IAMErrorLog](implementing-iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="14793-108">It contains declarations for the three **IUnknown** methods, and for the single method in [IAMErrorLog](implementing-iamerrorlog.md).</span></span> <span data-ttu-id="14793-109">La declaración de clase es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="14793-109">The class declaration is as follows:</span></span>


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



<span data-ttu-id="14793-110">La única variable miembro de la clase es m \_ lRef, que contiene el recuento de referencias del objeto.</span><span class="sxs-lookup"><span data-stu-id="14793-110">The only member variable in the class is m\_lRef, which holds the object's reference count.</span></span>

<span data-ttu-id="14793-111">A continuación, defina los métodos en **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="14793-111">Next, define the methods in **IUnknown**.</span></span> <span data-ttu-id="14793-112">En el ejemplo siguiente se muestra una implementación estándar para estos métodos:</span><span class="sxs-lookup"><span data-stu-id="14793-112">The following example shows a standard implementation for these methods:</span></span>


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



<span data-ttu-id="14793-113">Con el marco COM en su lugar, ahora puede implementar la interfaz **IAMErrorLog** .</span><span class="sxs-lookup"><span data-stu-id="14793-113">With the COM framework in place, you can now implement the **IAMErrorLog** interface.</span></span> <span data-ttu-id="14793-114">En la sección siguiente se describe cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="14793-114">The next section describes how to do this.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14793-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14793-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14793-116">Errores de registro</span><span class="sxs-lookup"><span data-stu-id="14793-116">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



