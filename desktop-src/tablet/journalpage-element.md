---
description: Contiene los detalles sobre una página individual en una nota de Journal.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911393"
---
# <a name="journalpage-element"></a>Elemento JournalPage

Contiene los detalles sobre una página individual en una nota de Journal.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos primarios

[**JournalDocument**](journaldocument-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**Inmóvil**](stationery-element.md)

[**DocImage**](docimage-element.md)

[**TitleInfo**](titleinfo-element.md)

[**Contenido**](content-element--journal-reader.md)

## <a name="attributes"></a>Atributos



| Atributo      | Tipo                      | Obligatorio | Descripción                                                                        | Valores posibles                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Number**     | **xs:nonNegativeInteger** | Obligatorio | Número ordinal de la página dentro del documento de diario, comenzando por uno (1). | Cualquier entero no negativo.                                |
| **Width**      | **xs:nonNegativeInteger** | Obligatorio | Ancho de la página.                                                             | Cualquier entero no negativo.                                |
| **Height**     | **xs:nonNegativeInteger** | Obligatorio | Alto de la página.                                                            | Cualquier entero no negativo.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Opcionales | Alto de la línea utilizada en la página.                                           | Cualquier entero no negativo.                                |
| **LanguageId** | **xs:nonNegativeInteger** | Opcionales | Identificador de idioma que se usa para la página.                                                 | Entero no negativo que representa un identificador de idioma válido. |



 

## <a name="element-information"></a>Información de elemento



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| Tipo de elemento | [**JournalPageType**](journalpagetype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                          |
| Nombre del esquema  | Lector de diario                                                      |



 

 

 



