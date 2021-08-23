---
title: Agregación
description: Agregación es el mecanismo de reutilización de objetos en el que el objeto externo expone interfaces del objeto interno como si se hubieran implementado en el propio objeto externo.
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4855b1fa3a614d190b8f192aeee2e7cf3d3d53bbdce589a1363e0398f70430c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731725"
---
# <a name="aggregation"></a>Agregación

Agregación es el mecanismo de reutilización de objetos en el que el objeto externo expone interfaces del objeto interno como si se hubieran implementado en el propio objeto externo. Esto resulta útil cuando el objeto externo delega cada llamada a una de sus interfaces en la misma interfaz del objeto interno. La agregación está disponible por comodidad para evitar sobrecargas de implementación adicionales en el objeto externo en este caso. La agregación es realmente un caso especializado [de contención o delegación.](containment-delegation.md)

La agregación es casi tan sencilla de implementar como la contención, excepto para las tres funciones [**IUnknown:**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)y [**Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) La captura es que, desde la perspectiva del cliente, cualquier **función IUnknown** del objeto externo debe afectar al objeto externo. Es decir, **AddRef** y **Release afectan** al objeto externo y **QueryInterface** expone todas las interfaces disponibles en el objeto externo. Sin embargo, si el objeto externo simplemente expone la interfaz de un objeto interno como propia, los miembros **IUnknown** de ese objeto interno a los que se llama a través de esa interfaz se comportarán de forma diferente a los miembros **IUnknown** en las interfaces del objeto externo, una infracción absoluta de las reglas y propiedades que rigen **IUnknown**.

La solución es que la agregación requiere una implementación explícita de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) en el objeto interno y la delegación de los métodos **IUnknown** de cualquier otra interfaz a los métodos **IUnknown** del objeto externo.

## <a name="creating-aggregable-objects"></a>Crear objetos aggregable

La creación de objetos que se pueden agregar es opcional; sin embargo, es fácil de hacer y proporciona ventajas significativas. Las reglas siguientes se aplican a la creación de un objeto aggregable:

-   La implementación del objeto aggregable (o interno) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para su [**interfaz IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) controla el recuento de referencias del objeto interno, y esta implementación no debe delegar en el desconocido del objeto externo (el **IUnknown de control).**
-   La implementación del objeto aggregable (o interno) de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para sus otras interfaces debe delegar en el [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de control y no debe afectar directamente al recuento de referencias del objeto interno.
-   El [**IUnknown interno**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) debe implementar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) solo para el objeto interno.
-   El objeto aggregable no debe llamar a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) cuando se mantiene una referencia al [**puntero IUnknown de**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) control.
-   Cuando se crea el objeto , si se solicita cualquier interfaz que no sea [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) la creación debe producir un error con E \_ NOINTERFACE.

El fragmento de código siguiente muestra una implementación correcta de un objeto aggregable mediante el método de clase anidada de implementar interfaces:


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



## <a name="aggregating-objects"></a>Agregar objetos

Al desarrollar un objeto aggregable, se aplican las reglas siguientes:

-   Al crear el objeto interno, el objeto externo debe solicitar explícitamente su [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).
-   El objeto externo debe proteger su implementación de [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) de la reenencia con un recuento de referencias artificial alrededor de su código de destrucción.
-   El objeto externo debe llamar a su método **IUnknown** [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) de control si consulta un puntero a cualquiera de las interfaces del objeto interno. Para liberar este puntero, el objeto externo llama a su método **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) de control, seguido de **Release en** el puntero del objeto interno.
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   El objeto externo no debe delegar a la vista una consulta para ninguna interfaz no reconocida en el objeto interno, a menos que ese comportamiento sea específicamente la intención del objeto externo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contención y delegación](containment-delegation.md)
</dt> </dl>

 

 