---
description: Contiene los detalles de una página individual en una nota de diario.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5062838476e6f67605101157640a490645e454b62d852b69f51dc4bb2215db99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442805"
---
# <a name="journalpage-element"></a>Elemento JournalPage

Contiene los detalles de una página individual en una nota de diario.

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

[**Content**](content-element--journal-reader.md)

## <a name="attributes"></a>Atributos



| Atributo      | Tipo                      | Obligatorio | Descripción                                                                        | Valores posibles                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Number**     | **xs:nonNegativeInteger** | Obligatorio | Número ordinal de la página dentro del documento Journal, empezando por uno (1). | Cualquier entero no negativo.                                |
| **Width**      | **xs:nonNegativeInteger** | Obligatorio | Ancho de la página.                                                             | Cualquier entero no negativo.                                |
| **Height**     | **xs:nonNegativeInteger** | Obligatorio | Alto de la página.                                                            | Cualquier entero no negativo.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Opcionales | Alto de la línea utilizada en la página.                                           | Cualquier entero no negativo.                                |
| **Languageid** | **xs:nonNegativeInteger** | Opcionales | Identificador de idioma usado para la página.                                                 | Entero no negativo que representa un identificador de idioma válido. |



 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|---------------------------------------------------------------------|
| Tipo de elemento | [**JournalPageType**](journalpagetype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                          |
| Nombre del esquema  | Lector de diario                                                      |



 

 

 



