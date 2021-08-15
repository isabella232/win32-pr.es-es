---
description: Configuración de un origen de medios
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configuración de un origen de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e6737d643db2ee473214586cd7ded4f9596133dac5f4fb177df4d7b6b19757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880596"
---
# <a name="configuring-a-media-source"></a>Configuración de un origen de medios

Cuando se usa el [Solucionador de origen](source-resolver.md) para crear un origen multimedia, puede especificar un almacén de propiedades que contenga propiedades de configuración. Estas propiedades se usarán para inicializar el origen de medios. El conjunto de propiedades admitidas depende de la implementación del origen de medios. No todos los orígenes de medios definen las propiedades de configuración.

En la tabla siguiente se enumeran las propiedades de configuración de los orígenes multimedia que se proporcionan en Media Foundation. Los orígenes multimedia de terceros pueden definir sus propias propiedades personalizadas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Origen multimedia</th>
<th>Propiedades</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Origen de red</td>
<td>Consulte <a href="network-source-features.md">Características de origen de red.</a></td>
</tr>
<tr class="even">
<td>Origen de medios de ASF</td>
<td><ul>
<li><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></li>
<li><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

Para configurar un origen, realice los pasos siguientes.

1.  Llame **a PSCreateMemoryPropertyStore** para crear un nuevo almacén de propiedades. Esta función devuelve un **puntero IPropertyStore.**
2.  Llame **a IPropertyStore::SetValue** para establecer una o varias propiedades de configuración.
3.  Llame a una de las funciones de creación del solucionador de origen, [**como IMFSourceResolver::CreateObjectFromURL,**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)y pase el puntero **IPropertyStore** en el *parámetro pProps.*


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



La resolución de origen pasa el **puntero IPropertyStore** directamente al controlador de esquema o al controlador de flujo de bytes que crea el origen. La resolución de origen no intenta validar las propiedades.

Por lo general, estas propiedades se usan para la configuración avanzada. Si no proporciona un almacén de propiedades, el origen de medios seguirá funcionando correctamente con la configuración predeterminada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 



