---
description: Establecer un Administrador de credenciales
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Establecer un Administrador de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574793"
---
# <a name="setting-a-credential-manager"></a>Establecer un Administrador de credenciales

Una aplicación que proporciona credenciales al origen de red debe hacer lo siguiente:

1.  Implemente un objeto de administrador de credenciales que exponga la [**interfaz IMFNetCredentialManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager)
2.  Antes de crear el origen de red, cree un nuevo almacén de propiedades.
3.  Establezca la [**propiedad MFNETSOURCE \_ CREDENTIAL \_ MANAGER**](mfnetsource-credential-manager-property.md) en el almacén de propiedades. El valor de la propiedad es un puntero a la [**interfaz IMFNetCredentialManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager)
4.  Pase un puntero al almacén de propiedades al solucionador de origen, como se describe en [Configuración de un origen de medios.](configuring-a-media-source.md)

Los orígenes de red usan el administrador de credenciales para obtener las credenciales de usuario. Si el origen de red requiere credenciales para acceder a un recurso de red, llama al método [**DE CREDENCIALNET DE LA APLICACIÓN::BeginGetCredentials.**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) Esta llamada inicia una solicitud asincrónica para obtener las credenciales del usuario. El **método BeginGetCredentials** puede obtener las credenciales de la caché de credenciales o del usuario. Las credenciales se almacenan en un *objeto de credencial*. Una vez completada la operación, la aplicación invoca la interfaz de devolución de llamada para notificar al origen de red. El origen de red llama [**a IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) para completar la operación asincrónica.

Dado que se trata de una operación asincrónica, la aplicación debe enviar la devolución de llamada al final de la operación. Para obtener instrucciones paso a paso sobre cómo escribir un método asincrónico, vea [Escribir un método asincrónico.](writing-an-asynchronous-method.md)

En el ejemplo siguiente se muestra cómo establecer la [**propiedad MFNETSOURCE \_ CREDENTIAL \_ MANAGER**](mfnetsource-credential-manager-property.md) en el origen de red.


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de origen de red](network-source-authentication.md)
</dt> </dl>

 

 



