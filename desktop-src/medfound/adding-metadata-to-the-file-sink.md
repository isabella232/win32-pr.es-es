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
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="562b6-103">Agregar metadatos al receptor de archivos</span><span class="sxs-lookup"><span data-stu-id="562b6-103">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="562b6-104">El receptor de archivos DE ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia de ASF en un archivo.</span><span class="sxs-lookup"><span data-stu-id="562b6-104">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="562b6-105">Para obtener información sobre el modelo de objetos de los receptores de medios de ASF y el uso general, vea [Receptores multimedia de ASF.](asf-media-sinks.md)</span><span class="sxs-lookup"><span data-stu-id="562b6-105">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="562b6-106">Después [de crear el receptor de archivos ASF,](creating-the-asf-file-sink.md)debe configurarse con información sobre las secuencias y la información de codificación en el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="562b6-106">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="562b6-107">Estos procedimientos se describen [en Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) y Setting Properties in the File [Sink](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="562b6-107">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="562b6-108">Además, también puede agregar información de metadatos que incluya pares nombre-valor, como "Autor", Título".</span><span class="sxs-lookup"><span data-stu-id="562b6-108">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="562b6-109">En este tema se describe el proceso de agregar información de metadatos al receptor de archivos para que aparezca en el objeto de [encabezado ASF final.](asf-file-structure.md)</span><span class="sxs-lookup"><span data-stu-id="562b6-109">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="562b6-110">Puede agregar información de metadatos al receptor de archivos ASF antes de compilar la topología de codificación.</span><span class="sxs-lookup"><span data-stu-id="562b6-110">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="562b6-111">El objeto ContentInfo de ASF para el receptor de archivos realiza un seguimiento de las propiedades de los metadatos y se exponen a la aplicación a través de la [**interfaz DESMETADATA.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)</span><span class="sxs-lookup"><span data-stu-id="562b6-111">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="562b6-112">Algunas de estas propiedades, como "IsVBR", que indica si el archivo contiene secuencias de velocidad de bits variable (VBR), las establece automáticamente el receptor de archivos analizando las propiedades de codificación de secuencias establecidas.</span><span class="sxs-lookup"><span data-stu-id="562b6-112">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="562b6-113">Para obtener una lista completa de las propiedades, consulte el tema "Lista de atributos" en la documentación del SDK de formato.</span><span class="sxs-lookup"><span data-stu-id="562b6-113">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="562b6-114">Uso de la interfaz IMFMetadata en el receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="562b6-114">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="562b6-115">Consulte el objeto de receptor de archivos ASF para obtener un puntero a su implementación de la interfaz [**IMFMetadataProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)</span><span class="sxs-lookup"><span data-stu-id="562b6-115">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="562b6-116">Llame [**a IMFMetadataProvider::GetMFMetadata para**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) obtener un puntero DE TIPO [**IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)</span><span class="sxs-lookup"><span data-stu-id="562b6-116">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="562b6-117">El *parámetro pPresentationDescriptor* se omite y la aplicación puede pasar **NULL.**</span><span class="sxs-lookup"><span data-stu-id="562b6-117">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="562b6-118">Si la aplicación pasa cero como identificador de flujo en el parámetro *dwStreamIdentifier,* el método recupera los metadatos que se aplican a todo el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="562b6-118">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="562b6-119">De lo contrario, solo se recuperan los metadatos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="562b6-119">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="562b6-120">Llame [**a IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para recuperar la lista de propiedades de codificación de archivos establecidas en el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="562b6-120">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="562b6-121">Llame [**a IMFMetadata::GetProperty para**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) obtener los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="562b6-121">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="562b6-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="562b6-122">Example</span></span>

<span data-ttu-id="562b6-123">En el código de ejemplo siguiente se muestra cómo enumerar los nombres de propiedad y los valores que se establecen en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="562b6-123">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="562b6-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="562b6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="562b6-125">Receptores multimedia de ASF</span><span class="sxs-lookup"><span data-stu-id="562b6-125">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="562b6-126">Componentes de ASF de capa de canalización</span><span class="sxs-lookup"><span data-stu-id="562b6-126">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="562b6-127">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="562b6-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



