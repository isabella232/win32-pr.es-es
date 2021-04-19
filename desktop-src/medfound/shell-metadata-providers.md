---
description: A partir de Windows 7, Microsoft Media Foundation expone metadatos a través de la interfaz IPropertyStore.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Proveedores de metadatos de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715488"
---
# <a name="shell-metadata-providers"></a>Proveedores de metadatos de Shell

A partir de Windows 7, Microsoft Media Foundation expone metadatos a través de la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Los metadatos obtenidos mediante el proceso definido en este tema solo deben usarse para el acceso de solo lectura. No se admite la escritura de datos con este proceso. Puede crear un objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) con fines de escritura mediante un identificador de clase (CLSID) Obtenido de [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).

## <a name="reading-metadata"></a>Leer metadatos

Para leer los metadatos de un origen multimedia, realice los pasos siguientes:

1.  Obtiene un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia. Puede usar la interfaz [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obtener un puntero **IMFMediaSource** .
2.  Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) en el origen de medios para obtener un puntero a la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . En el parámetro *guidService* de **MFGetService**, especifique el valor **del \_ \_ \_ servicio de controlador de propiedades MF**. Si el origen no admite la interfaz **IPropertyStore** , **MFGetService** devuelve el **\_ servicio MF E \_ no compatible \_**.
3.  Llame a los métodos de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para enumerar las propiedades de metadatos.

En el código siguiente se muestran estos pasos. Supongamos que `DisplayProperty` es una función que muestra un valor de **PROPVARIANT** .


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



Para obtener una lista de las claves de propiedad de metadatos, consulte [propiedades de metadatos para archivos multimedia](metadata-properties-for-media-files.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Metadatos de medios](media-metadata.md)
</dt> </dl>

 

 
