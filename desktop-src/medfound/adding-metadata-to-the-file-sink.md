---
description: Obtenga información sobre cómo agregar metadatos al receptor de archivos ASF, que una aplicación puede usar para archivar datos multimedia de ASF en un archivo.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Agregar metadatos al receptor de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ea86a09ff9e3d2a25bbf8d00d46691fd803365
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409968"
---
# <a name="adding-metadata-to-the-file-sink"></a>Agregar metadatos al receptor de archivos

El receptor de archivos DE ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia de ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios de ASF y el uso general, vea [Receptores multimedia de ASF.](asf-media-sinks.md)

Después [de crear el receptor de archivos ASF,](creating-the-asf-file-sink.md)debe configurarse con información sobre las secuencias y la información de codificación en el archivo de salida. Estos procedimientos se describen [en Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) y Setting Properties in the File [Sink](setting-properties-in-the-file-sink.md). Además, también puede agregar información de metadatos que incluya pares nombre-valor, como "Autor", Título". En este tema se describe el proceso de agregar información de metadatos al receptor de archivos para que aparezca en el objeto de [encabezado ASF final.](asf-file-structure.md)

Puede agregar información de metadatos al receptor de archivos ASF antes de compilar la topología de codificación. El objeto ContentInfo de ASF para el receptor de archivos realiza un seguimiento de las propiedades de los metadatos y se exponen a la aplicación a través de la [**interfaz DESMETADATA.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) Algunas de estas propiedades, como "IsVBR", que indica si el archivo contiene secuencias de velocidad de bits variable (VBR), las establece automáticamente el receptor de archivos analizando las propiedades de codificación de secuencias establecidas.

Para obtener una lista completa de las propiedades, consulte el tema "Lista de atributos" en la documentación del SDK de formato.

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a>Uso de la interfaz IMFMetadata en el receptor de archivos ASF

1.  Consulte el objeto de receptor de archivos ASF para obtener un puntero a su implementación de la interfaz [**IMFMetadataProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)
2.  Llame [**a IMFMetadataProvider::GetMFMetadata para**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) obtener un puntero DE TIPO [**IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)

    El *parámetro pPresentationDescriptor* se omite y la aplicación puede pasar **NULL.** Si la aplicación pasa cero como identificador de flujo en el parámetro *dwStreamIdentifier,* el método recupera los metadatos que se aplican a todo el archivo ASF. De lo contrario, solo se recuperan los metadatos de la secuencia.

3.  Llame [**a IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para recuperar la lista de propiedades de codificación de archivos establecidas en el contenido multimedia.
4.  Llame [**a IMFMetadata::GetProperty para**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) obtener los valores de propiedad.

## <a name="example"></a>Ejemplo

En el código de ejemplo siguiente se muestra cómo enumerar los nombres de propiedad y los valores que se establecen en el archivo ASF.


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Receptores multimedia de ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



