---
description: A partir Windows 7, Microsoft Media Foundation los metadatos a través de la interfaz IPropertyStore.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Proveedores de metadatos de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31960ed41743a86b62b63555236d2876166a14b098f0692f3d6cb22b051e338e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713365"
---
# <a name="shell-metadata-providers"></a>Proveedores de metadatos de Shell

A partir Windows 7, Microsoft Media Foundation los metadatos a través de la [**interfaz IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Los metadatos obtenidos mediante el proceso definido en este tema solo deben usarse para el acceso de solo lectura. No se admite la escritura de datos mediante este proceso. Puede crear un objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) con fines de escritura mediante un identificador de clase (CLSID) obtenido de [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).

## <a name="reading-metadata"></a>Leer metadatos

Para leer metadatos de un origen multimedia, realice los pasos siguientes:

1.  Obtenga un puntero a la [**interfaz IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia. Puede usar la interfaz [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obtener un puntero **IMFMediaSource.**
2.  Llame [**a MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) en el origen multimedia para obtener un puntero a la [**interfaz IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) En el *parámetro guidService* de **MFGetService**, especifique el valor **MF PROPERTY HANDLER \_ \_ \_ SERVICE**. Si el origen no admite la interfaz **IPropertyStore,** **MFGetService** devuelve **MF E \_ \_ UNSUPPORTED \_ SERVICE**.
3.  Llame [**a los métodos IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para enumerar las propiedades de metadatos.

En el código siguiente se muestran estos pasos. Suponga que `DisplayProperty` es una función que muestra un valor **PROPVARIANT.**


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



Para obtener una lista de claves de propiedad de metadatos, vea [Propiedades de metadatos para archivos multimedia.](metadata-properties-for-media-files.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Metadatos multimedia](media-metadata.md)
</dt> </dl>

 

 
