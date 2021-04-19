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
# <a name="shell-metadata-providers"></a><span data-ttu-id="556d2-103">Proveedores de metadatos de Shell</span><span class="sxs-lookup"><span data-stu-id="556d2-103">Shell Metadata Providers</span></span>

<span data-ttu-id="556d2-104">A partir de Windows 7, Microsoft Media Foundation expone metadatos a través de la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="556d2-104">Starting in Windows 7, Microsoft Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span>

<span data-ttu-id="556d2-105">Los metadatos obtenidos mediante el proceso definido en este tema solo deben usarse para el acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="556d2-105">Metadata obtained using the process defined in this topic should only be used for read-only access.</span></span> <span data-ttu-id="556d2-106">No se admite la escritura de datos con este proceso.</span><span class="sxs-lookup"><span data-stu-id="556d2-106">Writing data using this process is not supported.</span></span> <span data-ttu-id="556d2-107">Puede crear un objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) con fines de escritura mediante un identificador de clase (CLSID) Obtenido de [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span><span class="sxs-lookup"><span data-stu-id="556d2-107">You can create an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object for writing purposes using a class identifier (CLSID) obtained from [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="556d2-108">Leer metadatos</span><span class="sxs-lookup"><span data-stu-id="556d2-108">Reading Metadata</span></span>

<span data-ttu-id="556d2-109">Para leer los metadatos de un origen multimedia, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="556d2-109">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="556d2-110">Obtiene un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="556d2-110">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="556d2-111">Puede usar la interfaz [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obtener un puntero **IMFMediaSource** .</span><span class="sxs-lookup"><span data-stu-id="556d2-111">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="556d2-112">Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) en el origen de medios para obtener un puntero a la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="556d2-112">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span> <span data-ttu-id="556d2-113">En el parámetro *guidService* de **MFGetService**, especifique el valor **del \_ \_ \_ servicio de controlador de propiedades MF**.</span><span class="sxs-lookup"><span data-stu-id="556d2-113">In the *guidService* parameter of **MFGetService**, specify the value **MF\_PROPERTY\_HANDLER\_SERVICE**.</span></span> <span data-ttu-id="556d2-114">Si el origen no admite la interfaz **IPropertyStore** , **MFGetService** devuelve el **\_ servicio MF E \_ no compatible \_**.</span><span class="sxs-lookup"><span data-stu-id="556d2-114">If the source does not support the **IPropertyStore** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
3.  <span data-ttu-id="556d2-115">Llame a los métodos de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para enumerar las propiedades de metadatos.</span><span class="sxs-lookup"><span data-stu-id="556d2-115">Call [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods to enumerate the metadata properties.</span></span>

<span data-ttu-id="556d2-116">En el código siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="556d2-116">The following code shows these steps.</span></span> <span data-ttu-id="556d2-117">Supongamos que `DisplayProperty` es una función que muestra un valor de **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="556d2-117">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


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



<span data-ttu-id="556d2-118">Para obtener una lista de las claves de propiedad de metadatos, consulte [propiedades de metadatos para archivos multimedia](metadata-properties-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="556d2-118">For a list of metadata property keys, see [Metadata Properties for Media Files](metadata-properties-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="556d2-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="556d2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="556d2-120">Metadatos de medios</span><span class="sxs-lookup"><span data-stu-id="556d2-120">Media Metadata</span></span>](media-metadata.md)
</dt> </dl>

 

 
