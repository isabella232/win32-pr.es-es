---
description: Objetos de resultado asincrónico personalizados
ms.assetid: 78cef367-b007-46d5-bb7f-2b3f7eed9926
title: Objetos de resultado asincrónico personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7212152de737a0af8e290b2c837b40cd4ad68840a49df79db148b4691068678b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742931"
---
# <a name="custom-asynchronous-result-objects"></a>Objetos de resultado asincrónico personalizados

En este tema se describe cómo implementar la [**interfaz IMFAsyncResult.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)

Es poco frecuente que tenga que escribir una implementación personalizada de la interfaz [**IMFAsyncResult.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) En casi todos los casos, la implementación Media Foundation estándar es suficiente. (Esta implementación la devuelve la [**función MFCreateAsyncResult).**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) Sin embargo, si escribe una implementación personalizada, hay algunos problemas que debe tener en cuenta.

En primer lugar, la implementación debe heredar [**la estructura MFASYNCRESULT.**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) Las Media Foundation de trabajo usan esta estructura internamente para enviar la operación. Inicialice todos los miembros de la estructura en cero, excepto el miembro **pCallback,** que contiene un puntero a la interfaz de devolución de llamada del autor de la llamada.

En segundo lugar, el objeto debe llamar [**a MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) en su constructor para bloquear el Media Foundation plataforma. Llame [**a MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) para desbloquear la plataforma. Estas funciones ayudan a evitar que la plataforma se apague antes de que se destruya el objeto. Para obtener más información, vea [Colas de trabajo.](work-queues.md)

En el código siguiente se muestra una implementación básica de la [**interfaz IMFAsyncResult.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) Como se muestra, este código no proporciona características adicionales más allá de la implementación Media Foundation estándar.


```C++
///////////////////////////////////////////////////////////////////////////////
//  CMyAsyncResult
//
//  Custom implementation of IMFAsyncResult. All implementations of this 
//  interface must inherit the MFASYNCRESULT structure.
// 
///////////////////////////////////////////////////////////////////////////////

class CMyAsyncResult : public MFASYNCRESULT
{
protected:
    LONG        m_cRef;             // Reference count.
    BOOL        m_bLockPlatform;    // Locked the Media Foundation platform?
    IUnknown*   m_pState;           // Caller's state object. 
    IUnknown*   m_pObject;  // Optional object. See IMFAsyncResult::GetObject.

    // Constructor. 
    CMyAsyncResult(IMFAsyncCallback *pCallback, IUnknown *pState, HRESULT *phr) :
        m_cRef(1),
        m_bLockPlatform(FALSE),
        m_pObject(NULL),
        m_pState(pState)
    {
        *phr = MFLockPlatform();

        m_bLockPlatform = TRUE;

        // Initialize the MFASYNCRESULT members.
        ZeroMemory(&this->overlapped, sizeof(OVERLAPPED));
        hrStatusResult = S_OK;
        dwBytesTransferred = 0;
        hEvent = NULL;

        this->pCallback = pCallback;
        if (pCallback)
        {
            this->pCallback->AddRef();
        }

        if (m_pState)
        {
            m_pState->AddRef();
        }
    }

    virtual ~CMyAsyncResult()
    {
        SafeRelease(&pCallback);
        SafeRelease(&m_pState);
        SafeRelease(&m_pObject);

        if (m_bLockPlatform)
        {
            MFUnlockPlatform();
        }
    }

public:
    // Static method to create an instance of this object.
    static HRESULT CreateInstance(
        IMFAsyncCallback *pCallback,    // Callback to invoke.
        IUnknown *pState,               // Optional state object.
        CMyAsyncResult **ppResult       // Receives a pointer to the object.
        )
    {
        HRESULT hr = S_OK;

        *ppResult = NULL;

        CMyAsyncResult *pResult = 
            new (std::nothrow) CMyAsyncResult(pCallback, pState, &hr);

        if (pResult == NULL)
        {
            return E_OUTOFMEMORY;
        }
        if (FAILED(hr))
        {
            delete pResult;
            return hr;
        }

        // If the callback is NULL, create an event that will be signaled.
        if (pCallback == NULL)
        {
            pResult->hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
            if (pResult->hEvent == NULL)
            {
                hr = HRESULT_FROM_WIN32(GetLastError());
            }
        }

        if (SUCCEEDED(hr))
        {
            *ppResult = pResult;  // Return the pointer to the caller.
        }
        else
        {
            pResult->Release();
        }
        return hr;
    }

    // SetObject: Sets the optional result object. 
    // (This method is not part of the interface.)
    HRESULT SetObject(IUnknown *pObject)
    {
        SafeRelease(&m_pObject);
        m_pObject = pObject;
        if (pObject)
        {
            m_pObject->AddRef();
        }
        return S_OK;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CMyAsyncResult, IMFAsyncResult),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
    
    // IMFAsyncResult methods.
    STDMETHODIMP GetState(IUnknown** ppunkState)
    {
        if (ppunkState == NULL)
        {
            return E_POINTER;
        }

        *ppunkState = m_pState;
        if (m_pState)
        {
            (*ppunkState)->AddRef();
        }

        return S_OK;
    }

    STDMETHODIMP GetStatus( void)
    {
        return hrStatusResult;
    }

    STDMETHODIMP STDMETHODCALLTYPE SetStatus(HRESULT hrStatus)
    {
        hrStatusResult = hrStatus;
        return S_OK;
    }

    STDMETHODIMP GetObject(IUnknown **ppObject)
    {
        if (ppObject == NULL)
        {
            return E_POINTER;
        }

        *ppObject = m_pObject;
        if (m_pObject)
        {
            (*ppObject)->AddRef();
        }
        return S_OK;
    }

    IUnknown* STDMETHODCALLTYPE GetStateNoAddRef()
    {
        return m_pState;  // Warning! Can be NULL. 
    }
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Colas de trabajo](work-queues.md)
</dt> <dt>

[Métodos de devolución de llamada asincrónicos](asynchronous-callback-methods.md)
</dt> </dl>

 

 



