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
# <a name="supporting-multiple-callbacks"></a>Admitir varias devoluciones de llamada

Si llama a más de un método asincrónico, cada uno de ellos requiere una implementación independiente de [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Sin embargo, es posible que desee implementar las devoluciones de llamada en una sola clase de C++. La clase solo puede tener un método de **invocación** , por lo que una solución consiste en proporcionar una clase auxiliar que delegue las llamadas de **invocación** a otro método en una clase contenedora.

En el código siguiente se muestra una plantilla de clase denominada `AsyncCallback` , que muestra este enfoque.


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



El parámetro de plantilla es el nombre de la clase contenedora. El `AsyncCallback` constructor tiene dos parámetros: un puntero a la clase de contenedor y la dirección de un método de devolución de llamada en la clase contenedora. La clase contenedora puede tener varias instancias de la `AsyncCallback` clase como variables miembro, una para cada método asincrónico. Cuando la clase de contenedor llama a un método asincrónico, se usa la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del `AsyncCallback` objeto adecuado. Cuando `AsyncCallback` se llama al método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) del objeto, la llamada se delega al método correcto en la clase contenedora.

El `AsyncCallback` objeto también delega las llamadas **AddRef** y **Release** a la clase de contenedor, por lo que la clase contenedora administra la duración del `AsyncCallback` objeto. Esto garantiza que el `AsyncCallback` objeto no se eliminará hasta que se elimine el propio objeto contenedor.

En el código siguiente se muestra cómo usar esta plantilla:


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



En este ejemplo, la clase de contenedor se denomina `CMyObject` . La variable miembro *m \_ CB* es un `AsyncCallback` objeto. En el `CMyObject` constructor, la variable miembro *m \_ CB* se inicializa con la dirección del `CMyObject::OnInvoke` método.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Métodos de devolución de llamada asincrónica](asynchronous-callback-methods.md)
</dt> </dl>

 

 



