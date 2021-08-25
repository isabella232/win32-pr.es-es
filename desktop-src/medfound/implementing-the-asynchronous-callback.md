---
description: Implementar la devolución de llamada asincrónica
ms.assetid: c2c9d0f7-038b-4f23-985c-b812908d71a7
title: Implementar la devolución de llamada asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f064c9a3d16ebf54342065439415557ea4621c72a57a0a52e4f4c9ed65721e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941895"
---
# <a name="implementing-the-asynchronous-callback"></a>Implementar la devolución de llamada asincrónica

En el código siguiente se muestra el marco básico necesario para implementar la [**interfaz IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) En este ejemplo, el [**método Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) se declara como un método virtual puro. La implementación de este método dependerá del método asincrónico al que se llame. Para obtener más información, vea [Llamar a métodos asincrónicos.](calling-asynchronous-methods.md)


```C++
#include <shlwapi.h>

class CAsyncCallback : public IMFAsyncCallback 
{
public:
    CAsyncCallback () : m_cRef(1) { }
    virtual ~CAsyncCallback() { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CAsyncCallback, IMFAsyncCallback),
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
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult) = 0;
    // TODO: Implement this method. 

    // Inside Invoke, IMFAsyncResult::GetStatus to get the status.
    // Then call the EndX method to complete the operation. 

private:
    long    m_cRef;
};
```



Este código siguiente muestra una implementación de ejemplo de una clase que se deriva de `CAsyncCallback` :


```C++
class CMyCallback : public CAsyncCallback
{
    HANDLE m_hEvent;
    IMFByteStream *m_pStream;

    HRESULT m_hrStatus;
    ULONG   m_cbRead;

public:

    CMyCallback(IMFByteStream *pStream, HRESULT *phr) 
        : m_pStream(pStream), m_hrStatus(E_PENDING), m_cbRead(0)
    {
        *phr = S_OK;

        m_pStream->AddRef();

        m_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

        if (m_hEvent == NULL)
        {
            *phr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    ~CMyCallback()
    {
        m_pStream->Release();
        CloseHandle(m_hEvent);
    }

    HRESULT WaitForCompletion(DWORD msec)
    {
        DWORD result = WaitForSingleObject(m_hEvent, msec);

        switch (result)
        {
        case WAIT_TIMEOUT:
            return E_PENDING;

        case WAIT_ABANDONED:
        case WAIT_OBJECT_0:
            return m_hrStatus;

        default:
            return HRESULT_FROM_WIN32(GetLastError());
        }
    }

    ULONG   GetBytesRead() const { return m_cbRead; }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
};
```



Este ejemplo señala un evento dentro del [**método Invoke.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Para obtener una explicación de las distintas opciones, vea [Llamar a métodos asincrónicos.](calling-asynchronous-methods.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Métodos de devolución de llamada asincrónicos](asynchronous-callback-methods.md)
</dt> </dl>

 

 



