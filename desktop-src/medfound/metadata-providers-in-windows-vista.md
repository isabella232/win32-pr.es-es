---
description: En Windows Vista, Microsoft Media Foundation expone metadatos a través de la interfaz IMFMetadata.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Proveedores de metadatos en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677438"
---
# <a name="metadata-providers-in-windows-vista"></a>Proveedores de metadatos en Windows Vista

En Windows Vista, Microsoft Media Foundation expone metadatos a través de la interfaz [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .

## <a name="reading-metadata"></a>Leer metadatos

Para leer los metadatos de un origen multimedia, realice los pasos siguientes:

1.  Obtiene un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia. Puede usar la interfaz [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obtener un puntero **IMFMediaSource** .
2.  Llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obtener el descriptor de presentación del origen multimedia.
3.  Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) en el origen de medios para obtener un puntero a la interfaz [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) . En el parámetro *guidService* de **MFGetService**, especifique el valor **de \_ \_ \_ servicio del proveedor de metadatos MF**. Si el origen no admite la interfaz **IMFMetadataProvider** , **MFGetService** devuelve el **\_ servicio MF E \_ no compatible \_**.
4.  Llame a [**IMFMetadataProvider:: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) y pase un puntero al descriptor de presentación. Este método devuelve un puntero a la interfaz [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .
    -   Para obtener los metadatos de nivel de secuencia, llame primero a [**IMFStreamDescriptor:: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) para obtener el identificador de flujo. Después, pase el identificador de flujo en el parámetro *dwStreamIdentifier* de [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).
    -   Para obtener los metadatos en el nivel de presentación, establezca *dwStreamIdentifier* en cero.
5.  \[\]Llamada opcional [**IMFMetadata:: GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) para obtener una lista de los idiomas en los que los metadatos están disponibles. Los idiomas se identifican mediante etiquetas de idioma compatibles con RFC 1766.
6.  \[\]Llamada opcional [**IMFMetadata:: SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) para seleccionar el idioma.
7.  \[\]Llamada opcional [**IMFMetadata:: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para obtener una lista de los nombres de todas las propiedades de metadatos de esta secuencia o presentación.
8.  Llame a [**IMFMetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) para obtener un valor de propiedad de metadatos específico, pasando el nombre de la propiedad.

En el código siguiente se muestran los pasos 2 a 4:


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



En el código siguiente se muestran los pasos 7 y 8. Supongamos que `DisplayProperty` es una función que muestra un valor de **PROPVARIANT** .


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Metadatos de medios](media-metadata.md)
</dt> <dt>

[Proveedores de metadatos de Shell](shell-metadata-providers.md)
</dt> </dl>

 

 



