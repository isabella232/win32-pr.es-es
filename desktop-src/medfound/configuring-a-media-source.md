---
description: Configuración de un origen multimedia
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configuración de un origen multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 809d215cf282dba1e65c21316fafda47684a2151
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257951"
---
# <a name="configuring-a-media-source"></a>Configuración de un origen multimedia

Cuando se usa el [Solucionador de origen](source-resolver.md) para crear un origen multimedia, puede especificar un almacén de propiedades que contenga propiedades de configuración. Estas propiedades se usarán para inicializar el origen multimedia. El conjunto de propiedades admitidas depende de la implementación del origen multimedia. No todos los orígenes de medios definen las propiedades de configuración.

En la tabla siguiente se enumeran las propiedades de configuración de los orígenes multimedia que se proporcionan en Media Foundation. Los orígenes multimedia de terceros pueden definir sus propias propiedades personalizadas.




| Origen multimedia | Propiedades | 
|--------------|------------|
| Origen de red | Consulte <a href="network-source-features.md">Características de origen de red</a>. | 
| Origen multimedia de ASF | <ul><li><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></li><li><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></li><li><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></li><li><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></li></ul> | 




 

Para configurar un origen, realice los pasos siguientes.

1.  Llame **a PSCreateMemoryPropertyStore para** crear un nuevo almacén de propiedades. Esta función devuelve un **puntero IPropertyStore.**
2.  Llame **a IPropertyStore::SetValue para** establecer una o varias propiedades de configuración.
3.  Llame a una de las funciones de creación del solucionador de origen, [**como IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)y pase el puntero **IPropertyStore** en el *parámetro pProps.*


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



El solucionador de origen pasa el **puntero IPropertyStore** directamente al controlador de esquema o al controlador de flujo de bytes que crea el origen. El solucionador de origen no intenta validar las propiedades.

Por lo general, estas propiedades se usan para la configuración avanzada. Si no proporciona un almacén de propiedades, el origen de medios seguirá funcionando correctamente con la configuración predeterminada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 



