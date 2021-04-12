---
description: En este tema se presentan los requisitos para crear controladores de metadatos personalizados para el componente de creación de imágenes de Windows (WIC), incluidos los escritores y lectores de metadatos.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Información general sobre la extensibilidad de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277625"
---
# <a name="metadata-extensibility-overview"></a><span data-ttu-id="3f177-103">Información general sobre la extensibilidad de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-103">Metadata Extensibility Overview</span></span>

<span data-ttu-id="3f177-104">En este tema se presentan los requisitos para crear controladores de metadatos personalizados para el componente de creación de imágenes de Windows (WIC), incluidos los escritores y lectores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-104">This topic introduces the requirements for creating custom metadata handlers for the Windows Imaging Component (WIC), including both metadata readers and writers.</span></span> <span data-ttu-id="3f177-105">También se describen los requisitos para extender la detección de componentes en tiempo de ejecución de WIC para incluir los controladores de metadatos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3f177-105">It also discusses the requirements for extending WIC run-time component discovery to include your custom metadata handlers.</span></span>

<span data-ttu-id="3f177-106">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="3f177-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3f177-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3f177-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="3f177-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="3f177-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="3f177-109">Crear un lector de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-109">Creating a Metadata Reader</span></span>](#creating-a-metadata-reader)
    -   [<span data-ttu-id="3f177-110">Interfaz IWICMetadataReader</span><span class="sxs-lookup"><span data-stu-id="3f177-110">IWICMetadataReader Interface</span></span>](#iwicmetadatareader-interface)
    -   [<span data-ttu-id="3f177-111">Interfaz IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="3f177-111">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="3f177-112">Interfaz IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="3f177-112">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="3f177-113">Creación de un escritor de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-113">Creating a Metadata Writer</span></span>](#creating-a-metadata-writer)
    -   [<span data-ttu-id="3f177-114">Interfaz IWICMetadataWriter</span><span class="sxs-lookup"><span data-stu-id="3f177-114">IWICMetadataWriter Interface</span></span>](#iwicmetadatawriter-interface)
    -   [<span data-ttu-id="3f177-115">Interfaz IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="3f177-115">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="3f177-116">Interfaz IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="3f177-116">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="3f177-117">Instalación y registro de un controlador de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-117">Installing and Registering a Metadata Handler</span></span>](#installing-and-registering-a-metadata-handler)
    -   [<span data-ttu-id="3f177-118">Claves del registro del controlador de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-118">Metadata Handler Registry Keys</span></span>](#metadata-handler-registry-keys)
    -   [<span data-ttu-id="3f177-119">Lectores de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-119">Metadata Readers</span></span>](#metadata-readers)
    -   [<span data-ttu-id="3f177-120">Escritores de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-120">Metadata Writers</span></span>](#metadata-writers)
    -   [<span data-ttu-id="3f177-121">Firmar un controlador de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-121">Signing a Metadata Handler</span></span>](#signing-a-metadata-handler)
-   [<span data-ttu-id="3f177-122">Consideraciones especiales</span><span class="sxs-lookup"><span data-stu-id="3f177-122">Special Considerations</span></span>](#special-considerations)
    -   [<span data-ttu-id="3f177-123">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="3f177-123">PROPVARIANTS</span></span>](#propvariants)
    -   [<span data-ttu-id="3f177-124">Controladores 8BIM</span><span class="sxs-lookup"><span data-stu-id="3f177-124">8BIM Handlers</span></span>](#8bim-handlers)
-   [<span data-ttu-id="3f177-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f177-125">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="3f177-126">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3f177-126">Prerequisites</span></span>

<span data-ttu-id="3f177-127">Para entender este tema, debe tener un conocimiento exhaustivo de WIC, sus componentes y metadatos para las imágenes.</span><span class="sxs-lookup"><span data-stu-id="3f177-127">To understand this topic you should have an in-depth understanding of WIC, its components, and metadata for images.</span></span> <span data-ttu-id="3f177-128">Para obtener más información sobre los metadatos de WIC, consulte [información general sobre metadatos de WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="3f177-128">For more information on WIC metadata, see the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="3f177-129">Para obtener más información sobre los componentes de WIC, consulte [información general sobre el componente de creación de imágenes de Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="3f177-129">For more information on WIC components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="3f177-130">Introducción</span><span class="sxs-lookup"><span data-stu-id="3f177-130">Introduction</span></span>

<span data-ttu-id="3f177-131">Como se describe en [información general sobre los metadatos de WIC](-wic-about-metadata.md), a menudo hay varios bloques de metadatos en una imagen, cada uno de los cuales expone diferentes tipos de información en diferentes formatos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-131">As discussed in the [WIC Metadata Overview](-wic-about-metadata.md), there are often multiple blocks of metadata within an image, each exposing different types of information in different metadata formats.</span></span> <span data-ttu-id="3f177-132">Para interactuar con un formato de metadatos insertado en una imagen, una aplicación debe usar un controlador de metadatos adecuado.</span><span class="sxs-lookup"><span data-stu-id="3f177-132">To interact with a metadata format embedded within an image, an application must use an appropriate metadata handler.</span></span> <span data-ttu-id="3f177-133">WIC proporciona varios controladores de metadatos (tanto lectores de metadatos como escritores) que le permiten leer y escribir tipos específicos de metadatos como Exif o XMP.</span><span class="sxs-lookup"><span data-stu-id="3f177-133">WIC provides several metadata handlers (both metadata readers and writers) that enable you to read and write specific types of metadata such as Exif or XMP.</span></span>

<span data-ttu-id="3f177-134">Además de los controladores nativos proporcionados, WIC proporciona API que permiten crear nuevos controladores de metadatos que participan en la detección de componentes en tiempo de ejecución de WIC.</span><span class="sxs-lookup"><span data-stu-id="3f177-134">In addition to the native handlers provided, WIC provides APIs that enable you to create new metadata handlers that participate in WIC's run-time component discovery.</span></span> <span data-ttu-id="3f177-135">Esto permite que las aplicaciones que usan WIC lean y escriban los formatos de metadatos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3f177-135">This enables applications that use WIC to read and write your custom metadata formats.</span></span>

<span data-ttu-id="3f177-136">Los pasos siguientes permiten a los controladores de metadatos participar en la detección de metadatos en tiempo de ejecución de WIC.</span><span class="sxs-lookup"><span data-stu-id="3f177-136">The following steps enable your metadata handlers to participate in WIC's run-time metadata discovery.</span></span>

-   <span data-ttu-id="3f177-137">Implemente una clase de controlador de lector de metadatos ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) que exponga las interfaces WIC necesarias para leer el formato de metadatos personalizado.</span><span class="sxs-lookup"><span data-stu-id="3f177-137">Implement a metadata-reader handler class ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) that exposes the required WIC interfaces for reading your custom metadata format.</span></span> <span data-ttu-id="3f177-138">Esto permite a las aplicaciones basadas en WIC leer el formato de los metadatos de la misma manera que leen los formatos de metadatos nativos.</span><span class="sxs-lookup"><span data-stu-id="3f177-138">This enables WIC-based applications to read your metadata format the same way they read native metadata formats.</span></span>
-   <span data-ttu-id="3f177-139">Implemente una clase de controlador de escritor de metadatos ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) que exponga las interfaces WIC necesarias para codificar el formato de metadatos personalizado.</span><span class="sxs-lookup"><span data-stu-id="3f177-139">Implement a metadata-writer handler class ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) that exposes the required WIC interfaces for encoding your custom metadata format.</span></span> <span data-ttu-id="3f177-140">Esto permite a las aplicaciones basadas en WIC serializar el formato de los metadatos en formatos de imagen compatibles.</span><span class="sxs-lookup"><span data-stu-id="3f177-140">This enables WIC-based applications to serialize your metadata format into supported image formats.</span></span>
-   <span data-ttu-id="3f177-141">Firmar y registrar digitalmente los controladores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-141">Digitally sign and register your metadata handlers.</span></span> <span data-ttu-id="3f177-142">Esto permite detectar los controladores de metadatos en tiempo de ejecución haciendo coincidir el patrón de identificación del registro con el patrón incrustado en el archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="3f177-142">This enables your metadata handlers to be discovered at run time by matching the identifying pattern in the registry with the pattern embedded in the image file.</span></span>

## <a name="creating-a-metadata-reader"></a><span data-ttu-id="3f177-143">Crear un lector de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-143">Creating a Metadata Reader</span></span>

<span data-ttu-id="3f177-144">El acceso principal a los bloques de metadatos dentro de un códec se realiza a través de la interfaz [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) que implementa cada códec WIC.</span><span class="sxs-lookup"><span data-stu-id="3f177-144">The main access to metadata blocks within a codec is through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface that each WIC codec implements.</span></span> <span data-ttu-id="3f177-145">Esta interfaz enumera cada uno de los bloques de metadatos incrustados en un formato de imagen para que se puedan detectar y crear instancias del controlador de metadatos adecuado para cada bloque.</span><span class="sxs-lookup"><span data-stu-id="3f177-145">This interface enumerates each of the metadata blocks embedded in an image format so that the appropriate metadata handler can be discovered and instantiated for each block.</span></span> <span data-ttu-id="3f177-146">Los bloques de metadatos que no reconoce WIC se consideran desconocidos y se definen como GUID CLSID \_ WICUnknownMetadataReader.</span><span class="sxs-lookup"><span data-stu-id="3f177-146">The metadata blocks that are not recognized by WIC are considered unknown and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="3f177-147">Para que WIC reconozca el formato de los metadatos, debe crear una clase que implemente tres interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)y [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="3f177-147">To have your metadata format recognized by WIC, you must create a class that implements three interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="3f177-148">Si el formato de los metadatos tiene restricciones que presentan inadecuadamente algunos métodos de las interfaces necesarias, estos métodos deben devolver WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="3f177-148">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatareader-interface"></a><span data-ttu-id="3f177-149">Interfaz IWICMetadataReader</span><span class="sxs-lookup"><span data-stu-id="3f177-149">IWICMetadataReader Interface</span></span>

<span data-ttu-id="3f177-150">La interfaz [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) debe implementarse al crear un lector de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-150">The [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) interface must be implemented when creating a metadata reader.</span></span> <span data-ttu-id="3f177-151">Esta interfaz proporciona acceso a los elementos de metadatos subordinado en el flujo de datos de un formato de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-151">This interface provides access to the underling metadata items within the data stream of a metadata format.</span></span>

<span data-ttu-id="3f177-152">En el código siguiente se muestra la definición de la interfaz del lector de metadatos tal y como se define en el archivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="3f177-152">The following code shows the definition of the metadata reader interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

<span data-ttu-id="3f177-153">El método **GetMetadataFormat** devuelve el GUID del formato de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-153">The **GetMetadataFormat** method returns the GUID of your metadata format.</span></span>

<span data-ttu-id="3f177-154">El método **GetMetadataHandlerInfo** devuelve una interfaz [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) que proporciona información sobre el controlador de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-154">The **GetMetadataHandlerInfo** method returns an [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) interface that provides information about your metadata handler.</span></span> <span data-ttu-id="3f177-155">Esto incluye información como qué formatos de imagen admiten el formato de metadatos y si el lector de metadatos requiere acceso a la secuencia de metadatos completa.</span><span class="sxs-lookup"><span data-stu-id="3f177-155">This includes information such as what image formats support the metadata format and whether your metadata reader requires access to the full metadata stream.</span></span>

<span data-ttu-id="3f177-156">El método **getCount** devuelve el número de elementos de metadatos individuales (incluidos los bloques de metadatos incrustados) que se encuentran en la secuencia de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-156">The **GetCount** method returns the number of individual metadata items (including embedded metadata blocks) found within the metadata stream.</span></span>

<span data-ttu-id="3f177-157">El método **GetValueByIndex** devuelve un elemento de metadatos mediante un valor de índice.</span><span class="sxs-lookup"><span data-stu-id="3f177-157">The **GetValueByIndex** method returns a metadata item by an index value.</span></span> <span data-ttu-id="3f177-158">Este método permite a las aplicaciones recorrer cada elemento de metadatos en un bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-158">This method enables applications to loop through each metadata item in a metadata block.</span></span> <span data-ttu-id="3f177-159">En el código siguiente se muestra cómo una aplicación puede utilizar este método para recuperar cada elemento de metadatos en un bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-159">The following code demonstrates how an application can use this method to retrieve each metadata item in a metadata block.</span></span>


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



<span data-ttu-id="3f177-160">El método **GetValue** recupera un elemento de metadatos específico por esquema o identificador.</span><span class="sxs-lookup"><span data-stu-id="3f177-160">The **GetValue** method retrieves a specific metadata item by schema and/or ID.</span></span> <span data-ttu-id="3f177-161">Este método es similar al método **GetValueByIndex** , salvo que recupera un elemento de metadatos que tiene un esquema o un identificador específicos.</span><span class="sxs-lookup"><span data-stu-id="3f177-161">This method is similar to the **GetValueByIndex** method except that it retrieves a metadata item that has a specific schema or ID.</span></span>

<span data-ttu-id="3f177-162">El método **GetEnumerator** devuelve un enumerador de cada elemento de metadatos en el bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-162">The **GetEnumerator** method returns an enumerator of each metadata item in the metadata block.</span></span> <span data-ttu-id="3f177-163">Esto permite a las aplicaciones usar un enumerador para navegar por el formato de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-163">This enables applications to use an enumerator to navigate your metadata format.</span></span>

<span data-ttu-id="3f177-164">Si el formato de los metadatos no tiene un concepto de esquemas para los elementos de metadatos, el elemento GetValue... los métodos deben omitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3f177-164">If your metadata format does not have a notion of schemas for metadata items, the GetValue... methods should ignore this property.</span></span> <span data-ttu-id="3f177-165">Sin embargo, si el formato admite nombres de esquema, debe prever un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="3f177-165">If, however, your format supports schema naming, you should anticipate a **NULL** value.</span></span>

<span data-ttu-id="3f177-166">Si un elemento de metadatos es un bloque de metadatos incrustado, cree un controlador de metadatos a partir del subflujo del contenido incrustado y devuelva el nuevo controlador de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-166">If a metadata item is an embedded metadata block, create a metadata handler from the substream of the embedded content and return the new metadata handler.</span></span> <span data-ttu-id="3f177-167">Si no hay ningún lector de metadatos disponible para el bloque anidado, cree una instancia y devuelva un lector de metadatos desconocido.</span><span class="sxs-lookup"><span data-stu-id="3f177-167">If there is no metadata reader available for the nested block, instantiate and return an unknown metadata reader.</span></span> <span data-ttu-id="3f177-168">Para crear un nuevo lector de metadatos para el bloque incrustado, llame a los métodos **CreateMetadataReaderFromContainer** o **CreateMetadataReader** del generador de componentes, o llame a la función [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) .</span><span class="sxs-lookup"><span data-stu-id="3f177-168">To create a new metadata reader for the embedded block, call the component factory's **CreateMetadataReaderFromContainer** or **CreateMetadataReader** methods, or call the [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) function.</span></span>

<span data-ttu-id="3f177-169">Si el flujo de metadatos contiene contenido big-endian, el lector de metadatos es responsable de intercambiar los valores de datos que procesa.</span><span class="sxs-lookup"><span data-stu-id="3f177-169">If the metadata stream contains big-endian content, the metadata reader is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="3f177-170">También es responsable de informar a los lectores de metadatos anidados que están trabajando con el flujo de datos Big-Endian.</span><span class="sxs-lookup"><span data-stu-id="3f177-170">It is also responsible for informing any nested metadata readers that they are working with big-endian data stream.</span></span> <span data-ttu-id="3f177-171">Sin embargo, todos los valores se deben devolver en formato Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="3f177-171">However, all values should be returned in little-endian format.</span></span>

<span data-ttu-id="3f177-172">Implementar la compatibilidad con la navegación por espacios de nombres al admitir consultas en las que el identificador del elemento de metadatos es un `VT_CLSID` (GUID) que corresponde a un formato de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-172">Implement support for namespace navigation by supporting queries where the metadata item ID is a `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="3f177-173">Si se identifica un lector de metadatos anidado para ese formato durante el análisis, se debe devolver.</span><span class="sxs-lookup"><span data-stu-id="3f177-173">If a nested metadata reader for that format is identified during parsing, it must be returned.</span></span> <span data-ttu-id="3f177-174">Esto permite a las aplicaciones usar un lector de consultas de metadatos para buscar en el formato de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-174">This enables applications to use a metadata query reader to search your metadata format.</span></span>

<span data-ttu-id="3f177-175">Al obtener un elemento de metadatos por identificador, debe usar la [función PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) para convertir el identificador en el tipo esperado.</span><span class="sxs-lookup"><span data-stu-id="3f177-175">When getting a metadata item by ID, you should use [PropVariantChangeType Function](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) to coerce the ID into the expected type.</span></span> <span data-ttu-id="3f177-176">Por ejemplo, el lector de IFD convertirá un identificador en un tipo `VT_UI2` para que coincida con el tipo de datos de un identificador de etiqueta de IFD USHORT.</span><span class="sxs-lookup"><span data-stu-id="3f177-176">For example, the IFD reader will coerce an ID to type `VT_UI2` to coincide with the data type of an IFD tag ID USHORT.</span></span> <span data-ttu-id="3f177-177">Para ello, el tipo de entrada y el tipo esperado deben ser [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="3f177-177">The input type and expected type must both be [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to do this.</span></span> <span data-ttu-id="3f177-178">Esto no es necesario, pero al realizar esta coerción se simplifica el código que llama al lector para consultar los elementos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-178">This is not required, but doing this coercion simplifies code that calls the reader to query for metadata items.</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="3f177-179">Interfaz IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="3f177-179">IWICPersistStream Interface</span></span>

<span data-ttu-id="3f177-180">La interfaz [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hereda de **IPersistStream** y proporciona métodos adicionales para guardar y cargar objetos mediante la enumeración [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="3f177-180">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="3f177-181">En el código siguiente se muestra la definición de la interfaz [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) tal como se define en el archivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="3f177-181">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="3f177-182">El método **LoadEx** proporciona el lector de metadatos con un flujo de datos que contiene el bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-182">The **LoadEx** method provides your metadata reader with a data stream containing your metadata block.</span></span> <span data-ttu-id="3f177-183">El lector analiza este flujo para tener acceso a los elementos de metadatos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="3f177-183">Your reader parses this stream to access the underlying metadata items.</span></span> <span data-ttu-id="3f177-184">El lector de metadatos se inicializa con un subflujo que se coloca al principio del contenido de metadatos sin formato.</span><span class="sxs-lookup"><span data-stu-id="3f177-184">Your metadata reader is initialized with a substream that is positioned at the beginning of the raw metadata content.</span></span> <span data-ttu-id="3f177-185">Si el lector no requiere el flujo completo, el subflujo está limitado en el intervalo solo al contenido del bloque de metadatos; de lo contrario, se proporciona la secuencia de metadatos completa con la posición establecida al principio del bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-185">If your reader does not require the full stream, the substream is limited in range to only the content of the metadata block; otherwise, the full metadata stream is provided with the position set at the beginning of your metadata block.</span></span>

<span data-ttu-id="3f177-186">Los escritores de metadatos usan el método **SaveEx** para serializar el bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-186">The **SaveEx** method is used by metadata writers to serialize your metadata block.</span></span> <span data-ttu-id="3f177-187">Cuando se usa **SaveEx** en un lector de metadatos, debe devolver WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="3f177-187">When **SaveEx** is used in a metadata reader, it should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="3f177-188">Interfaz IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="3f177-188">IWICStreamProvider Interface</span></span>

<span data-ttu-id="3f177-189">La interfaz [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) permite que el lector de metadatos proporcione referencias a su flujo de contenido, proporcione información sobre la secuencia y actualice las versiones en caché de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3f177-189">The [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface enables your metadata reader to provide references to its content stream, provide information about the stream, and refresh cached versions of the stream.</span></span>

<span data-ttu-id="3f177-190">En el código siguiente se muestra la definición de la interfaz [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) tal como se define en el archivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="3f177-190">The following code shows the definition of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

<span data-ttu-id="3f177-191">El método **GetStream** recupera una referencia a la secuencia de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-191">The **GetStream** method retrieves a reference to your metadata stream.</span></span> <span data-ttu-id="3f177-192">La secuencia que devuelva debe tener el puntero de secuencia restablecido a la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="3f177-192">The stream you return should have the stream pointer reset to the start position.</span></span> <span data-ttu-id="3f177-193">Si el formato de los metadatos requiere acceso completo a secuencias, la posición inicial debe ser el inicio del bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-193">If your metadata format requires full stream access, the start position should be the start of your metadata block.</span></span>

<span data-ttu-id="3f177-194">El método **GetPersistOptions** devuelve las opciones actuales de la secuencia de la enumeración [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="3f177-194">The **GetPersistOptions** method returns the stream's current options from the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="3f177-195">El método **GetPreferredVendorGUID** devuelve el GUID del proveedor del lector de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-195">The **GetPreferredVendorGUID** method returns the GUID of the vendor of the metadata reader.</span></span>

<span data-ttu-id="3f177-196">El método **RefreshStream** actualiza la secuencia de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-196">The **RefreshStream** method refreshes the metadata stream.</span></span> <span data-ttu-id="3f177-197">Este método debe llamar a **LoadEx** con una secuencia **null** para los bloques de metadatos anidados.</span><span class="sxs-lookup"><span data-stu-id="3f177-197">This method must call **LoadEx** with a **NULL** stream for any nested metadata blocks.</span></span> <span data-ttu-id="3f177-198">Esto es necesario porque los bloques de metadatos anidados y sus elementos pueden dejar de existir, debido a la edición en contexto.</span><span class="sxs-lookup"><span data-stu-id="3f177-198">This is necessary because nested metadata blocks and their items may no longer exist, due to in-place editing.</span></span>

## <a name="creating-a-metadata-writer"></a><span data-ttu-id="3f177-199">Creación de un escritor de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-199">Creating a Metadata Writer</span></span>

<span data-ttu-id="3f177-200">Un escritor de metadatos es un tipo de controlador de metadatos que proporciona una manera de serializar un bloque de metadatos en un marco de imagen o fuera de un fotograma individual si el formato de imagen lo admite.</span><span class="sxs-lookup"><span data-stu-id="3f177-200">A metadata writer is a type of metadata handler that provides a way to serialize a metadata block to an image frame, or outside an individual frame if the image format supports it.</span></span> <span data-ttu-id="3f177-201">El acceso principal a los escritores de metadatos dentro de un códec es a través de la interfaz [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) que implementa cada codificador WIC.</span><span class="sxs-lookup"><span data-stu-id="3f177-201">The main access to the metadata writers within a codec is through the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface that each WIC encoder implements.</span></span> <span data-ttu-id="3f177-202">Esta interfaz permite a las aplicaciones enumerar cada uno de los bloques de metadatos insertados en una imagen para que se pueda detectar y crear una instancia del escritor de metadatos adecuado para cada bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-202">This interface enables applications to enumerate each of the metadata blocks embedded in an image so that the appropriate metadata writer can be discovered and instantiated for each metadata block.</span></span> <span data-ttu-id="3f177-203">Los bloques de metadatos que no tienen un escritor de metadatos correspondiente se consideran desconocidos y se definen como GUID CLSID \_ WICUnknownMetadataReader.</span><span class="sxs-lookup"><span data-stu-id="3f177-203">Metadata blocks that do not have a corresponding metadata writer are considered unknown, and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="3f177-204">Para habilitar las aplicaciones habilitadas para WIC para serializar y escribir el formato de metadatos, debe crear una clase que implemente las interfaces siguientes: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)y [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="3f177-204">To enable WIC enabled applications to serialize and write your metadata format, you must create a class that implements the following interfaces: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="3f177-205">Si el formato de los metadatos tiene restricciones que presentan inadecuadamente algunos métodos de las interfaces necesarias, estos métodos deben devolver WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="3f177-205">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatawriter-interface"></a><span data-ttu-id="3f177-206">Interfaz IWICMetadataWriter</span><span class="sxs-lookup"><span data-stu-id="3f177-206">IWICMetadataWriter Interface</span></span>

<span data-ttu-id="3f177-207">El escritor de metadatos debe implementar la interfaz [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) .</span><span class="sxs-lookup"><span data-stu-id="3f177-207">The [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) interface must be implemented by your metadata writer.</span></span> <span data-ttu-id="3f177-208">Además, dado que **IWICMetadataWriter** hereda de [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), también debe implementar todos los métodos de **IWICMetadataReader**.</span><span class="sxs-lookup"><span data-stu-id="3f177-208">Additionally, because **IWICMetadataWriter** inherits from [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), you must also implement all the methods of **IWICMetadataReader**.</span></span> <span data-ttu-id="3f177-209">Dado que ambos tipos de controlador requieren la misma herencia de interfaz, puede que desee crear una única clase que proporcione la funcionalidad de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3f177-209">Because both handler types require the same interface inheritance, you might want to create a single class that provides both reading and writing functionality.</span></span>

<span data-ttu-id="3f177-210">En el código siguiente se muestra la definición de la interfaz del escritor de metadatos tal y como se define en el archivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="3f177-210">The following code shows the definition of the metadata writer interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

<span data-ttu-id="3f177-211">El método **SetValue** escribe el elemento de metadatos especificado en la secuencia de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-211">The **SetValue** method writes the specified metadata item to the metadata stream.</span></span>

<span data-ttu-id="3f177-212">El método **SetValueByIndex** escribe el elemento de metadatos especificado en el índice especificado en la secuencia de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-212">The **SetValueByIndex** method writes the specified metadata item to the specified index in the metadata stream.</span></span> <span data-ttu-id="3f177-213">El índice no hace referencia al identificador, sino a la posición del elemento en el bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-213">The index does not refer to the ID but to the position of the item within the metadata block.</span></span>

<span data-ttu-id="3f177-214">El método **RemoveValue** quita el elemento de metadatos especificado de la secuencia de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-214">The **RemoveValue** method removes the specified metadata item from the metadata stream.</span></span>

<span data-ttu-id="3f177-215">El método **RemoveValueByIndex** quita el elemento de metadatos en el índice especificado de la secuencia de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-215">The **RemoveValueByIndex** method removes the metadata item at the specified index from the metadata stream.</span></span> <span data-ttu-id="3f177-216">Después de quitar un elemento, se espera que los elementos de metadatos restantes ocupen el índice anulado si el índice no es el último índice.</span><span class="sxs-lookup"><span data-stu-id="3f177-216">After removing an item, it is expected that the remaining metadata items will occupy the vacated index if the index is not the last index.</span></span> <span data-ttu-id="3f177-217">También se espera que el recuento cambie después de quitar el elemento.</span><span class="sxs-lookup"><span data-stu-id="3f177-217">It is also expected that the count will change after the item is removed.</span></span>

<span data-ttu-id="3f177-218">Es responsabilidad del escritor de metadatos convertir los elementos [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) en la estructura subyacente requerida por el formato.</span><span class="sxs-lookup"><span data-stu-id="3f177-218">It is the metadata writer's responsibility to convert the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) items to the underlying structure required by your format.</span></span> <span data-ttu-id="3f177-219">Sin embargo, a diferencia del lector de metadatos, los tipos de variante no se deben forzar normalmente a tipos diferentes, ya que el llamador está indicando específicamente qué tipo de datos se va a usar.</span><span class="sxs-lookup"><span data-stu-id="3f177-219">However, unlike the metadata reader, VARIANT types should not normally be coerced to different types as the caller is specifically indicating what data type to use.</span></span>

<span data-ttu-id="3f177-220">El escritor de metadatos debe confirmar todos los elementos de metadatos en el flujo de imagen, incluidos los valores ocultos o no reconocidos.</span><span class="sxs-lookup"><span data-stu-id="3f177-220">Your metadata writer must commit all metadata items to the image stream, including hidden or unrecognized values.</span></span> <span data-ttu-id="3f177-221">Esto incluye bloques de metadatos anidados desconocidos.</span><span class="sxs-lookup"><span data-stu-id="3f177-221">This includes unknown nested metadata blocks.</span></span> <span data-ttu-id="3f177-222">Sin embargo, es responsabilidad del codificador establecer los elementos de metadatos críticos antes de iniciar la operación de guardar.</span><span class="sxs-lookup"><span data-stu-id="3f177-222">However, it is the encoder's responsibility to set any critical metadata items prior to initiating the save operation.</span></span>

<span data-ttu-id="3f177-223">Si la secuencia de metadatos contiene contenido big-endian, el escritor de metadatos es responsable de intercambiar los valores de datos que procesa.</span><span class="sxs-lookup"><span data-stu-id="3f177-223">If the metadata stream contains big-endian content, the metadata writer is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="3f177-224">También es responsable de informar a los escritores de metadatos anidados que están trabajando con un flujo de datos Big-Endian cuando se guardan.</span><span class="sxs-lookup"><span data-stu-id="3f177-224">It is also responsible for informing any nested metadata writers that they are working with a big-endian data stream when they save.</span></span>

<span data-ttu-id="3f177-225">Implemente la compatibilidad con la creación y eliminación de espacios de nombres al admitir operaciones Set y Remove en elementos de metadatos con un tipo de `VT_CLSID` (un GUID) que se corresponda con un formato de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-225">Implement support for namespace creation and removal by supporting set and remove operations on metadata items with a type of `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="3f177-226">El escritor de metadatos llama a la función [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para insertar correctamente el contenido del escritor de metadatos anidados en el escritor de metadatos primario.</span><span class="sxs-lookup"><span data-stu-id="3f177-226">The metadata writer calls the [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) function to properly embed the nested metadata writer content into the parent metadata writer.</span></span>

<span data-ttu-id="3f177-227">Si el formato de los metadatos admite la codificación en contexto, es responsable de administrar el relleno necesario.</span><span class="sxs-lookup"><span data-stu-id="3f177-227">If your metadata format supports in-place encoding, you are responsible for managing the required padding.</span></span> <span data-ttu-id="3f177-228">Para obtener más información sobre la codificación en contexto, consulte [información general sobre metadatos de WIC](-wic-about-metadata.md) e [información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="3f177-228">For more information on in-place encoding, see [WIC Metadata Overview](-wic-about-metadata.md) and [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="3f177-229">Interfaz IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="3f177-229">IWICPersistStream Interface</span></span>

<span data-ttu-id="3f177-230">La interfaz [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) hereda de **IPersistStream** y proporciona métodos adicionales para guardar y cargar objetos mediante la enumeración [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="3f177-230">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="3f177-231">En el código siguiente se muestra la definición de la interfaz [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) tal como se define en el archivo wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="3f177-231">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="3f177-232">El método **LoadEx** proporciona el controlador de metadatos con un flujo de datos que contiene el bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-232">The **LoadEx** method provides your metadata handler with a data stream containing your metadata block.</span></span>

<span data-ttu-id="3f177-233">El método **SaveEx** serializa los metadatos en un flujo.</span><span class="sxs-lookup"><span data-stu-id="3f177-233">The **SaveEx** method serializes the metadata into a stream.</span></span> <span data-ttu-id="3f177-234">Si el flujo proporcionado es el mismo que el de la secuencia de inicialización, debe realizar la codificación en contexto.</span><span class="sxs-lookup"><span data-stu-id="3f177-234">If the provided stream is the same as initialization stream, you should perform in-place encoding.</span></span> <span data-ttu-id="3f177-235">Si se admite la codificación en contexto, este método debe devolver WINCODEC \_ Err \_ TOOMUCHMETADATA cuando no hay suficiente relleno para realizar la codificación en contexto.</span><span class="sxs-lookup"><span data-stu-id="3f177-235">If in-place encoding is supported, this method should return WINCODEC\_ERR\_TOOMUCHMETADATA when there is insufficient padding to perform in-place encoding.</span></span> <span data-ttu-id="3f177-236">Si no se admite la codificación en contexto, este método debe devolver WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="3f177-236">If in-place encoding is not supported, this method should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

<span data-ttu-id="3f177-237">El método **IPersistStream:: GetSizeMax** debe implementarse y debe devolver el tamaño exacto del contenido de los metadatos que se escribiría en el almacenamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="3f177-237">The **IPersistStream::GetSizeMax** method must be implemented and must return the exact size of the metadata content that would be written in subsequent save.</span></span>

<span data-ttu-id="3f177-238">El método **IPersistStream:: IsDirty** debe implementarse si el escritor de metadatos se inicializa a través de una secuencia, para que una imagen pueda determinar de forma confiable si su contenido ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3f177-238">The **IPersistStream::IsDirty** method should be implemented if the metadata writer is initialized through a stream, so that an image can reliably determine whether its content has changed.</span></span>

<span data-ttu-id="3f177-239">Si el formato de los metadatos admite bloques de metadatos anidados, el escritor de metadatos debe delegar en los escritores de metadatos anidados la serialización de su contenido al guardar en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="3f177-239">If your metadata format supports nested metadata blocks, your metadata writer should delegate to the nested metadata writers the serializing of its content when saving to a stream.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="3f177-240">Interfaz IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="3f177-240">IWICStreamProvider Interface</span></span>

<span data-ttu-id="3f177-241">La implementación de la interfaz [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) para un escritor de metadatos es la misma que la de un lector de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-241">The implementation of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface for a metadata writer is the same as that of a metadata reader.</span></span> <span data-ttu-id="3f177-242">Para obtener más información, consulte la sección creación de un lector de metadatos en este documento.</span><span class="sxs-lookup"><span data-stu-id="3f177-242">For more information, see Creating a Metadata Reader section in this document.</span></span>

## <a name="installing-and-registering-a-metadata-handler"></a><span data-ttu-id="3f177-243">Instalación y registro de un controlador de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-243">Installing and Registering a Metadata Handler</span></span>

<span data-ttu-id="3f177-244">Para instalar un controlador de metadatos, debe proporcionar el ensamblado de controlador y registrarlo en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="3f177-244">To install a metadata handler, you must provide the handler assembly and register it in the system registry.</span></span> <span data-ttu-id="3f177-245">Puede decidir cómo y cuándo se rellenan las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="3f177-245">You can decide how and when the registry keys are populated.</span></span>

> [!Note]  
> <span data-ttu-id="3f177-246">Para facilitar la lectura, los GUID hexadecimales reales no se muestran en las claves del registro que se muestran en las siguientes secciones de este documento.</span><span class="sxs-lookup"><span data-stu-id="3f177-246">For readability, the actual hexadecimal GUIDs are not shown in the registry keys shown in the following sections of this document.</span></span> <span data-ttu-id="3f177-247">Para buscar el valor hexadecimal de un nombre descriptivo especificado, vea los archivos wincodec. idl y wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="3f177-247">To find the hexadecimal value for a specified friendly name, see the wincodec.idl and wincodecsdk.idl files.</span></span>

 

### <a name="metadata-handler-registry-keys"></a><span data-ttu-id="3f177-248">Claves del registro del controlador de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-248">Metadata Handler Registry Keys</span></span>

<span data-ttu-id="3f177-249">Cada controlador de metadatos se identifica mediante un CLSID único y cada controlador debe registrar su CLSID en el GUID del identificador de categoría del controlador de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-249">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="3f177-250">Cada identificador de categoría del tipo de controlador se define en wincodec. idl; el nombre de identificador de categoría para los lectores es CATId \_ WICMetadataReader y el nombre de identificador de categoría para escritores es CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="3f177-250">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

<span data-ttu-id="3f177-251">Cada controlador de metadatos se identifica mediante un CLSID único y cada controlador debe registrar su CLSID en el GUID del identificador de categoría del controlador de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-251">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="3f177-252">Cada identificador de categoría del tipo de controlador se define en wincodec. idl; el nombre de identificador de categoría para los lectores es CATId \_ WICMetadataReader y el nombre de identificador de categoría para escritores es CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="3f177-252">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

> [!Note]  
> <span data-ttu-id="3f177-253">En las siguientes listas de claves del registro, {Reader CLSID} hace referencia al CLSID único que se proporciona para el lector de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-253">In the following registry key listings, {Reader CLSID} refers to the unique CLSID that you provide for your metadata reader.</span></span> <span data-ttu-id="3f177-254">{Writer CLSID} hace referencia al CLSID único que se proporciona para el escritor de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-254">{Writer CLSID} refers to the unique CLSID that you provide for your metadata writer.</span></span> <span data-ttu-id="3f177-255">{Handler CLSID} hace referencia al CLSID del lector, el CLSID del escritor o ambos, en función de los controladores que se proporcionen.</span><span class="sxs-lookup"><span data-stu-id="3f177-255">{Handler CLSID} refers to the reader's CLSID, the writer's CLSID, or both, depending on which handlers you are providing.</span></span> <span data-ttu-id="3f177-256">{Container GUID} hace referencia al objeto contenedor (formato de imagen o formato de metadatos) que puede contener el bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-256">{Container GUID} refers to the container object (image format or metadata format) that can contain the metadata block.</span></span>

 

<span data-ttu-id="3f177-257">Las siguientes claves del registro registran el controlador de metadatos con los demás controladores de metadatos disponibles:</span><span class="sxs-lookup"><span data-stu-id="3f177-257">The following registry keys register your metadata handler with the other metadata handlers available:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

<span data-ttu-id="3f177-258">Además de registrar los controladores en sus categorías respectivas, también debe registrar claves adicionales que proporcionen información específica del controlador.</span><span class="sxs-lookup"><span data-stu-id="3f177-258">In addition to registering your handlers in their respective categories, you must also register additional keys that provide information specific to the handler.</span></span> <span data-ttu-id="3f177-259">Los lectores y escritores comparten requisitos de clave del registro similares.</span><span class="sxs-lookup"><span data-stu-id="3f177-259">Readers and writers share similar registry key requirements.</span></span> <span data-ttu-id="3f177-260">En la sintaxis siguiente se muestra cómo registrar un controlador.</span><span class="sxs-lookup"><span data-stu-id="3f177-260">The following syntax shows how to register a handler.</span></span> <span data-ttu-id="3f177-261">Tanto el controlador de lector como el controlador del sistema de escritura deben registrarse de esta manera mediante sus respectivos CLSID:</span><span class="sxs-lookup"><span data-stu-id="3f177-261">Both the reader handler and writer handler must be registered in this way, using their respective CLSIDs:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a><span data-ttu-id="3f177-262">Lectores de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-262">Metadata Readers</span></span>

<span data-ttu-id="3f177-263">El registro del lector de metadatos también incluye claves que describen cómo se puede incrustar el lector en un formato de contenedor.</span><span class="sxs-lookup"><span data-stu-id="3f177-263">The metadata reader registration also includes keys that describe how the reader can be embedded in a container format.</span></span> <span data-ttu-id="3f177-264">Un formato de contenedor puede ser un formato de imagen como TIFF o JPEG; también puede ser otro formato de metadatos, como un bloque de metadatos de IFD.</span><span class="sxs-lookup"><span data-stu-id="3f177-264">A container format can be an image format such as TIFF or JPEG; it can also be another metadata format such as an IFD metadata block.</span></span> <span data-ttu-id="3f177-265">Los formatos de contenedor de imágenes compatibles de forma nativa se muestran en wincodec. idl; cada formato de contenedor de imágenes se define como un GUID con un nombre que comienza con el GUID \_ ContainerFormat.</span><span class="sxs-lookup"><span data-stu-id="3f177-265">Natively supported image container formats are listed in wincodec.idl; each image container format is defined as a GUID with a name that begins with GUID\_ContainerFormat.</span></span> <span data-ttu-id="3f177-266">Los formatos de contenedor de metadatos admitidos de forma nativa se enumeran en wincodecsdk. idl; cada formato de contenedor de metadatos se define como un GUID con un nombre que comienza con el GUID \_ MetadataFormat.</span><span class="sxs-lookup"><span data-stu-id="3f177-266">Natively supported metadata container formats are listed in wincodecsdk.idl; each metadata container format is defined as a GUID with a name that begins with GUID\_MetadataFormat.</span></span>

<span data-ttu-id="3f177-267">Las claves siguientes registran un contenedor que admite el lector de metadatos y los datos necesarios para leer de ese contenedor.</span><span class="sxs-lookup"><span data-stu-id="3f177-267">The following keys register a container that the metadata reader supports, and the data needed to read from that container.</span></span> <span data-ttu-id="3f177-268">Cada contenedor que admite el lector debe estar registrado de esta manera.</span><span class="sxs-lookup"><span data-stu-id="3f177-268">Each container supported by the reader must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

<span data-ttu-id="3f177-269">La clave de patrón describe el modelo binario que se usa para hacer coincidir el bloque de metadatos con el lector.</span><span class="sxs-lookup"><span data-stu-id="3f177-269">The Pattern key describes the binary pattern that is used to match the metadata block to the reader.</span></span> <span data-ttu-id="3f177-270">Al definir un patrón para el lector de metadatos, debe ser lo suficientemente confiable como para que una coincidencia positiva signifique que el lector de metadatos puede comprender los metadatos en el bloque de metadatos que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="3f177-270">When defining a pattern for your metadata reader, it should be reliable enough that a positive match means the metadata reader can understand the metadata in the metadata block being processed.</span></span>

<span data-ttu-id="3f177-271">La clave de desfase de datos describe el desplazamiento fijo de los metadatos a partir del encabezado de bloque.</span><span class="sxs-lookup"><span data-stu-id="3f177-271">The DataOffset key describes the fixed offset of the metadata from the block header.</span></span> <span data-ttu-id="3f177-272">Esta clave es opcional y, si no se especifica, significa que los metadatos reales no pueden encontrarse con un desplazamiento fijo del encabezado de bloque.</span><span class="sxs-lookup"><span data-stu-id="3f177-272">This key is optional and, if not specified, means that the actual metadata cannot be located using a fixed offset from the block header.</span></span>

### <a name="metadata-writers"></a><span data-ttu-id="3f177-273">Escritores de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-273">Metadata Writers</span></span>

<span data-ttu-id="3f177-274">El registro del escritor de metadatos también incluye claves que describen cómo escribir el encabezado que precede al contenido de los metadatos incrustado en un formato de contenedor.</span><span class="sxs-lookup"><span data-stu-id="3f177-274">The metadata writer registration also includes keys that describe how to write out the header preceding the metadata content embedded in a container format.</span></span> <span data-ttu-id="3f177-275">Al igual que con el lector, un formato de contenedor puede ser un formato de imagen u otro bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-275">As with the reader, a container format can be an image format or another metadata block.</span></span>

<span data-ttu-id="3f177-276">Las claves siguientes registran un contenedor que admite el escritor de metadatos y los datos necesarios para escribir el encabezado y los metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-276">The following keys register a container that the metadata writer supports, and the data needed to write the header and metadata.</span></span> <span data-ttu-id="3f177-277">Cada contenedor que admite el sistema de escritura debe estar registrado de esta manera.</span><span class="sxs-lookup"><span data-stu-id="3f177-277">Each container supported by the writer must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

<span data-ttu-id="3f177-278">La clave WriteHeader describe el patrón binario del encabezado de bloque de metadatos que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="3f177-278">The WriteHeader key describes the binary pattern of the metadata block header to be written.</span></span> <span data-ttu-id="3f177-279">Este patrón binario coincide con la clave del patrón de lector del formato de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-279">This binary pattern coincides with the metadata format's reader Pattern key.</span></span>

<span data-ttu-id="3f177-280">La clave WriteOffset describe el desplazamiento fijo del encabezado de bloque en el que deben escribirse los metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-280">The WriteOffset key describes the fixed offset from the block header at which the metadata should be written.</span></span> <span data-ttu-id="3f177-281">Esta clave es opcional y, si no se especifica, significa que los metadatos reales no deben escribirse con el encabezado.</span><span class="sxs-lookup"><span data-stu-id="3f177-281">This key is optional and, if not specified, means that the actual metadata should not be written out with the header.</span></span>

### <a name="signing-a-metadata-handler"></a><span data-ttu-id="3f177-282">Firmar un controlador de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-282">Signing a Metadata Handler</span></span>

<span data-ttu-id="3f177-283">Todos los controladores de metadatos deben estar firmados digitalmente para participar en el proceso de detección de WIC.</span><span class="sxs-lookup"><span data-stu-id="3f177-283">All metadata handlers must be digitally signed to participate in the WIC discovery process.</span></span> <span data-ttu-id="3f177-284">WIC no cargará ningún controlador que no esté firmado por una entidad de certificación de confianza.</span><span class="sxs-lookup"><span data-stu-id="3f177-284">WIC will not load any handler that is not signed by a trusted certificate authority.</span></span> <span data-ttu-id="3f177-285">Para obtener más información sobre la firma digital, vea [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f177-285">For more information on digital signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="special-considerations"></a><span data-ttu-id="3f177-286">Consideraciones especiales</span><span class="sxs-lookup"><span data-stu-id="3f177-286">Special Considerations</span></span>

<span data-ttu-id="3f177-287">En las secciones siguientes se incluye información adicional que debe tener en cuenta al crear sus propios controladores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-287">The following sections include additional information you must consider when creating your own metadata handlers.</span></span>

### <a name="propvariants"></a><span data-ttu-id="3f177-288">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="3f177-288">PROPVARIANTS</span></span>

<span data-ttu-id="3f177-289">WIC usa un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) para representar un elemento de metadatos para lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3f177-289">WIC uses a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to represent a metadata item for both reading and writing.</span></span> <span data-ttu-id="3f177-290">Un PROPVARIANT proporciona un tipo de datos y un valor de datos para un elemento de metadatos que se usa en un formato de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-290">A PROPVARIANT provides a data type and data value for a metadata item used within a metadata format.</span></span> <span data-ttu-id="3f177-291">Como escritor de un controlador de metadatos, tiene mucha flexibilidad en cuanto a cómo se almacenan los datos en el formato de metadatos y cómo se representan los datos dentro de un bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-291">As the writer of a metadata handler, you have a lot of flexibility on how data is stored in the metadata format and how data is represented within a metadata block.</span></span> <span data-ttu-id="3f177-292">En la tabla siguiente se proporcionan instrucciones que le ayudarán a decidir el tipo de PROPVARIANT adecuado para usarlo en diferentes situaciones.</span><span class="sxs-lookup"><span data-stu-id="3f177-292">The following table provides guidelines to help you decide on the appropriate PROPVARIANT type to use in different situations.</span></span>



| <span data-ttu-id="3f177-293">El tipo de metadatos es...</span><span class="sxs-lookup"><span data-stu-id="3f177-293">Metadata type is...</span></span>          | <span data-ttu-id="3f177-294">Uso del tipo PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="3f177-294">Use PROPVARIANT type</span></span>      | <span data-ttu-id="3f177-295">Propiedad PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="3f177-295">PROPVARIANT Property</span></span>                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f177-296">Vacío o no existe.</span><span class="sxs-lookup"><span data-stu-id="3f177-296">Empty or non-existent.</span></span>       | <span data-ttu-id="3f177-297">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="3f177-297">VT\_EMPTY</span></span>                 | <span data-ttu-id="3f177-298">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="3f177-298">Not applicable.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3f177-299">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="3f177-299">Undefined.</span></span>                   | <span data-ttu-id="3f177-300">BLOB de VT \_</span><span class="sxs-lookup"><span data-stu-id="3f177-300">VT\_BLOB</span></span>                  | <span data-ttu-id="3f177-301">Use la propiedad BLOB para establecer el tamaño y el puntero en el objeto de BLOB asignado mediante CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="3f177-301">Use the blob property to set the size and pointer to the BLOB object allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="3f177-302">Un bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-302">A metadata block.</span></span>            | <span data-ttu-id="3f177-303">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="3f177-303">VT\_UNKNOWN</span></span>               | <span data-ttu-id="3f177-304">Este tipo usa la propiedad punkVal.</span><span class="sxs-lookup"><span data-stu-id="3f177-304">This type uses the punkVal property.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="3f177-305">Matriz de tipos.</span><span class="sxs-lookup"><span data-stu-id="3f177-305">An array of types.</span></span>           | <span data-ttu-id="3f177-306">VT \_ Vector \| VT \_ {Type}</span><span class="sxs-lookup"><span data-stu-id="3f177-306">VT\_VECTOR \| VT\_{type}</span></span>  | <span data-ttu-id="3f177-307">Use la propiedad CA {Type} para establecer el recuento y el puntero a la matriz asignada mediante CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="3f177-307">Use the ca{type} property to set the count and pointer to the array allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="3f177-308">Matriz de bloques de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3f177-308">An array of metadata blocks.</span></span> | <span data-ttu-id="3f177-309">VT \_ Vector \| VT ( \_ variante)</span><span class="sxs-lookup"><span data-stu-id="3f177-309">VT\_VECTOR \| VT\_VARIANT</span></span> | <span data-ttu-id="3f177-310">Use la propiedad capropvar para establecer la matriz de variantes.</span><span class="sxs-lookup"><span data-stu-id="3f177-310">Use the capropvar property to set the array of variants.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="3f177-311">Valor racional con signo.</span><span class="sxs-lookup"><span data-stu-id="3f177-311">A signed rational value.</span></span>     | <span data-ttu-id="3f177-312">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="3f177-312">VT\_I8</span></span>                    | <span data-ttu-id="3f177-313">Use la propiedad hVal para establecer el valor.</span><span class="sxs-lookup"><span data-stu-id="3f177-313">Use the hVal property to set the value.</span></span> <span data-ttu-id="3f177-314">Establezca la palabra alta en el denominador y la palabra inferior en el numerador.</span><span class="sxs-lookup"><span data-stu-id="3f177-314">Set the high word to the denominator and the low word to the numerator.</span></span>                                                                                                                                                                |
| <span data-ttu-id="3f177-315">Un valor racional.</span><span class="sxs-lookup"><span data-stu-id="3f177-315">A rational value.</span></span>            | <span data-ttu-id="3f177-316">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="3f177-316">VT\_UI8</span></span>                   | <span data-ttu-id="3f177-317">Use la propiedad uhVal para establecer el valor.</span><span class="sxs-lookup"><span data-stu-id="3f177-317">Use the uhVal property to set the value.</span></span> <span data-ttu-id="3f177-318">Establezca HighPart en el denominador y el LowPart en el numerador.</span><span class="sxs-lookup"><span data-stu-id="3f177-318">Set the HighPart to the denominator and the LowPart to the numerator.</span></span> <span data-ttu-id="3f177-319">Tenga en cuenta que LowPart es un int sin signo. El numerador se debe convertir de un int sin signo a un entero para asegurarse de que el bit de signo se conserva si está presente.</span><span class="sxs-lookup"><span data-stu-id="3f177-319">Note that the LowPart is an unsigned int. The numerator should be converted from an unsigned int to an int to ensure that the sign bit is preserved if present.</span></span> |



 

<span data-ttu-id="3f177-320">Para evitar la redundancia en la representación de elementos de matriz, no utilice matrices seguras; Use solo matrices simples.</span><span class="sxs-lookup"><span data-stu-id="3f177-320">To avoid redundancy in representing array items, do not use safe arrays; use only simple arrays.</span></span> <span data-ttu-id="3f177-321">Esto reduce el trabajo que una aplicación necesita realizar al interpretar los tipos de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="3f177-321">This reduces the work an application needs to perform when interpreting [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types.</span></span>

<span data-ttu-id="3f177-322">Evite usar `VT_BYREF` y almacenar valores en línea siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="3f177-322">Avoid using `VT_BYREF` and store values inline whenever possible.</span></span> <span data-ttu-id="3f177-323">`VT_BYREF` no es eficaz para los tipos pequeños (comunes para los elementos de metadatos) y no proporciona información de tamaño.</span><span class="sxs-lookup"><span data-stu-id="3f177-323">`VT_BYREF` is inefficient for small types (common for metadata items) and does not provide size information.</span></span>

<span data-ttu-id="3f177-324">Antes de usar [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), llame siempre a **PropVariantInit** para inicializar el valor.</span><span class="sxs-lookup"><span data-stu-id="3f177-324">Before using a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), always call **PropVariantInit** to initialize the value.</span></span> <span data-ttu-id="3f177-325">Cuando haya terminado con el PROPVARIANT, llame siempre a **PropVariantClear** para liberar cualquier memoria asignada a la variable.</span><span class="sxs-lookup"><span data-stu-id="3f177-325">When you are finished with the PROPVARIANT, always call **PropVariantClear** to release any memory allocated for the variable.</span></span>

### <a name="8bim-handlers"></a><span data-ttu-id="3f177-326">Controladores 8BIM</span><span class="sxs-lookup"><span data-stu-id="3f177-326">8BIM Handlers</span></span>

<span data-ttu-id="3f177-327">Al escribir un controlador de metadatos para un bloque de metadatos de 8BIM, debe usar una firma que encapsule la firma 8BIM y el identificador.</span><span class="sxs-lookup"><span data-stu-id="3f177-327">When writing a metadata handler for an 8BIM metadata block, you must use a signature that encapsulates both the 8BIM signature and the ID.</span></span> <span data-ttu-id="3f177-328">Por ejemplo, el lector de metadatos 8BIMIPTC nativo proporciona la siguiente información del registro para la detección del lector:</span><span class="sxs-lookup"><span data-stu-id="3f177-328">For example, the native 8BIMIPTC metadata reader provides the following registry information for reader discovery:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

<span data-ttu-id="3f177-329">El lector 8BIMIPTC tiene un patrón registrado de 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span><span class="sxs-lookup"><span data-stu-id="3f177-329">The 8BIMIPTC reader has a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span></span> <span data-ttu-id="3f177-330">Los primeros cuatro bytes (0x38, 0x42, 0x49, 0x4D) son la firma 8BIM y los dos últimos bytes (0x04, 0x04) son el identificador del registro IPTC.</span><span class="sxs-lookup"><span data-stu-id="3f177-330">The first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature, and the last two bytes (0x04, 0x04) are the ID for the IPTC record.</span></span>

<span data-ttu-id="3f177-331">Por lo tanto, para escribir un lector de metadatos de 8BIM para la información de resolución, necesitaría un patrón registrado de 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span><span class="sxs-lookup"><span data-stu-id="3f177-331">So, to write an 8BIM metadata reader for resolution information, you would need a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span></span> <span data-ttu-id="3f177-332">De nuevo, los cuatro primeros bytes (0x38, 0x42, 0x49, 0x4D) son la firma 8BIM.</span><span class="sxs-lookup"><span data-stu-id="3f177-332">Again, the first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature.</span></span> <span data-ttu-id="3f177-333">Sin embargo, los dos últimos bytes (0x03, 0xED) son el identificador de la información de resolución tal y como se define en el formato PSD.</span><span class="sxs-lookup"><span data-stu-id="3f177-333">The last two bytes (0x03, 0xED), however, are the resolution information ID as defined by the PSD format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f177-334">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f177-334">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3f177-335">**Vista**</span><span class="sxs-lookup"><span data-stu-id="3f177-335">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3f177-336">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="3f177-336">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="3f177-337">Información general sobre metadatos de WIC</span><span class="sxs-lookup"><span data-stu-id="3f177-337">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="3f177-338">Información general del lenguaje de consulta de metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-338">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="3f177-339">Información general sobre la lectura y escritura de metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="3f177-339">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="3f177-340">Cómo volver a codificar una imagen JPEG con metadatos</span><span class="sxs-lookup"><span data-stu-id="3f177-340">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

<span data-ttu-id="3f177-341">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="3f177-341">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3f177-342">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="3f177-342">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
