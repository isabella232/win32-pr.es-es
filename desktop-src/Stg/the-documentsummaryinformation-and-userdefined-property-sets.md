---
title: Conjuntos de propiedades DocumentSummaryInformation y UserDefined
description: Un conjunto de propiedades DocumentSummaryInformation y UserDefined es una extensión del conjunto de propiedades Información de resumen. Ambos conjuntos de propiedades pueden existir simultáneamente.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Conjuntos de propiedades definidos por el usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270564"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a>Conjuntos de propiedades DocumentSummaryInformation y UserDefined

Un **conjunto de propiedades DocumentSummaryInformation** y **UserDefined** es una extensión del [conjunto de propiedades Información de resumen](the-summary-information-property-set.md). Ambos conjuntos de propiedades pueden existir simultáneamente.

El nombre de la secuencia que contiene el conjunto de propiedades **DocumentSummaryInformation** es **\\ "005DocumentSummaryInformation".** El identificador de formato (FMTID) del conjunto de propiedades **DocumentSummaryInformation** es **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.

La declaración de este valor está disponible en los archivos de encabezado proporcionados como **FMTID \_ DocSummaryInformation**. Para obtener más información, vea [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [Format Identifiers](format-identifiers.md).

Esta secuencia también tiene una sección independiente para las propiedades personalizadas definidas por el usuario, como en los conjuntos de propiedades **DocumentSummaryInformation** y **UserDefined.** Esta sección aparece en la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) como un conjunto de propiedades independiente, con el siguiente FMTID (disponible como **FMTID \_ UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.

Estos dos conjuntos de propiedades son los únicos para los que una sola secuencia puede contener varios conjuntos de propiedades. El hecho de que estos dos conjuntos de propiedades estén en una sola secuencia afecta al comportamiento de la **interfaz IPropertySetStorage.** Para obtener más información, vea [**IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

En la tabla siguiente se enumeran las propiedades agregadas al conjunto de propiedades **DocumentSummaryInformation** y **UserDefined.** Al igual que en el conjunto de **propiedades SummaryInformation,** los nombres no suelen almacenarse en el conjunto de propiedades, sino que se deducen del identificador de propiedad.



| Nombre de propiedad      | Identificador de la propiedad     | Valor del identificador de propiedad | Tipo VARIANT                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| Category           | **PIDDSI \_ CATEGORY**    | 0x00000002                | **VT \_ LPSTR**                     |
| PresentationTarget | **\_PREFORMATO PIDDSI**  | 0x00000003                | **VT \_ LPSTR**                     |
| Bytes              | **PIDDSI \_ BYTECOUNT**   | 0x00000004                | **VT \_ I4**                        |
| Líneas              | **PIDDSI \_ LINECOUNT**   | 0x00000005                | **VT \_ I4**                        |
| Párrafos         | **PIDDSI \_ PARCOUNT**    | 0x00000006                | **VT \_ I4**                        |
| Diapositivas             | **PIDDSI \_ SLIDECOUNT**  | 0x00000007                | **VT \_ I4**                        |
| Notas              | **PIDDSI \_ NOTECOUNT**   | 0x00000008                | **VT \_ I4**                        |
| HiddenSlides       | **PIDDSI \_ HIDDENCOUNT** | 0x00000009                | **VT \_ I4**                        |
| MMClips            | **PIDDSI \_ MMCLIPCOUNT** | 0x0000000A                | **VT \_ I4**                        |
| ScaleCrop          | **ESCALA DE \_ PIDDSI**       | 0x0000000B                | **VT \_ BOOL**                      |
| HeadingPairs       | **ENCABEZADO \_ DE PIDDSIPAIR** | 0x0000000C                | **VT \_ VECTOR** \| **VT \_ VARIANT** |
| TitlesofParts      | **PIDDSI \_ DOCPARTS**    | 0x0000000D                | **VT \_ VECTOR** \| **VT \_ LPSTR**   |
| Manager            | **PIDDSI \_ MANAGER**     | 0x0000000E                | **VT \_ LPSTR**                     |
| Compañía            | **PIDDSI \_ COMPANY**     | 0x0000000F                | **VT \_ LPSTR**                     |
| LinksUpToDate      | **VÍNCULOS \_ PIDDSIDIRTY**  | 0x00000010                | **VT \_ BOOL**                      |



 

Estas propiedades tienen los siguientes usos:

<dl> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría
</dt> <dd>

Cadena de texto escrito por el usuario que indica a qué categoría pertenece el archivo (notación, propuesta, y así sucesivamente). Resulta útil para buscar archivos del mismo tipo.

</dd> <dt>

<span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget
</dt> <dd>

Formato de destino para presentación (35 mm, impresora, vídeo, y así sucesivamente).

</dd> <dt>

<span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes
</dt> <dd>

Número de bytes.

</dd> <dt>

<span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Líneas
</dt> <dd>

Número de líneas.

</dd> <dt>

<span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Párrafos
</dt> <dd>

Número de párrafos.

</dd> <dt>

<span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Diapositivas
</dt> <dd>

Número de diapositivas.

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notas
</dt> <dd>

Número de páginas que contienen notas.

</dd> <dt>

<span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides
</dt> <dd>

Número de diapositivas ocultas.

</dd> <dt>

<span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips
</dt> <dd>

Número de clips de sonido o vídeo.

</dd> <dt>

<span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop
</dt> <dd>

Se establece en True (-1) cuando se desea escalar la miniatura. Si no se establece, se desea recortar.

</dd> <dt>

<span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs
</dt> <dd>

Propiedad usada internamente que indica la agrupación de diferentes partes del documento y el número de elementos de cada grupo. Los títulos de las partes del documento se almacenan en la **propiedad TitlesofParts.** La **propiedad HeadingPairs** se almacena como un vector de variantes, en pares repetidos de **valores VT \_ LPSTR** (o **VT \_ LPWSTR)** y **VT \_ I4.** El **valor \_ LPSTR de VT** representa un nombre de encabezado y el valor VT **\_ I4** indica el recuento de partes del documento bajo ese encabezado.

</dd> <dt>

<span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts
</dt> <dd>

Nombres de elementos de documento.

</dd> <dt>

<span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Director
</dt> <dd>

Administrador del proyecto.

</dd> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Empresa
</dt> <dd>

Nombre de la compañía.

</dd> <dt>

<span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate
</dt> <dd>

Valor booleano para indicar si los vínculos personalizados se ve afectados por un ruido excesivo en todas las aplicaciones.

> [!Note]  
> Como se describe en la versión 12.3. Formato serializado para conjuntos de propiedades de la especificación de diseño OLE 2.0, los elementos vectoriales de las propiedades **HeadingPairs** y **TitlesofParts** deben alinearse en límites de 32 bits dentro del conjunto de propiedades. Sin embargo, en los conjuntos de propiedades **DocumentSummaryInformation** y **UserDefined,** cuando la página de códigos del conjunto de propiedades no es Unicode, estos elementos deben empaquetarse.

 

</dd> </dl>

El **conjunto de propiedades UserDefined** se puede usar para contener cualquier propiedad. Normalmente, se usa para almacenar las propiedades con nombre creadas por un usuario.

 

 




