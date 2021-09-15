---
description: Implementación de IMFNetCredentialManager
ms.assetid: 3eb2afec-195c-4d8d-8e08-7e6ec7c572f8
title: Implementación de IMFNetCredentialManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c026f2c12b2ff248032a56d9c48a0e0e1576c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581048"
---
# <a name="implementing-imfnetcredentialmanager"></a>Implementación de IMFNetCredentialManager

En el [**método IMFNetCredentialManager::BeginGetCredentials,**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) haga lo siguiente.

1.  Si aún no tiene un puntero [**DE LA CREDENCIAL DE CREDENCIALCACHE,**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) llame a [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) para crear el objeto de caché de credenciales. Almacene este puntero.
2.  Llame [**a IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential). Establezca las marcas en el *parámetro dwAuthenticationFlags* de la siguiente manera:
    -   Si el **miembro hrOp** de la estructura [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) es igual a **NS \_ E PROXY \_ \_ ACCESSDENIED,** establezca la marca **MFNET AUTHENTICATION \_ \_ PROXY.**
    -   Si **fClearTextPackage es** **TRUE,** establezca la marca **MFNET AUTHENTICATION CLEAR \_ \_ \_ TEXT.**
    -   Si **fAllowLoggedOnUser** es **TRUE,** establezca la marca **DE USUARIO DE AUTENTICACIÓN DE MFNET \_ \_ \_ \_ INICIADA.**
3.  El [**método GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) devuelve un puntero [**DE CREDENCIAL DE CREDENCIAL Y,**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) posiblemente, la marca REQUIRE \_ PROMPT. Almacene el **puntero DECREDENTIALNetCredential.**
4.  Si [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) no devuelve la **marca REQUIRE \_ PROMPT,** ha terminado. Vaya al paso 9.
5.  De lo contrario, [**si GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) devuelve la marca **REQUIRE \_ PROMPT,** debe solicitar al usuario su nombre de usuario y contraseña.
6.  Si **fClearTextPackage es** **FALSE,** cifre las credenciales.
7.  Llame [**a IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) y [**ASENETCREDENTIAL::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) para establecer el nombre y la contraseña del usuario en el objeto de credenciales.
8.  Opcionalmente, llame a [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) para actualizar el objeto de caché de credenciales con las preferencias del usuario para almacenar y enviar credenciales.
9.  Invoque la devolución de [**llamada DECALLBACKAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) llamando [**a MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).

En el [**método IMFNetCredentialManager::EndGetCredentials,**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) devuelva el puntero DE LA CREDENCIAL [**DE LA CREDENCIAL OBTENIDO**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) en el método [**BeginGetCredentials.**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials)

En el [**método IMFNetCredentialManager::SetGood,**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) pase los parámetros de entrada directamente al [**método IMFNetCredentialCache::SetGood.**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) Esto notifica a la caché de credenciales si el servidor aceptó las credenciales.

Si necesita preguntar al usuario (paso 5) o cifrar las credenciales (paso 6), debe hacerlo en un subproceso de cola de trabajo, para que no bloquee la canalización Microsoft Media Foundation trabajo. Llame [**a MFPutWorkItem y,**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) a continuación, realice los pasos restantes dentro de la devolución de llamada de cola de trabajo.

> [!Note]  
> Tenga en cuenta [**que beginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) puede invocarse mientras se crea el origen de red. Por lo tanto, si crea el origen de red mediante una llamada al método [**sincrónico IMFSourceResolver::CreateObjectFromURL,**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) el subproceso que realiza la llamada podría bloquearse mientras se adquieren las credenciales. Por lo tanto, se recomienda usar en su lugar el [**método ASYNCHRONOUSSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) asincrónico.

 

## <a name="example"></a>Ejemplo

En este ejemplo se muestra un tipo de comportamiento que podría proporcionar un administrador de credenciales.

Esta es una declaración de la clase que implementa [**ELMANAGERNetCredentialManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager)


```C++
class CCredentialManager : public IMFNetCredentialManager, IMFAsyncCallback 
{
    long                    m_cRef;
    IMFNetCredentialCache   *m_pCredentialCache;

public:
    CCredentialManager () : m_cRef(1), m_pCredentialCache(NULL)
    { 
    }
    ~CCredentialManager()
    {
        SafeRelease(&m_pCredentialCache);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCredentialManager, IMFNetCredentialManager),
            QITABENT(CCredentialManager, IMFAsyncCallback),
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

    STDMETHODIMP BeginGetCredentials(
        MFNetCredentialManagerGetParam* pParam,
        IMFAsyncCallback* pCallback,
        IUnknown* pState
        );

    STDMETHODIMP EndGetCredentials(
        IMFAsyncResult* pResult, 
        IMFNetCredential** ppCred);

    STDMETHODIMP SetGood(IMFNetCredential* pCred, BOOL fGood)
    {
        if (!pCred)
        {
            return E_POINTER;
        }

        return m_pCredentialCache->SetGood(pCred, fGood);
    }


    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



Para realizar un seguimiento del estado de [**la operación BeginGetCredentials,**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) la clase usa el siguiente objeto auxiliar:


```C++
// Holds state information for the GetCredentials operation, so that work can 
// be moved to a work-queue thread.

struct CredentialOp : public IUnknown
{
    long                m_cRef;
    IMFNetCredential    *m_pCredential;
    DWORD               m_dwFlags;

    CredentialOp(IMFNetCredential *pCredential) 
        : m_cRef(1), m_dwFlags(0), m_pCredential(pCredential)
    {
        m_pCredential->AddRef();
    }

    ~CredentialOp()
    {
        SafeRelease(&m_pCredential);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CredentialOp, IUnknown),
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
};
```



El [**método BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) crea la caché de credenciales y obtiene un [**puntero DE CREDENCIAL DE CREDENCIAL.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) Si se debe solicitar al usuario (indicado por la marca **REQUIRE \_ PROMPT),** el método llama a [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) para poner en cola un nuevo elemento de trabajo:


```C++
STDMETHODIMP CCredentialManager::BeginGetCredentials(
    MFNetCredentialManagerGetParam* pParam,
    IMFAsyncCallback* pCallback,
    IUnknown* pState
    )
{
    if (!pParam || !pCallback)
    {
        return E_POINTER;
    }

    DWORD dwAuthenticationFlags = 0;
    DWORD dwRequirementFlags = 0;

    if (pParam->hrOp == NS_E_PROXY_ACCESSDENIED)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_PROXY;
    }

    if (pParam->fAllowLoggedOnUser)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_LOGGED_ON_USER;
    }

    if (pParam->fClearTextPackage)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_CLEAR_TEXT;
    }

    IMFNetCredential *pCredential =  NULL;
    IMFAsyncResult* pResult = NULL;

    HRESULT hr = S_OK;

    if (m_pCredentialCache == NULL)
    {
        hr = MFCreateCredentialCache(&m_pCredentialCache);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    hr = m_pCredentialCache->GetCredential(
        pParam->pszUrl, 
        pParam->pszRealm, 
        dwAuthenticationFlags, 
        &pCredential, 
        &dwRequirementFlags
        );

    if (FAILED(hr))
    {
        goto done;
    }

    if( ( dwRequirementFlags & REQUIRE_PROMPT ) == 0 )
    {
        // The credential is good to use. Prompting the user is not required.
        hr = S_OK;
        goto done;
    }

    // The credential requires prompting the user. 
    CredentialOp *pOp = new (std::nothrow) CredentialOp(pCredential);

    if (pOp == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Set flags. Use these to inform the user if the credentials will
    // be sent in plaintext or saved in the credential cache.

    if (pParam->fClearTextPackage)
    {
        // Notify the user that credentials will be sent in plaintext.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT;
    }

    if(dwRequirementFlags & REQUIRE_SAVE_SELECTED )
    {
        // Credentials will be saved in the cache by default.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_SAVE;
    }

    // NOTE: The application should enable to user to deselect these two flags;
    // for example, through check boxes in the prompt dialog.


    // Now queue the work item.

    hr = MFCreateAsyncResult(pOp, pCallback, pState, &pResult);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION, this, pResult);

done:
    SafeRelease(&pResult);
    SafeRelease(&pCredential);
    SafeRelease(&pOp);
    return hr;
}
```



El subproceso de cola de trabajo llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), que solicita al usuario y, a continuación, llama a [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar el puntero de devolución de llamada proporcionado en [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).


```C++
STDMETHODIMP CCredentialManager::Invoke(IMFAsyncResult* pResult)
{
    IUnknown *pState = NULL;
    IMFAsyncResult *pGetCredentialsResult = NULL;
    IUnknown *pOpState = NULL;

    CredentialOp *pOp = NULL;   // not AddRef'd

    HRESULT hr = pResult->GetState(&pState);

    if (SUCCEEDED(hr))
    {
        hr = pState->QueryInterface(IID_PPV_ARGS(&pGetCredentialsResult));
    }

    if (SUCCEEDED(hr))
    {
        hr = pGetCredentialsResult->GetObject(&pOpState);
    }

    if (SUCCEEDED(hr))
    {
        pOp = static_cast<CredentialOp*>(pOpState);

        // Display a dialog for the user to enter user name and password.
        hr = PromptUserCredentials(pOp);
    }

    if (SUCCEEDED(hr) && m_pCredentialCache)
    {
        // Update with options set by the user.
        hr = m_pCredentialCache->SetUserOptions(
            pOp->m_pCredential, 
            pOp->m_dwFlags
            );
    }

    if (pGetCredentialsResult)
    {
        pGetCredentialsResult->SetStatus(hr);
        MFInvokeCallback(pGetCredentialsResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pGetCredentialsResult);
    SafeRelease(&pOpState);
    return S_OK;
}
```



El [**método EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) completa la operación devolviendo el puntero [**DE LA CREDENCIAL DE CREDENCIAL AL**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) autor de la llamada.


```C++
STDMETHODIMP CCredentialManager::EndGetCredentials(
    IMFAsyncResult* pResult, 
    IMFNetCredential** ppCred
    )
{
    if (!pResult || !ppCred)
    {
        return E_POINTER;
    }

    *ppCred = NULL;

    IUnknown *pUnk = NULL;

    // Check the result of the asynchronous operation.
    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        // The operation failed.
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    CredentialOp *pOp = static_cast<CredentialOp*>(pUnk);

    *ppCred = pOp->m_pCredential;
    pOp->m_pCredential = NULL;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de origen de red](network-source-authentication.md)
</dt> </dl>

 

 



