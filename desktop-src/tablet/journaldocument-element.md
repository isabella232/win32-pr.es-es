---
description: El elemento de nivel superior de un archivo XML de notas de Journal.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546918"
---
# <a name="journaldocument-element"></a>Elemento JournalDocument

El elemento de nivel superior de un archivo XML de notas de Journal.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a>Elementos primarios

Ninguno.

## <a name="child-elements"></a>Elementos secundarios

[**Diseño de fondo**](stationery-element.md)

[**JournalPage**](journalpage-element.md)

## <a name="attributes"></a>Atributos



| Atributo             | Tipo                      | Obligatorio | Descripción                                                      | Valores posibles           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Versión**           | **xs:string**             | Obligatorio | Versión del documento de diario representada en el archivo XML. | 1,0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | Obligatorio | El ancho predeterminado de la página del documento de diario.          | Cualquier entero no negativo. |
| **DefaultPageHeight** | **xs:nonNegativeInteger** | Obligatorio | El alto predeterminado de la página del documento de diario.         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|              |                                            |
|--------------|--------------------------------------------|
| Tipo de elemento | **JournalDocument**                        |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink |
| Nombre del esquema  | Lector de diario                             |



 

 

 



