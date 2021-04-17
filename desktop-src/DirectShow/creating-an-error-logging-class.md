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
# <a name="creating-an-error-logging-class"></a>Crear una clase de registro de errores

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En este tema se describe cómo implementar el registro de errores en los [servicios de edición de DirectShow](directshow-editing-services.md).

En primer lugar, declare una clase que implementará el registro de errores. La clase hereda la interfaz [**IAMErrorLog**](iamerrorlog.md) . Contiene declaraciones para los tres métodos **IUnknown** y para el método único en [IAMErrorLog](implementing-iamerrorlog.md). La declaración de clase es la siguiente:


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



La única variable miembro de la clase es m \_ lRef, que contiene el recuento de referencias del objeto.

A continuación, defina los métodos en **IUnknown**. En el ejemplo siguiente se muestra una implementación estándar para estos métodos:


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



Con el marco COM en su lugar, ahora puede implementar la interfaz **IAMErrorLog** . En la sección siguiente se describe cómo hacerlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores de registro](logging-errors.md)
</dt> </dl>

 

 



