---
description: Implementación de IMediaBuffer
ms.assetid: bde7cef8-f43e-4a11-8b77-fed5585d390a
title: Implementación de IMediaBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3425b3f612667a0b6577de385d59362bd8dafd0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678643"
---
# <a name="implementing-imediabuffer"></a>Implementación de IMediaBuffer

En el modelo de streaming de DMO predeterminado, los búferes se administran a través de la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) . El cliente de DMO es responsable de implementar un objeto que expone esta interfaz. La interfaz **IMediaBuffer** tiene tres métodos:

-   **GetBufferAndLength** devuelve la dirección del búfer (es decir, el bloque real de memoria que contiene los datos) y el tamaño de los datos válidos en el búfer.
-   **GetMaxLength** devuelve el tamaño del búfer.
-   **SetLength** especifica la longitud de los datos válidos en el búfer.

El procesamiento en contexto no requiere la interfaz **IMediaBuffer** . En el código siguiente se muestra una implementación mínima de **IMediaBuffer**:


```C++
//  CMediaBuffer class.
#include <dmo.h>
class CMediaBuffer : public IMediaBuffer
{
private:
    DWORD        m_cbLength;
    const DWORD  m_cbMaxLength;
    LONG         m_nRefCount;  // Reference count
    BYTE         *m_pbData;


    CMediaBuffer(DWORD cbMaxLength, HRESULT& hr) :
        m_nRefCount(1),
        m_cbMaxLength(cbMaxLength),
        m_cbLength(0),
        m_pbData(NULL)
    {
        m_pbData = new BYTE[cbMaxLength];
        if (!m_pbData) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    ~CMediaBuffer()
    {
        if (m_pbData) 
        {
            delete [] m_pbData;
        }
    }

public:

    // Function to create a new IMediaBuffer object and return 
    // an AddRef'd interface pointer.
    static HRESULT Create(long cbMaxLen, IMediaBuffer **ppBuffer)
    {
        HRESULT hr = S_OK;
        CMediaBuffer *pBuffer = NULL;

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }

        pBuffer = new CMediaBuffer(cbMaxLen, hr);

        if (pBuffer == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
           *ppBuffer = pBuffer;
           (*ppBuffer)->AddRef();
        }

        if (pBuffer)
        {
            pBuffer->Release();
        }
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        if (ppv == NULL) 
        {
            return E_POINTER;
        }
        else if (riid == IID_IMediaBuffer || riid == IID_IUnknown) 
        {
            *ppv = static_cast<IMediaBuffer *>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRef = InterlockedDecrement(&m_nRefCount);
        if (lRef == 0) 
        {
            delete this;
            // m_cRef is no longer valid! Return lRef.
        }
        return lRef;  
    }

    // IMediaBuffer methods.
    STDMETHODIMP SetLength(DWORD cbLength)
    {
        if (cbLength > m_cbMaxLength) 
        {
            return E_INVALIDARG;
        }
        m_cbLength = cbLength;
        return S_OK;
    }

    STDMETHODIMP GetMaxLength(DWORD *pcbMaxLength)
    {
        if (pcbMaxLength == NULL) 
        {
            return E_POINTER;
        }
        *pcbMaxLength = m_cbMaxLength;
        return S_OK;
    }

    STDMETHODIMP GetBufferAndLength(BYTE **ppbBuffer, DWORD *pcbLength)
    {
        // Either parameter can be NULL, but not both.
        if (ppbBuffer == NULL && pcbLength == NULL) 
        {
            return E_POINTER;
        }
        if (ppbBuffer) 
        {
            *ppbBuffer = m_pbData;
        }
        if (pcbLength) 
        {
            *pcbLength = m_cbLength;
        }
        return S_OK;
    }
};

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hospedar directamente un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



