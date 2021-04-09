---
description: El receptor de archivos ASF es una implementación de IMFMediaSink proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios ASF y el uso general, consulte receptores multimedia ASF.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Agregar metadatos al receptor de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bb63a10d935b52e6d048dbc5dcd07370dd2ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082167"
---
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="99686-104">Agregar metadatos al receptor de archivos</span><span class="sxs-lookup"><span data-stu-id="99686-104">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="99686-105">El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo.</span><span class="sxs-lookup"><span data-stu-id="99686-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="99686-106">Para obtener información sobre el modelo de objetos y el uso general de los receptores de medios ASF, consulte [receptores de medios ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="99686-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="99686-107">Después de [crear el receptor de archivos ASF](creating-the-asf-file-sink.md), debe configurarse con información sobre los flujos y la información de codificación del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="99686-107">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="99686-108">Estos procedimientos se describen en [Agregar información de secuencias al receptor de archivos ASF](adding-stream-information-to-the-asf-file-sink.md) y [establecer las propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="99686-108">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="99686-109">Además, también puede agregar información de metadatos que incluye pares de nombre/valor, como "autor", título ".</span><span class="sxs-lookup"><span data-stu-id="99686-109">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="99686-110">En este tema se describe el proceso de agregar información de metadatos al receptor de archivos para que aparezca en el [objeto de encabezado ASF](asf-file-structure.md)final.</span><span class="sxs-lookup"><span data-stu-id="99686-110">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="99686-111">Puede agregar información de metadatos al receptor de archivos ASF antes de compilar la topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="99686-111">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="99686-112">El objeto ContentInfo de ASF del receptor de archivos realiza un seguimiento de las propiedades de metadatos y se expone a la aplicación a través de la interfaz [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="99686-112">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="99686-113">Algunas de estas propiedades, como "IsVBR", que indica si el archivo contiene secuencias de velocidad de bits variable (VBR), se establecen automáticamente en el receptor de archivos mediante el análisis de las propiedades de codificación de la secuencia que se establecen.</span><span class="sxs-lookup"><span data-stu-id="99686-113">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="99686-114">Para obtener una lista completa de las propiedades, vea el tema "lista de atributos" en la documentación del SDK de formato.</span><span class="sxs-lookup"><span data-stu-id="99686-114">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="99686-115">Uso de la interfaz IMFMetadata en el receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="99686-115">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="99686-116">Consulte el objeto de receptor de archivo ASF para obtener un puntero a su implementación de la interfaz [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="99686-116">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="99686-117">Llame a [**IMFMetadataProvider:: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) para obtener un puntero [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="99686-117">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="99686-118">Se omite el parámetro *pPresentationDescriptor* y la aplicación puede pasar **null**.</span><span class="sxs-lookup"><span data-stu-id="99686-118">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="99686-119">Si la aplicación pasa cero como identificador de secuencia en el parámetro *dwStreamIdentifier* , el método recupera los metadatos que se aplican a todo el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="99686-119">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="99686-120">De lo contrario, solo se recuperan los metadatos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="99686-120">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="99686-121">Llame a [**IMFMetadata:: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para recuperar la lista de propiedades de codificación de archivos establecida en el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="99686-121">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="99686-122">Llame a [**IMFMetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) para obtener los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="99686-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="99686-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99686-123">Example</span></span>

<span data-ttu-id="99686-124">En el ejemplo de código siguiente se muestra cómo enumerar los nombres de propiedad y los valores que se establecen en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="99686-124">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="99686-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99686-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99686-126">Receptores de medios ASF</span><span class="sxs-lookup"><span data-stu-id="99686-126">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="99686-127">Componentes ASF de capa de canalización</span><span class="sxs-lookup"><span data-stu-id="99686-127">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="99686-128">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="99686-128">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



