---
description: Configuración de un origen de medios
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configuración de un origen de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea741e3c04282af445fbea7be07854bf517ec44f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105649327"
---
# <a name="configuring-a-media-source"></a><span data-ttu-id="a8133-103">Configuración de un origen de medios</span><span class="sxs-lookup"><span data-stu-id="a8133-103">Configuring a Media Source</span></span>

<span data-ttu-id="a8133-104">Al usar el [solucionador de origen](source-resolver.md) para crear un origen de medios, puede especificar un almacén de propiedades que contenga propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="a8133-104">When you use the [Source Resolver](source-resolver.md) to create a media source, you can specify a property store that contains configuration properties.</span></span> <span data-ttu-id="a8133-105">Estas propiedades se usarán para inicializar el origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="a8133-105">These properties will be used to initialize the media source.</span></span> <span data-ttu-id="a8133-106">El conjunto de propiedades admitidas depende de la implementación del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="a8133-106">The set of supported properties depends on the implementation of the media source.</span></span> <span data-ttu-id="a8133-107">No todos los orígenes de medios definen propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="a8133-107">Not every media source defines configuration properties.</span></span>

<span data-ttu-id="a8133-108">En la tabla siguiente se enumeran las propiedades de configuración de los orígenes multimedia que se proporcionan en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a8133-108">The following table lists the configuration properties for the media sources that are provided in Media Foundation.</span></span> <span data-ttu-id="a8133-109">Los orígenes de medios de terceros pueden definir sus propias propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="a8133-109">Third-party media sources can define their own custom properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8133-110">Origen de medios</span><span class="sxs-lookup"><span data-stu-id="a8133-110">Media source</span></span></th>
<th><span data-ttu-id="a8133-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8133-111">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8133-112">Origen de red</span><span class="sxs-lookup"><span data-stu-id="a8133-112">Network source</span></span></td>
<td><span data-ttu-id="a8133-113">Consulte <a href="network-source-features.md">características de origen de red</a>.</span><span class="sxs-lookup"><span data-stu-id="a8133-113">See <a href="network-source-features.md">Network Source Features</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8133-114">Origen de medios ASF</span><span class="sxs-lookup"><span data-stu-id="a8133-114">ASF media source</span></span></td>
<td><ul>
<li><span data-ttu-id="a8133-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8133-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span></span></li>
<li><span data-ttu-id="a8133-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span><span class="sxs-lookup"><span data-stu-id="a8133-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span></span></li>
<li><span data-ttu-id="a8133-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span><span class="sxs-lookup"><span data-stu-id="a8133-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span></span></li>
<li><span data-ttu-id="a8133-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span><span class="sxs-lookup"><span data-stu-id="a8133-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a8133-119">Para configurar un origen, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a8133-119">To configure a source, perform the following steps.</span></span>

1.  <span data-ttu-id="a8133-120">Llame a **PSCreateMemoryPropertyStore** para crear un nuevo almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a8133-120">Call **PSCreateMemoryPropertyStore** to create a new property store.</span></span> <span data-ttu-id="a8133-121">Esta función devuelve un puntero **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="a8133-121">This function returns an **IPropertyStore** pointer.</span></span>
2.  <span data-ttu-id="a8133-122">Llame a **IPropertyStore:: SetValue** para establecer una o varias propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="a8133-122">Call **IPropertyStore::SetValue** to set one or more configuration properties.</span></span>
3.  <span data-ttu-id="a8133-123">Llame a una de las funciones de creación del solucionador de origen, como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), y pase el puntero **IPropertyStore** en el parámetro *pProps* .</span><span class="sxs-lookup"><span data-stu-id="a8133-123">Call one of the source resolver's creation functions, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), and pass the **IPropertyStore** pointer in the *pProps* parameter.</span></span>


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



<span data-ttu-id="a8133-124">La resolución de origen pasa el puntero **IPropertyStore** directamente al controlador de esquema o al controlador de flujo de bytes que crea el origen.</span><span class="sxs-lookup"><span data-stu-id="a8133-124">The source resolver passes the **IPropertyStore** pointer directly to the scheme handler or byte-stream handler that creates the source.</span></span> <span data-ttu-id="a8133-125">La resolución de origen no realiza ningún intento de validar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="a8133-125">The source resolver makes no attempt to validate the properties.</span></span>

<span data-ttu-id="a8133-126">Por lo general, estas propiedades se usan para la configuración avanzada.</span><span class="sxs-lookup"><span data-stu-id="a8133-126">Generally, these properties are used for advanced settings.</span></span> <span data-ttu-id="a8133-127">Si no proporciona un almacén de propiedades, el origen multimedia seguirá funcionando correctamente con la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a8133-127">If you don't provide a property store, the media source should still function correctly with default settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8133-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8133-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8133-129">Solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="a8133-129">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



