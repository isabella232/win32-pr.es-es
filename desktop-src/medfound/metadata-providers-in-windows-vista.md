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
# <a name="metadata-providers-in-windows-vista"></a><span data-ttu-id="b29ef-103">Proveedores de metadatos en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b29ef-103">Metadata Providers in Windows Vista</span></span>

<span data-ttu-id="b29ef-104">En Windows Vista, Microsoft Media Foundation expone metadatos a través de la interfaz [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="b29ef-104">In Windows Vista, Microsoft Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="b29ef-105">Leer metadatos</span><span class="sxs-lookup"><span data-stu-id="b29ef-105">Reading Metadata</span></span>

<span data-ttu-id="b29ef-106">Para leer los metadatos de un origen multimedia, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b29ef-106">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="b29ef-107">Obtiene un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="b29ef-107">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="b29ef-108">Puede usar la interfaz [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obtener un puntero **IMFMediaSource** .</span><span class="sxs-lookup"><span data-stu-id="b29ef-108">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="b29ef-109">Llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obtener el descriptor de presentación del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="b29ef-109">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="b29ef-110">Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) en el origen de medios para obtener un puntero a la interfaz [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="b29ef-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span> <span data-ttu-id="b29ef-111">En el parámetro *guidService* de **MFGetService**, especifique el valor **de \_ \_ \_ servicio del proveedor de metadatos MF**.</span><span class="sxs-lookup"><span data-stu-id="b29ef-111">In the *guidService* parameter of **MFGetService**, specify the value **MF\_METADATA\_PROVIDER\_SERVICE**.</span></span> <span data-ttu-id="b29ef-112">Si el origen no admite la interfaz **IMFMetadataProvider** , **MFGetService** devuelve el **\_ servicio MF E \_ no compatible \_**.</span><span class="sxs-lookup"><span data-stu-id="b29ef-112">If the source does not support the **IMFMetadataProvider** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
4.  <span data-ttu-id="b29ef-113">Llame a [**IMFMetadataProvider:: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) y pase un puntero al descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="b29ef-113">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) and pass in a pointer to the presentation descriptor.</span></span> <span data-ttu-id="b29ef-114">Este método devuelve un puntero a la interfaz [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="b29ef-114">This method returns a pointer to the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>
    -   <span data-ttu-id="b29ef-115">Para obtener los metadatos de nivel de secuencia, llame primero a [**IMFStreamDescriptor:: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) para obtener el identificador de flujo.</span><span class="sxs-lookup"><span data-stu-id="b29ef-115">To get stream-level metadata first call [**IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) to get the stream identifier.</span></span> <span data-ttu-id="b29ef-116">Después, pase el identificador de flujo en el parámetro *dwStreamIdentifier* de [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span><span class="sxs-lookup"><span data-stu-id="b29ef-116">Then pass the stream identifier in the *dwStreamIdentifier* parameter of [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span></span>
    -   <span data-ttu-id="b29ef-117">Para obtener los metadatos en el nivel de presentación, establezca *dwStreamIdentifier* en cero.</span><span class="sxs-lookup"><span data-stu-id="b29ef-117">To get presentation-level metadata, set *dwStreamIdentifier* to zero.</span></span>
5.  <span data-ttu-id="b29ef-118">\[\]Llamada opcional [**IMFMetadata:: GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) para obtener una lista de los idiomas en los que los metadatos están disponibles.</span><span class="sxs-lookup"><span data-stu-id="b29ef-118">\[Optional\] Call [**IMFMetadata::GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) to get a list of the languages in which metadata is available.</span></span> <span data-ttu-id="b29ef-119">Los idiomas se identifican mediante etiquetas de idioma compatibles con RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="b29ef-119">Languages are identified using RFC 1766-compliant language tags.</span></span>
6.  <span data-ttu-id="b29ef-120">\[\]Llamada opcional [**IMFMetadata:: SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) para seleccionar el idioma.</span><span class="sxs-lookup"><span data-stu-id="b29ef-120">\[Optional\] Call [**IMFMetadata::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) to select the language.</span></span>
7.  <span data-ttu-id="b29ef-121">\[\]Llamada opcional [**IMFMetadata:: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para obtener una lista de los nombres de todas las propiedades de metadatos de esta secuencia o presentación.</span><span class="sxs-lookup"><span data-stu-id="b29ef-121">\[Optional\] Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to get a list of the names of all the metadata properties for this stream or presentation.</span></span>
8.  <span data-ttu-id="b29ef-122">Llame a [**IMFMetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) para obtener un valor de propiedad de metadatos específico, pasando el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b29ef-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get a specific metadata property value, passing in the name of the property.</span></span>

<span data-ttu-id="b29ef-123">En el código siguiente se muestran los pasos 2 a 4:</span><span class="sxs-lookup"><span data-stu-id="b29ef-123">The following code shows steps 2–4:</span></span>


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



<span data-ttu-id="b29ef-124">En el código siguiente se muestran los pasos 7 y 8.</span><span class="sxs-lookup"><span data-stu-id="b29ef-124">The following code shows steps 7–8.</span></span> <span data-ttu-id="b29ef-125">Supongamos que `DisplayProperty` es una función que muestra un valor de **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="b29ef-125">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b29ef-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b29ef-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b29ef-127">Metadatos de medios</span><span class="sxs-lookup"><span data-stu-id="b29ef-127">Media Metadata</span></span>](media-metadata.md)
</dt> <dt>

[<span data-ttu-id="b29ef-128">Proveedores de metadatos de Shell</span><span class="sxs-lookup"><span data-stu-id="b29ef-128">Shell Metadata Providers</span></span>](shell-metadata-providers.md)
</dt> </dl>

 

 



