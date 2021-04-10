---
description: En este tema se presenta el nuevo esquema de la plataforma de metadatos extensible (XMP) y la propiedad Photo de Windows 7 System. Photo. PeopleNames que permite el etiquetado de personas en una fotografía digital.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Información general sobre el etiquetado de personas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156740"
---
# <a name="people-tagging-overview"></a><span data-ttu-id="3a68c-103">Información general sobre el etiquetado de personas</span><span class="sxs-lookup"><span data-stu-id="3a68c-103">People Tagging Overview</span></span>

<span data-ttu-id="3a68c-104">En este tema se presenta el nuevo esquema de la plataforma de metadatos extensible (XMP) y la propiedad Photo de Windows 7 [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) que permite el etiquetado de personas en una fotografía digital.</span><span class="sxs-lookup"><span data-stu-id="3a68c-104">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span> <span data-ttu-id="3a68c-105">En este tema también se describe cómo usar la API de Windows Imaging Component (WIC) para leer y escribir los metadatos necesarios para el etiquetado de personas.</span><span class="sxs-lookup"><span data-stu-id="3a68c-105">This topic also discusses how to use the Windows Imaging Component (WIC) API to both read and write the metadata needed for people tagging.</span></span>

<span data-ttu-id="3a68c-106">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="3a68c-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3a68c-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3a68c-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="3a68c-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="3a68c-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="3a68c-109">Etiquetado de personas</span><span class="sxs-lookup"><span data-stu-id="3a68c-109">People Tagging</span></span>](#people-tagging-overview)
    -   [<span data-ttu-id="3a68c-110">Nombres de personas</span><span class="sxs-lookup"><span data-stu-id="3a68c-110">People Names</span></span>](#people-names)
    -   [<span data-ttu-id="3a68c-111">Rectángulos de personas</span><span class="sxs-lookup"><span data-stu-id="3a68c-111">People Rectangles</span></span>](#people-rectangles)
-   [<span data-ttu-id="3a68c-112">Referencia de esquema</span><span class="sxs-lookup"><span data-stu-id="3a68c-112">Schema Reference</span></span>](#schema-reference)
    -   [<span data-ttu-id="3a68c-113">Esquema de Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="3a68c-113">Microsoft Photo 1.2 Schema</span></span>](#microsoft-photo-12-schema)
    -   [<span data-ttu-id="3a68c-114">Esquema de Microsoft Photo RegionInfo</span><span class="sxs-lookup"><span data-stu-id="3a68c-114">Microsoft Photo RegionInfo Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="3a68c-115">Esquema de la región de fotos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="3a68c-115">Microsoft Photo Region Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="3a68c-116">Metadatos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a68c-116">Sample Metadata</span></span>](#sample-metadata)
-   [<span data-ttu-id="3a68c-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a68c-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="3a68c-118">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3a68c-118">Prerequisites</span></span>

<span data-ttu-id="3a68c-119">Para entender este tema, debe estar familiarizado con las interfaces del descodificador de WIC y sus componentes de modelo de objetos componentes (COM) relacionados, tal como se describe en [información general sobre el componente de creación de imágenes de Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="3a68c-119">To understand this topic, you should be familiar with the WIC decoder interfaces and its related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="3a68c-120">También ayuda a tener una familiaridad general con los metadatos de la creación de imágenes, especialmente XMP.</span><span class="sxs-lookup"><span data-stu-id="3a68c-120">It also helps to have a general familiarity with imaging metadata, especially XMP.</span></span>

## <a name="introduction"></a><span data-ttu-id="3a68c-121">Introducción</span><span class="sxs-lookup"><span data-stu-id="3a68c-121">Introduction</span></span>

<span data-ttu-id="3a68c-122">Microsoft ha creado un nuevo esquema XMP para etiquetar a los usuarios de una imagen digital.</span><span class="sxs-lookup"><span data-stu-id="3a68c-122">Microsoft has created a new XMP schema for tagging people within a digital image.</span></span> <span data-ttu-id="3a68c-123">Este esquema permite a las aplicaciones almacenar los nombres y las ubicaciones de las personas que se encuentran en la imagen como metadatos en la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-123">This schema enables applications to store the names and locations of individuals who are in the image as metadata within the image.</span></span> <span data-ttu-id="3a68c-124">Además del nuevo esquema, la nueva propiedad de foto [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) está disponible en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a68c-124">In addition to the new schema, the new photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) is available in Windows 7.</span></span> <span data-ttu-id="3a68c-125">Esta nueva propiedad permite a las aplicaciones leer los nombres de las personas almacenadas en los metadatos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-125">This new property enables applications to read the individual's names stored in the image metadata.</span></span> <span data-ttu-id="3a68c-126">WIC emplea estas nuevas características al permitir que las aplicaciones lean y escriban fácilmente los metadatos de etiquetado de las fotos digitales.</span><span class="sxs-lookup"><span data-stu-id="3a68c-126">WIC utilizes these new features by enabling applications to easily read and write people tagging metadata to digital photos.</span></span>

## <a name="people-tagging"></a><span data-ttu-id="3a68c-127">Etiquetado de personas</span><span class="sxs-lookup"><span data-stu-id="3a68c-127">People Tagging</span></span>

<span data-ttu-id="3a68c-128">WIC proporciona a los desarrolladores de aplicaciones los componentes COM que leen los datos de la imagen, así como los metadatos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-128">WIC provides application developers with COM components which read image data as well as image metadata.</span></span> <span data-ttu-id="3a68c-129">Para leer y escribir metadatos, como la nueva característica de etiquetado de personas, WIC proporciona las interfaces [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) y [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="3a68c-129">For reading and writing metadata, such as the new people tagging feature, WIC provides the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) and [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interfaces.</span></span> <span data-ttu-id="3a68c-130">Estas interfaces permiten a las aplicaciones usar el [lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md) para escribir metadatos en los marcos individuales de una imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-130">These interfaces enable applications to use the [metadata query language](-wic-codec-metadataquerylanguage.md) to write metadata to the individual frames of an image.</span></span> <span data-ttu-id="3a68c-131">En la siguiente sección se muestra cómo leer y escribir metadatos de etiquetado de personas en los metadatos de una imagen mediante lectores y escritores de consultas de WIC.</span><span class="sxs-lookup"><span data-stu-id="3a68c-131">The following section demonstrates how to read and write the people-tagging metadata into an image's metadata by using WIC query readers and writers.</span></span>

### <a name="people-names"></a><span data-ttu-id="3a68c-132">Nombres de personas</span><span class="sxs-lookup"><span data-stu-id="3a68c-132">People Names</span></span>

<span data-ttu-id="3a68c-133">Parte de la característica de etiquetado de personas es la capacidad de simplemente obtener una lista de los nombres de las personas etiquetadas dentro de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-133">Part of the people-tagging feature is the ability to simply get a list the names of the people tagged within the image.</span></span> <span data-ttu-id="3a68c-134">Esta parte de la característica es compatible con los controladores de metadatos de [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) y WIC.</span><span class="sxs-lookup"><span data-stu-id="3a68c-134">This part of the feature is supported by the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) and WIC's metadata handlers.</span></span> <span data-ttu-id="3a68c-135">La interfaz [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , junto con la propiedad System. Photo. PeopleNames, se usa para leer los nombres de las personas identificadas en una imagen y almacenadas en los metadatos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-135">The [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) interface, in conjunction with the System.Photo.PeopleNames property, are used to read the names of people identified in an image and stored in the image metadata.</span></span>

<span data-ttu-id="3a68c-136">En el ejemplo de código siguiente se muestra un lector de consultas Obtenido de un fotograma de imagen para consultar los metadatos de una imagen para los nombres etiquetados de la propiedad [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="3a68c-136">The following code example demonstrates a query reader obtained from an image frame to query an image's metadata for tagged names of the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



<span data-ttu-id="3a68c-137">La expresión de consulta "System. Photo. PeopleNames" consulta el marco para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3a68c-137">The query expression "System.Photo.PeopleNames" queries the frame for the property.</span></span> <span data-ttu-id="3a68c-138">Si existen metadatos de etiquetado de personas y contiene nombres de personas, el valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) se establecerá en VT \_ LPWStr y el valor de los datos contendrá la lista de nombres etiquetados.</span><span class="sxs-lookup"><span data-stu-id="3a68c-138">If the people-tagging metadata exists and contains people's names, the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will be set to VT\_LPWSTR and the data value will contain the list of tagged names.</span></span> <span data-ttu-id="3a68c-139">Para obtener más información sobre cómo leer metadatos de imagen, vea [información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="3a68c-139">For more information on reading image metadata, see [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="3a68c-140">La consulta de la etiqueta nombres de personas solo es útil si la imagen contiene realmente los metadatos de etiquetado de personas.</span><span class="sxs-lookup"><span data-stu-id="3a68c-140">Querying for the people names tag is only useful if the image actually contains the people-tagging metadata.</span></span> <span data-ttu-id="3a68c-141">Para que esto suceda, una aplicación debe escribirla primero.</span><span class="sxs-lookup"><span data-stu-id="3a68c-141">For this to occur, an application must first have written it.</span></span> <span data-ttu-id="3a68c-142">Para escribir los metadatos de los nombres de las personas, use un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) y la ruta de acceso de XMP explícita de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="3a68c-142">To write the people names metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="3a68c-143">En el ejemplo de código siguiente se muestra cómo usar un escritor de consultas para escribir un nombre en la ruta de la consulta.</span><span class="sxs-lookup"><span data-stu-id="3a68c-143">The following code example demonstrates using a query writer to write a name to the query path.</span></span>


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



<span data-ttu-id="3a68c-144">Tenga en cuenta el paso que construye la estructura XMP y la establece en `MPRI:Regions/{ulong=0}` .</span><span class="sxs-lookup"><span data-stu-id="3a68c-144">Note the step constructing the XMP structure and setting it under `MPRI:Regions/{ulong=0}`.</span></span> <span data-ttu-id="3a68c-145">Sin este paso, el WIC no puede identificar dónde colocarlo `PersonDisplayName` más adelante.</span><span class="sxs-lookup"><span data-stu-id="3a68c-145">Without this step, the WIC can't identify where to place the `PersonDisplayName` later on.</span></span> <span data-ttu-id="3a68c-146">Tenga en cuenta también que se usa la ruta de acceso de consulta explícita en lugar de [System. Photo. PeopleNames](-wic-photoprop-system-photo-peoplenames.md), cuya directiva de metadatos no admite la escritura de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3a68c-146">Also note that the explicit query path is used instead of [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md), whose metadata policy does not support writing metadata.</span></span>

### <a name="people-rectangles"></a><span data-ttu-id="3a68c-147">Rectángulos de personas</span><span class="sxs-lookup"><span data-stu-id="3a68c-147">People Rectangles</span></span>

<span data-ttu-id="3a68c-148">Sin embargo, los nombres de las personas solo forman parte de la característica de etiquetado de personas.</span><span class="sxs-lookup"><span data-stu-id="3a68c-148">People's names however, are only part of the people-tagging feature.</span></span> <span data-ttu-id="3a68c-149">Además de almacenar los nombres de las personas en los metadatos, el esquema también admite la información de la región que identifica el área específica (un rectángulo) que la persona se muestra en la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-149">In addition to storing people's names in the metadata, the schema also supports region information that identifies the specific area (a rectangle) the person is shown in the image.</span></span>

<span data-ttu-id="3a68c-150">La información del rectángulo se representa mediante cuatro valores decimales delimitados por comas, como "0,25, 0,25, 0,25, 0,25".</span><span class="sxs-lookup"><span data-stu-id="3a68c-150">The rectangle information is represented by four comma-delimited decimal values, such as "0.25, 0.25, 0.25, 0.25".</span></span> <span data-ttu-id="3a68c-151">Los dos primeros valores especifican la coordenada superior izquierda; las dos últimas especifican el alto y el ancho del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="3a68c-151">The first two values specify the top-left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="3a68c-152">Las dimensiones de la imagen con el fin de definir rectángulos de personas se normalizan en 1, lo que significa que en el ejemplo "0,25, 0,25, 0,25, 0,25", el rectángulo inicia 1/4 de la distancia desde la parte superior y el 1/4 de la distancia desde la izquierda de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-152">The dimensions of the image for the purposes of defining people rectangles are normalized to 1, which means that in the "0.25, 0.25, 0.25, 0.25" example, the rectangle starts 1/4 of the distance from the top and 1/4 of the distance from the left of the image.</span></span> <span data-ttu-id="3a68c-153">Tanto el alto como el ancho del rectángulo son 1/4 del tamaño de sus dimensiones de imagen respectivas.</span><span class="sxs-lookup"><span data-stu-id="3a68c-153">Both the height and width of the rectangle are 1/4 of the size of their respective image dimensions.</span></span>

<span data-ttu-id="3a68c-154">La información del rectángulo que identifica a las personas se escribe de la misma manera en que se escriben los nombres de las personas, dentro de la misma estructura.</span><span class="sxs-lookup"><span data-stu-id="3a68c-154">The rectangle information that identifies individuals is written in the same way people's names are written, within the same structure.</span></span> <span data-ttu-id="3a68c-155">Para escribir los metadatos del rectángulo, use un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) y la ruta de acceso de XMP explícita de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="3a68c-155">To write the rectangle metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="3a68c-156">En el ejemplo de código siguiente se continúa el ejemplo anterior y se agrega un rectángulo que representa "John Doe" a los metadatos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-156">The following code example continues the previous example and adds a rectangle representing 'John Doe' to the image's metadata.</span></span> <span data-ttu-id="3a68c-157">Tenga en cuenta que usa el mismo `{ulong=0}` Índice para asociar este rectángulo a "John Doe".</span><span class="sxs-lookup"><span data-stu-id="3a68c-157">Note that it uses the same `{ulong=0}` index to associate this rectangle with 'John Doe'.</span></span>


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a><span data-ttu-id="3a68c-158">Referencia de esquemas</span><span class="sxs-lookup"><span data-stu-id="3a68c-158">Schema Reference</span></span>

<span data-ttu-id="3a68c-159">Los esquemas XMP de Microsoft para el etiquetado de personas definen un conjunto de propiedades para etiquetar personas en fotos digitales.</span><span class="sxs-lookup"><span data-stu-id="3a68c-159">The Microsoft XMP schemas for people tagging define a set of properties to tag individuals in digital photos.</span></span>

<span data-ttu-id="3a68c-160">En las secciones siguientes se proporcionan las definiciones de esquema necesarias para el etiquetado de personas.</span><span class="sxs-lookup"><span data-stu-id="3a68c-160">The following sections provide the schema definitions needed for people tagging.</span></span> <span data-ttu-id="3a68c-161">Siempre que sea posible, las definiciones de esquema usan las convenciones proporcionadas por las [Especificaciones de la plataforma de metadatos extensible (XMP) de Adobe](https://www.adobe.com/devnet/xmp/).</span><span class="sxs-lookup"><span data-stu-id="3a68c-161">Wherever possible, the schema definitions use the conventions provided by [Adobe's Extensible Metadata Platform (XMP) Specifications](https://www.adobe.com/devnet/xmp/).</span></span> <span data-ttu-id="3a68c-162">En las definiciones de esquema de este tema se muestra el identificador uniforme de recursos (URI) del espacio de nombres XML que identifica el esquema y el prefijo de espacio de nombres del esquema preferido, seguido de una tabla que muestra todas las propiedades definidas para el esquema.</span><span class="sxs-lookup"><span data-stu-id="3a68c-162">The schema definitions in this topic show the XML namespace Uniform Resource Identifier (URI) that identifies the schema and the preferred schema namespace prefix, followed by a table that lists all properties defined for the schema.</span></span> <span data-ttu-id="3a68c-163">Cada tabla tiene las columnas siguientes:</span><span class="sxs-lookup"><span data-stu-id="3a68c-163">Each table has the following columns:</span></span>

-   <span data-ttu-id="3a68c-164">**Property** : el nombre de la propiedad, incluido el prefijo de espacio de nombres preferido.</span><span class="sxs-lookup"><span data-stu-id="3a68c-164">**Property** - The name of the property, including the preferred namespace prefix.</span></span>

-   <span data-ttu-id="3a68c-165">**Tipo de valor** : el tipo de valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3a68c-165">**Value type** - The value type of the property.</span></span> <span data-ttu-id="3a68c-166">Los esquemas compatibles con el etiquetado de personas usan los tipos de valor XMP siempre que sea posible, incluidas la fecha y el texto.</span><span class="sxs-lookup"><span data-stu-id="3a68c-166">The people-tagging support schemas use the XMP value types whenever possible, including Date and Text.</span></span> <span data-ttu-id="3a68c-167">Los tipos de matriz van precedidos del tipo de contenedor: `alt` , `bag` o `seq` .</span><span class="sxs-lookup"><span data-stu-id="3a68c-167">Array types are preceded by the container type: `alt`, `bag`, or `seq`.</span></span>

-   <span data-ttu-id="3a68c-168">Las propiedades de los esquemas de **categoría** son internas o externas:</span><span class="sxs-lookup"><span data-stu-id="3a68c-168">**Category** - Schema properties are internal or external:</span></span>

    -   <span data-ttu-id="3a68c-169">La aplicación debe establecer los metadatos internos.</span><span class="sxs-lookup"><span data-stu-id="3a68c-169">Internal metadata must be set by the application.</span></span>

    -   <span data-ttu-id="3a68c-170">El usuario debe establecer los metadatos externos y es independiente del contenido del documento.</span><span class="sxs-lookup"><span data-stu-id="3a68c-170">External metadata must be set by the user and is independent of the contents of the document.</span></span>

-   <span data-ttu-id="3a68c-171">**Descripción** : la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3a68c-171">**Description** - The description of the property.</span></span>

### <a name="microsoft-photo-12-schema"></a><span data-ttu-id="3a68c-172">Esquema de Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="3a68c-172">Microsoft Photo 1.2 Schema</span></span>

<span data-ttu-id="3a68c-173">El esquema de Microsoft Photo 1,2 proporciona un conjunto de propiedades para las regiones de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-173">The Microsoft Photo 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="3a68c-174">El URI del espacio de nombres del esquema es `https://ns.microsoft.com/photo/1.2/` .</span><span class="sxs-lookup"><span data-stu-id="3a68c-174">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/`.</span></span>
-   <span data-ttu-id="3a68c-175">El prefijo del espacio de nombres del esquema preferido es `MP` .</span><span class="sxs-lookup"><span data-stu-id="3a68c-175">The preferred schema namespace prefix is `MP`.</span></span>



| <span data-ttu-id="3a68c-176">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a68c-176">Property</span></span>      | <span data-ttu-id="3a68c-177">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="3a68c-177">Value type</span></span> | <span data-ttu-id="3a68c-178">Category</span><span class="sxs-lookup"><span data-stu-id="3a68c-178">Category</span></span> | <span data-ttu-id="3a68c-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a68c-179">Description</span></span>                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a68c-180">MP: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="3a68c-180">MP:RegionInfo</span></span> | <span data-ttu-id="3a68c-181">RegionInfo</span><span class="sxs-lookup"><span data-stu-id="3a68c-181">RegionInfo</span></span> | <span data-ttu-id="3a68c-182">Interno</span><span class="sxs-lookup"><span data-stu-id="3a68c-182">Internal</span></span> | <span data-ttu-id="3a68c-183">**requerido** : almacena la raíz de los metadatos de etiquetado de personas.</span><span class="sxs-lookup"><span data-stu-id="3a68c-183">**required** : Stores the root of the people-tagging metadata.</span></span> <span data-ttu-id="3a68c-184">Vea la sección esquema de Microsoft Photo RegionInfo que se incluye a continuación.</span><span class="sxs-lookup"><span data-stu-id="3a68c-184">See the Microsoft Photo RegionInfo Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-regioninfo-schema"></a><span data-ttu-id="3a68c-185">Esquema de Microsoft Photo RegionInfo</span><span class="sxs-lookup"><span data-stu-id="3a68c-185">Microsoft Photo RegionInfo Schema</span></span>

<span data-ttu-id="3a68c-186">El esquema de Microsoft Photo RegionInfo 1,2 proporciona un conjunto de propiedades para la información de la región.</span><span class="sxs-lookup"><span data-stu-id="3a68c-186">The Microsoft Photo RegionInfo 1.2 schema provides a set of properties for region info.</span></span>

-   <span data-ttu-id="3a68c-187">El URI del espacio de nombres del esquema es `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .</span><span class="sxs-lookup"><span data-stu-id="3a68c-187">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/RegionInfo#`.</span></span>
-   <span data-ttu-id="3a68c-188">El prefijo del espacio de nombres del esquema preferido es `MPRI` .</span><span class="sxs-lookup"><span data-stu-id="3a68c-188">The preferred schema namespace prefix is `MPRI`.</span></span>



| <span data-ttu-id="3a68c-189">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a68c-189">Property</span></span>              | <span data-ttu-id="3a68c-190">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="3a68c-190">Value type</span></span> | <span data-ttu-id="3a68c-191">Category</span><span class="sxs-lookup"><span data-stu-id="3a68c-191">Category</span></span> | <span data-ttu-id="3a68c-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a68c-192">Description</span></span>                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a68c-193">MPRI:DateRegionsValid</span><span class="sxs-lookup"><span data-stu-id="3a68c-193">MPRI:DateRegionsValid</span></span> | <span data-ttu-id="3a68c-194">Fecha</span><span class="sxs-lookup"><span data-stu-id="3a68c-194">Date</span></span>       | <span data-ttu-id="3a68c-195">Externo</span><span class="sxs-lookup"><span data-stu-id="3a68c-195">External</span></span> | <span data-ttu-id="3a68c-196">**opcional** : fecha en que se creó la última región.</span><span class="sxs-lookup"><span data-stu-id="3a68c-196">**optional** : Date that the last region was created.</span></span>                                                          |
| <span data-ttu-id="3a68c-197">MPRI: regiones</span><span class="sxs-lookup"><span data-stu-id="3a68c-197">MPRI:Regions</span></span>          | <span data-ttu-id="3a68c-198">Región de bolsa</span><span class="sxs-lookup"><span data-stu-id="3a68c-198">bag Region</span></span> | <span data-ttu-id="3a68c-199">Externo</span><span class="sxs-lookup"><span data-stu-id="3a68c-199">External</span></span> | <span data-ttu-id="3a68c-200">**requerido** : almacena las regiones de etiquetado de personas.</span><span class="sxs-lookup"><span data-stu-id="3a68c-200">**required** : Stores the people tagging regions.</span></span> <span data-ttu-id="3a68c-201">Vea la sección esquema de la región fotográfica de Microsoft siguiente.</span><span class="sxs-lookup"><span data-stu-id="3a68c-201">See the Microsoft Photo Region Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-region-schema"></a><span data-ttu-id="3a68c-202">Esquema de la región de fotos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="3a68c-202">Microsoft Photo Region Schema</span></span>

<span data-ttu-id="3a68c-203">El esquema de Microsoft Photo Region 1,2 proporciona un conjunto de propiedades para las regiones de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a68c-203">The Microsoft Photo Region 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="3a68c-204">El URI del espacio de nombres del esquema es `https://ns.microsoft.com/photo/1.2/t/Region#` .</span><span class="sxs-lookup"><span data-stu-id="3a68c-204">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/Region#`.</span></span>
-   <span data-ttu-id="3a68c-205">El prefijo del espacio de nombres del esquema preferido es `MPReg` .</span><span class="sxs-lookup"><span data-stu-id="3a68c-205">The preferred schema namespace prefix is `MPReg`.</span></span>



| <span data-ttu-id="3a68c-206">MPReg: propiedad</span><span class="sxs-lookup"><span data-stu-id="3a68c-206">MPReg:Property</span></span>          | <span data-ttu-id="3a68c-207">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="3a68c-207">Value type</span></span> | <span data-ttu-id="3a68c-208">Category</span><span class="sxs-lookup"><span data-stu-id="3a68c-208">Category</span></span> | <span data-ttu-id="3a68c-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a68c-209">Description</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a68c-210">MPReg:PersonDisplayName</span><span class="sxs-lookup"><span data-stu-id="3a68c-210">MPReg:PersonDisplayName</span></span> | <span data-ttu-id="3a68c-211">Texto</span><span class="sxs-lookup"><span data-stu-id="3a68c-211">Text</span></span>       | <span data-ttu-id="3a68c-212">Externo</span><span class="sxs-lookup"><span data-stu-id="3a68c-212">External</span></span> | <span data-ttu-id="3a68c-213">**requerido** : almacena el nombre de la persona en el rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="3a68c-213">**required** : Stores the name of the person in the given rectangle.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="3a68c-214">MPReg: rectángulo</span><span class="sxs-lookup"><span data-stu-id="3a68c-214">MPReg:Rectangle</span></span>         | <span data-ttu-id="3a68c-215">Texto</span><span class="sxs-lookup"><span data-stu-id="3a68c-215">Text</span></span>       | <span data-ttu-id="3a68c-216">Externo</span><span class="sxs-lookup"><span data-stu-id="3a68c-216">External</span></span> | <span data-ttu-id="3a68c-217">**opcional** : almacena el rectángulo que identifica a la persona de la fotografía.</span><span class="sxs-lookup"><span data-stu-id="3a68c-217">**optional** : Stores the rectangle that identifies the person within the photo.</span></span> <span data-ttu-id="3a68c-218">El rectángulo se almacena como cuatro valores decimales delimitados por comas.</span><span class="sxs-lookup"><span data-stu-id="3a68c-218">The rectangle is stored as four comma-delimited decimal values.</span></span> <span data-ttu-id="3a68c-219">Los dos primeros valores especifican la coordenada superior izquierda; las dos últimas especifican el alto y el ancho del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="3a68c-219">The first two values specify the top left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="3a68c-220">Los valores decimales se deben normalizar en 1.</span><span class="sxs-lookup"><span data-stu-id="3a68c-220">The decimal values must be normalized to 1.</span></span> |
| <span data-ttu-id="3a68c-221">MPReg:PersonEmailDigest</span><span class="sxs-lookup"><span data-stu-id="3a68c-221">MPReg:PersonEmailDigest</span></span> | <span data-ttu-id="3a68c-222">Texto</span><span class="sxs-lookup"><span data-stu-id="3a68c-222">Text</span></span>       | <span data-ttu-id="3a68c-223">Externo</span><span class="sxs-lookup"><span data-stu-id="3a68c-223">External</span></span> | <span data-ttu-id="3a68c-224">**opcional** : almacena el hash de mensaje cifrado SHA-1 de la dirección de correo electrónico activa de la persona.</span><span class="sxs-lookup"><span data-stu-id="3a68c-224">**optional** : Stores the SHA-1 encrypted message hash of the person's Live e-mail address.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="3a68c-225">MPReg:PersonLiveIdCID</span><span class="sxs-lookup"><span data-stu-id="3a68c-225">MPReg:PersonLiveIdCID</span></span>   | <span data-ttu-id="3a68c-226">Texto</span><span class="sxs-lookup"><span data-stu-id="3a68c-226">Text</span></span>       | <span data-ttu-id="3a68c-227">Externo</span><span class="sxs-lookup"><span data-stu-id="3a68c-227">External</span></span> | <span data-ttu-id="3a68c-228">**opcional** : almacena la representación decimal con signo del Cid en directo de la persona, un entero de 64 bits que identifica públicamente una identidad dinámica.</span><span class="sxs-lookup"><span data-stu-id="3a68c-228">**optional** :Stores the signed decimal representation of the person's Live CID, a 64-bit integer that publicly identifies a Live identity.</span></span>                                                                                                                                                                     |



 

### <a name="sample-metadata"></a><span data-ttu-id="3a68c-229">Metadatos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a68c-229">Sample Metadata</span></span>

<span data-ttu-id="3a68c-230">La siguiente es una representación de los metadatos XMP para el etiquetado de personas.</span><span class="sxs-lookup"><span data-stu-id="3a68c-230">The following is a representation of the XMP metadata for people tagging.</span></span>

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a><span data-ttu-id="3a68c-231">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a68c-231">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3a68c-232">**Vista**</span><span class="sxs-lookup"><span data-stu-id="3a68c-232">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3a68c-233">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="3a68c-233">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="3a68c-234">Información general sobre metadatos de WIC</span><span class="sxs-lookup"><span data-stu-id="3a68c-234">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="3a68c-235">Información general sobre la lectura y escritura de metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="3a68c-235">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="3a68c-236">Información general del lenguaje de consulta de metadatos</span><span class="sxs-lookup"><span data-stu-id="3a68c-236">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
