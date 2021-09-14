---
description: En este tema se presentan el nuevo esquema de Extensible Metadata Platform (XMP) y la propiedad de foto system.Photo.PeopleNames de Windows 7 que permite el etiquetado de personas en una foto digital.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Introducción al etiquetado de personas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362782"
---
# <a name="people-tagging-overview"></a>Introducción al etiquetado de personas

En este tema se presentan el nuevo esquema de Extensible Metadata Platform (XMP) y la propiedad de foto [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) de Windows 7 que permite el etiquetado de personas en una foto digital. En este tema también se describe cómo usar la API Windows Imaging Component (WIC) para leer y escribir los metadatos necesarios para el etiquetado de personas.

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Introducción](#introduction)
-   [Etiquetado de personas](#people-tagging-overview)
    -   [Nombres de personas](#people-names)
    -   [Rectángulos de personas](#people-rectangles)
-   [Referencia de esquema](#schema-reference)
    -   [Esquema de Microsoft Photo 1.2](#microsoft-photo-12-schema)
    -   [Microsoft Photo RegionInfo Schema](#microsoft-photo-regioninfo-schema)
    -   [Esquema de la región foto de Microsoft](#microsoft-photo-regioninfo-schema)
    -   [Metadatos de ejemplo](#sample-metadata)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Prerrequisitos

Para comprender este tema, debe estar familiarizado con las interfaces de descodificador de WIC y sus componentes de Modelo de objetos componentes (COM) relacionados, como se describe en la introducción a los componentes de creación de imágenes de [Windows.](-wic-about-windows-imaging-codec.md) También ayuda a familiarizarse con los metadatos de creación de imágenes, especialmente XMP.

## <a name="introduction"></a>Introducción

Microsoft ha creado un nuevo esquema XMP para etiquetar personas dentro de una imagen digital. Este esquema permite a las aplicaciones almacenar los nombres y las ubicaciones de las personas que se encuentran en la imagen como metadatos dentro de la imagen. Además del nuevo esquema, la nueva propiedad [photo System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) está disponible en Windows 7. Esta nueva propiedad permite a las aplicaciones leer los nombres del usuario almacenados en los metadatos de la imagen. WIC usa estas nuevas características al permitir que las aplicaciones lean y escriban fácilmente los metadatos de los usuarios en fotos digitales.

## <a name="people-tagging"></a>Etiquetado de personas

WIC proporciona a los desarrolladores de aplicaciones componentes COM que leen datos de imagen, así como metadatos de imagen. Para leer y escribir metadatos, como la nueva característica de etiquetado de personas, WIC proporciona las interfaces [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) e [**IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) Estas interfaces permiten a las aplicaciones usar el lenguaje [de consulta de metadatos](-wic-codec-metadataquerylanguage.md) para escribir metadatos en los fotogramas individuales de una imagen. En la sección siguiente se muestra cómo leer y escribir los metadatos de etiquetado de personas en los metadatos de una imagen mediante lectores y escritores de consultas WIC.

### <a name="people-names"></a>Nombres de personas

Parte de la característica de etiquetado de personas es la capacidad de obtener simplemente una lista de los nombres de las personas etiquetadas dentro de la imagen. Esta parte de la característica es compatible con los controladores de [metadatos de System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) y WIC. La [**interfaz IWICMetadataQueryReader,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) junto con la propiedad System.Photo.PeopleNames, se usa para leer los nombres de las personas identificadas en una imagen y almacenadas en los metadatos de la imagen.

En el ejemplo de código siguiente se muestra un lector de consultas obtenido de un marco de imagen para consultar los metadatos de una imagen en busca de nombres etiquetados de la propiedad [System.Photo.PeopleNames.](../properties/props-system-photo-peoplenames.md)


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



La expresión de consulta "System.Photo.PeopleNames" consulta el marco para la propiedad . Si los metadatos de etiquetado de personas existen y contienen nombres de personas, el valor [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) se establecerá en VT LPWSTR y el valor de datos contendrá la lista de nombres \_ etiquetados. Para obtener más información sobre la lectura de metadatos de imagen, vea [Información general sobre la lectura y escritura de metadatos de imagen.](-wic-codec-readingwritingmetadata.md)

La consulta de la etiqueta people names solo es útil si la imagen contiene realmente los metadatos de etiquetado de personas. Para que esto ocurra, una aplicación debe haberla escrito primero. Para escribir los metadatos de nombres de personas, use [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) y la ruta de acceso XMP explícita de los metadatos. En el ejemplo de código siguiente se muestra cómo usar un escritor de consultas para escribir un nombre en la ruta de acceso de la consulta.


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



Observe el paso para construir la estructura XMP y establecerla en `MPRI:Regions/{ulong=0}` . Sin este paso, wic no puede identificar dónde colocar más `PersonDisplayName` adelante. Tenga en cuenta también que se usa la ruta de acceso de consulta explícita en lugar de [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md), cuya directiva de metadatos no admite la escritura de metadatos.

### <a name="people-rectangles"></a>Rectángulos de personas

Sin embargo, los nombres de los usuarios solo forman parte de la característica de etiquetado de personas. Además de almacenar los nombres de las personas en los metadatos, el esquema también admite información de región que identifica el área específica (un rectángulo) que la persona se muestra en la imagen.

La información del rectángulo se representa mediante cuatro valores decimales delimitados por comas, como "0,25, 0,25, 0,25, 0,25". Los dos primeros valores especifican la coordenada superior izquierda; los dos últimos especifican el alto y el ancho del rectángulo. Las dimensiones de la imagen para definir rectángulos de personas se normalizan en 1, lo que significa que en el ejemplo "0,25, 0,25, 0,25, 0,25" el rectángulo comienza 1/4 de la distancia desde la parte superior y 1/4 de la distancia desde la izquierda de la imagen. Tanto el alto como el ancho del rectángulo son 1/4 del tamaño de sus respectivas dimensiones de imagen.

La información del rectángulo que identifica a los individuos se escribe de la misma manera que se escriben los nombres de las personas, dentro de la misma estructura. Para escribir los metadatos del rectángulo, use [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) y la ruta de acceso XMP explícita de los metadatos. En el ejemplo de código siguiente se continúa con el ejemplo anterior y se agrega un rectángulo que representa "John Doe" a los metadatos de la imagen. Tenga en cuenta que usa el mismo `{ulong=0}` índice para asociar este rectángulo a "John Doe".


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

Los esquemas XMP de Microsoft para el etiquetado de personas definen un conjunto de propiedades para etiquetar individuos en fotos digitales.

En las secciones siguientes se proporcionan las definiciones de esquema necesarias para el etiquetado de personas. Siempre que sea posible, las definiciones de esquema usan las convenciones proporcionadas por las especificaciones de [extensible Metadata Platform (XMP) de Adobe.](https://www.adobe.com/devnet/xmp/) Las definiciones de esquema de este tema muestran el identificador uniforme de recursos (URI) del espacio de nombres XML que identifica el esquema y el prefijo de espacio de nombres de esquema preferido, seguido de una tabla que enumera todas las propiedades definidas para el esquema. Cada tabla tiene las siguientes columnas:

-   **Propiedad:** nombre de la propiedad, incluido el prefijo de espacio de nombres preferido.

-   **Tipo de** valor: tipo de valor de la propiedad. Los esquemas de compatibilidad con el etiquetado de personas usan los tipos de valor XMP siempre que sea posible, incluidos Date y Text. Los tipos de matriz van precedidos del tipo de contenedor: `alt` `bag` , o `seq` .

-   **Categoría:** las propiedades de esquema son internas o externas:

    -   La aplicación debe establecer los metadatos internos.

    -   El usuario debe establecer los metadatos externos y es independiente del contenido del documento.

-   **Descripción:** la descripción de la propiedad.

### <a name="microsoft-photo-12-schema"></a>Esquema de Microsoft Photo 1.2

El esquema de Microsoft Photo 1.2 proporciona un conjunto de propiedades para las regiones de imagen.

-   El URI del espacio de nombres de esquema es `https://ns.microsoft.com/photo/1.2/` .
-   El prefijo de espacio de nombres de esquema preferido es `MP` .



| Propiedad      | Tipo de valor | Category | Descripción                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP:RegionInfo | RegionInfo | Interno | **required:** almacena la raíz de los metadatos de etiquetado de personas. Consulte la sección Microsoft Photo RegionInfo Schema (Esquema de Microsoft Photo RegionInfo) que se muestra a continuación. |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Microsoft Photo RegionInfo Schema

El esquema Microsoft Photo RegionInfo 1.2 proporciona un conjunto de propiedades para la información de la región.

-   El URI del espacio de nombres de esquema es `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   El prefijo de espacio de nombres de esquema preferido es `MPRI` .



| Propiedad              | Tipo de valor | Category | Descripción                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI:DateRegionsValid | Date       | Externo | **opcional:** fecha en que se creó la última región.                                                          |
| MPRI:Regiones          | región de la bolsa | Externo | **required:** almacena las regiones de etiquetado de personas. Consulte la sección Esquema de la región foto de Microsoft que se muestra a continuación. |



 

### <a name="microsoft-photo-region-schema"></a>Esquema de la región foto de Microsoft

El esquema de Microsoft Photo Region 1.2 proporciona un conjunto de propiedades para las regiones de imagen.

-   El URI del espacio de nombres de esquema es `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   El prefijo de espacio de nombres de esquema preferido es `MPReg` .



| MPReg:Property          | Tipo de valor | Category | Descripción                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPReg:PersonDisplayName | Texto       | Externo | **required:** almacena el nombre de la persona en el rectángulo especificado.                                                                                                                                                                                                                                            |
| MPReg:Rectangle         | Texto       | Externo | **opcional:** almacena el rectángulo que identifica a la persona dentro de la foto. El rectángulo se almacena como cuatro valores decimales delimitados por comas. Los dos primeros valores especifican la coordenada superior izquierda; los dos últimos especifican el alto y el ancho del rectángulo. Los valores decimales deben normalizarse en 1. |
| MPReg:PersonEmailDigest | Texto       | Externo | **opcional:** almacena el hash de mensajes cifrados SHA-1 de la dirección de correo electrónico en directo de la persona.                                                                                                                                                                                                                     |
| MPReg:PersonLiveIdCID   | Texto       | Externo | **opcional:** almacena la representación decimal con signo del CID en directo de la persona, un entero de 64 bits que identifica públicamente una identidad en directo.                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>Metadatos de ejemplo

A continuación se muestra una representación de los metadatos XMP para el etiquetado de personas.

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

**Conceptual**
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Introducción a los metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre la lectura y escritura de metadatos de imagen](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Información general sobre el lenguaje de consulta de metadatos](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
