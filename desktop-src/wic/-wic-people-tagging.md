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
# <a name="people-tagging-overview"></a>Información general sobre el etiquetado de personas

En este tema se presenta el nuevo esquema de la plataforma de metadatos extensible (XMP) y la propiedad Photo de Windows 7 [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) que permite el etiquetado de personas en una fotografía digital. En este tema también se describe cómo usar la API de Windows Imaging Component (WIC) para leer y escribir los metadatos necesarios para el etiquetado de personas.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Etiquetado de personas](#people-tagging-overview)
    -   [Nombres de personas](#people-names)
    -   [Rectángulos de personas](#people-rectangles)
-   [Referencia de esquema](#schema-reference)
    -   [Esquema de Microsoft Photo 1,2](#microsoft-photo-12-schema)
    -   [Esquema de Microsoft Photo RegionInfo](#microsoft-photo-regioninfo-schema)
    -   [Esquema de la región de fotos de Microsoft](#microsoft-photo-regioninfo-schema)
    -   [Metadatos de ejemplo](#sample-metadata)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

Para entender este tema, debe estar familiarizado con las interfaces del descodificador de WIC y sus componentes de modelo de objetos componentes (COM) relacionados, tal como se describe en [información general sobre el componente de creación de imágenes de Windows](-wic-about-windows-imaging-codec.md). También ayuda a tener una familiaridad general con los metadatos de la creación de imágenes, especialmente XMP.

## <a name="introduction"></a>Introducción

Microsoft ha creado un nuevo esquema XMP para etiquetar a los usuarios de una imagen digital. Este esquema permite a las aplicaciones almacenar los nombres y las ubicaciones de las personas que se encuentran en la imagen como metadatos en la imagen. Además del nuevo esquema, la nueva propiedad de foto [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) está disponible en Windows 7. Esta nueva propiedad permite a las aplicaciones leer los nombres de las personas almacenadas en los metadatos de la imagen. WIC emplea estas nuevas características al permitir que las aplicaciones lean y escriban fácilmente los metadatos de etiquetado de las fotos digitales.

## <a name="people-tagging"></a>Etiquetado de personas

WIC proporciona a los desarrolladores de aplicaciones los componentes COM que leen los datos de la imagen, así como los metadatos de la imagen. Para leer y escribir metadatos, como la nueva característica de etiquetado de personas, WIC proporciona las interfaces [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) y [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Estas interfaces permiten a las aplicaciones usar el [lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md) para escribir metadatos en los marcos individuales de una imagen. En la siguiente sección se muestra cómo leer y escribir metadatos de etiquetado de personas en los metadatos de una imagen mediante lectores y escritores de consultas de WIC.

### <a name="people-names"></a>Nombres de personas

Parte de la característica de etiquetado de personas es la capacidad de simplemente obtener una lista de los nombres de las personas etiquetadas dentro de la imagen. Esta parte de la característica es compatible con los controladores de metadatos de [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) y WIC. La interfaz [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , junto con la propiedad System. Photo. PeopleNames, se usa para leer los nombres de las personas identificadas en una imagen y almacenadas en los metadatos de la imagen.

En el ejemplo de código siguiente se muestra un lector de consultas Obtenido de un fotograma de imagen para consultar los metadatos de una imagen para los nombres etiquetados de la propiedad [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .


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



La expresión de consulta "System. Photo. PeopleNames" consulta el marco para la propiedad. Si existen metadatos de etiquetado de personas y contiene nombres de personas, el valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) se establecerá en VT \_ LPWStr y el valor de los datos contendrá la lista de nombres etiquetados. Para obtener más información sobre cómo leer metadatos de imagen, vea [información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md).

La consulta de la etiqueta nombres de personas solo es útil si la imagen contiene realmente los metadatos de etiquetado de personas. Para que esto suceda, una aplicación debe escribirla primero. Para escribir los metadatos de los nombres de las personas, use un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) y la ruta de acceso de XMP explícita de los metadatos. En el ejemplo de código siguiente se muestra cómo usar un escritor de consultas para escribir un nombre en la ruta de la consulta.


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



Tenga en cuenta el paso que construye la estructura XMP y la establece en `MPRI:Regions/{ulong=0}` . Sin este paso, el WIC no puede identificar dónde colocarlo `PersonDisplayName` más adelante. Tenga en cuenta también que se usa la ruta de acceso de consulta explícita en lugar de [System. Photo. PeopleNames](-wic-photoprop-system-photo-peoplenames.md), cuya directiva de metadatos no admite la escritura de metadatos.

### <a name="people-rectangles"></a>Rectángulos de personas

Sin embargo, los nombres de las personas solo forman parte de la característica de etiquetado de personas. Además de almacenar los nombres de las personas en los metadatos, el esquema también admite la información de la región que identifica el área específica (un rectángulo) que la persona se muestra en la imagen.

La información del rectángulo se representa mediante cuatro valores decimales delimitados por comas, como "0,25, 0,25, 0,25, 0,25". Los dos primeros valores especifican la coordenada superior izquierda; las dos últimas especifican el alto y el ancho del rectángulo. Las dimensiones de la imagen con el fin de definir rectángulos de personas se normalizan en 1, lo que significa que en el ejemplo "0,25, 0,25, 0,25, 0,25", el rectángulo inicia 1/4 de la distancia desde la parte superior y el 1/4 de la distancia desde la izquierda de la imagen. Tanto el alto como el ancho del rectángulo son 1/4 del tamaño de sus dimensiones de imagen respectivas.

La información del rectángulo que identifica a las personas se escribe de la misma manera en que se escriben los nombres de las personas, dentro de la misma estructura. Para escribir los metadatos del rectángulo, use un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) y la ruta de acceso de XMP explícita de los metadatos. En el ejemplo de código siguiente se continúa el ejemplo anterior y se agrega un rectángulo que representa "John Doe" a los metadatos de la imagen. Tenga en cuenta que usa el mismo `{ulong=0}` Índice para asociar este rectángulo a "John Doe".


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



## <a name="schema-reference"></a>Referencia de esquemas

Los esquemas XMP de Microsoft para el etiquetado de personas definen un conjunto de propiedades para etiquetar personas en fotos digitales.

En las secciones siguientes se proporcionan las definiciones de esquema necesarias para el etiquetado de personas. Siempre que sea posible, las definiciones de esquema usan las convenciones proporcionadas por las [Especificaciones de la plataforma de metadatos extensible (XMP) de Adobe](https://www.adobe.com/devnet/xmp/). En las definiciones de esquema de este tema se muestra el identificador uniforme de recursos (URI) del espacio de nombres XML que identifica el esquema y el prefijo de espacio de nombres del esquema preferido, seguido de una tabla que muestra todas las propiedades definidas para el esquema. Cada tabla tiene las columnas siguientes:

-   **Property** : el nombre de la propiedad, incluido el prefijo de espacio de nombres preferido.

-   **Tipo de valor** : el tipo de valor de la propiedad. Los esquemas compatibles con el etiquetado de personas usan los tipos de valor XMP siempre que sea posible, incluidas la fecha y el texto. Los tipos de matriz van precedidos del tipo de contenedor: `alt` , `bag` o `seq` .

-   Las propiedades de los esquemas de **categoría** son internas o externas:

    -   La aplicación debe establecer los metadatos internos.

    -   El usuario debe establecer los metadatos externos y es independiente del contenido del documento.

-   **Descripción** : la descripción de la propiedad.

### <a name="microsoft-photo-12-schema"></a>Esquema de Microsoft Photo 1,2

El esquema de Microsoft Photo 1,2 proporciona un conjunto de propiedades para las regiones de la imagen.

-   El URI del espacio de nombres del esquema es `https://ns.microsoft.com/photo/1.2/` .
-   El prefijo del espacio de nombres del esquema preferido es `MP` .



| Propiedad      | Tipo de valor | Category | Descripción                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP: RegionInfo | RegionInfo | Interno | **requerido** : almacena la raíz de los metadatos de etiquetado de personas. Vea la sección esquema de Microsoft Photo RegionInfo que se incluye a continuación. |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Esquema de Microsoft Photo RegionInfo

El esquema de Microsoft Photo RegionInfo 1,2 proporciona un conjunto de propiedades para la información de la región.

-   El URI del espacio de nombres del esquema es `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   El prefijo del espacio de nombres del esquema preferido es `MPRI` .



| Propiedad              | Tipo de valor | Category | Descripción                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI:DateRegionsValid | Fecha       | Externo | **opcional** : fecha en que se creó la última región.                                                          |
| MPRI: regiones          | Región de bolsa | Externo | **requerido** : almacena las regiones de etiquetado de personas. Vea la sección esquema de la región fotográfica de Microsoft siguiente. |



 

### <a name="microsoft-photo-region-schema"></a>Esquema de la región de fotos de Microsoft

El esquema de Microsoft Photo Region 1,2 proporciona un conjunto de propiedades para las regiones de la imagen.

-   El URI del espacio de nombres del esquema es `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   El prefijo del espacio de nombres del esquema preferido es `MPReg` .



| MPReg: propiedad          | Tipo de valor | Category | Descripción                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPReg:PersonDisplayName | Texto       | Externo | **requerido** : almacena el nombre de la persona en el rectángulo especificado.                                                                                                                                                                                                                                            |
| MPReg: rectángulo         | Texto       | Externo | **opcional** : almacena el rectángulo que identifica a la persona de la fotografía. El rectángulo se almacena como cuatro valores decimales delimitados por comas. Los dos primeros valores especifican la coordenada superior izquierda; las dos últimas especifican el alto y el ancho del rectángulo. Los valores decimales se deben normalizar en 1. |
| MPReg:PersonEmailDigest | Texto       | Externo | **opcional** : almacena el hash de mensaje cifrado SHA-1 de la dirección de correo electrónico activa de la persona.                                                                                                                                                                                                                     |
| MPReg:PersonLiveIdCID   | Texto       | Externo | **opcional** : almacena la representación decimal con signo del Cid en directo de la persona, un entero de 64 bits que identifica públicamente una identidad dinámica.                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>Metadatos de ejemplo

La siguiente es una representación de los metadatos XMP para el etiquetado de personas.

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Información general del lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
