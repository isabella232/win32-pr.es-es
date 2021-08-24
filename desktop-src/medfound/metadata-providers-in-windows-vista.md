---
description: En Windows Vista, Microsoft Media Foundation expone los metadatos a través de la interfaz DE METADATOSMetadata.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Proveedores de metadatos en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1edf65b59e0f47e603b057f49a76d8721b8733849937cb29fd0afbe0b9b44920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827075"
---
# <a name="metadata-providers-in-windows-vista"></a>Proveedores de metadatos en Windows Vista

En Windows Vista, Microsoft Media Foundation expone metadatos a través de la [**interfaz DE METADATOSMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)

## <a name="reading-metadata"></a>Leer metadatos

Para leer metadatos de un origen multimedia, realice los pasos siguientes:

1.  Obtenga un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia. Puede usar la interfaz [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obtener un puntero **DE MÉTODOMEDIASOURCE.**
2.  Llame [**a IMFMediaSource::CreatePresentationDescriptor para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) obtener el descriptor de presentación del origen multimedia.
3.  Llame [**a MFGetService en**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) el origen de medios para obtener un puntero a la interfaz [**MFMetadataProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) En el *parámetro guidService* de **MFGetService**, especifique el valor **MF METADATA PROVIDER \_ \_ \_ SERVICE**. Si el origen no admite la interfaz **MFMetadataProvider,** **MFGetService** devuelve **MF E \_ \_ UNSUPPORTED \_ SERVICE**.
4.  Llame [**a IMFMetadataProvider::GetMFMetadata y**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) pase un puntero al descriptor de presentación. Este método devuelve un puntero a la [**interfaz IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)
    -   Para obtener los metadatos de nivel de flujo, llame primero [**a IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) para obtener el identificador de flujo. A continuación, pase el identificador de flujo en el *parámetro dwStreamIdentifier* [**de GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).
    -   Para obtener metadatos de nivel de presentación, *establezca dwStreamIdentifier* en cero.
5.  \[Llame \] opcional a LA PROPIEDAD DE METADATOSMetadata::GetAllLanguages para obtener una lista de los idiomas en los que están disponibles los metadatos. [](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) Los idiomas se identifican mediante etiquetas de idioma compatibles con RFC 1766.
6.  \[Llame \] opcional [**a IMFMetadata::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) para seleccionar el idioma.
7.  \[Llame \] [**opcionalmente a IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para obtener una lista de los nombres de todas las propiedades de metadatos de esta secuencia o presentación.
8.  Llame [**a IMFMetadata::GetProperty para**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) obtener un valor de propiedad de metadatos específico y pase el nombre de la propiedad.

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



En el código siguiente se muestran los pasos del 7 al 8. Suponga que `DisplayProperty` es una función que muestra un valor **PROPVARIANT.**


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

[Metadatos multimedia](media-metadata.md)
</dt> <dt>

[Proveedores de metadatos de shell](shell-metadata-providers.md)
</dt> </dl>

 

 



