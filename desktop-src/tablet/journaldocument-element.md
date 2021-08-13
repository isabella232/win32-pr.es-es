---
description: Elemento de nivel superior de un archivo XML de nota de diario.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 738e5d8cfad1dd7b751877547d9b7b03c87feebdb4dbf8c3dbcbdcf719d87b2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442815"
---
# <a name="journaldocument-element"></a>Elemento JournalDocument

Elemento de nivel superior de un archivo XML de nota de diario.

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
| **Versión**           | **xs:string**             | Obligatorio | Versión del documento Journal representada en el archivo XML. | 1.0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | Obligatorio | Ancho predeterminado de la página para el documento Journal.          | Cualquier entero no negativo. |
| **DefaultPageHeight** | **xs:nonNegativeInteger** | Obligatorio | Alto predeterminado de la página para el documento Diario.         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|--------------------------------------------|
| Tipo de elemento | **JournalDocument**                        |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink |
| Nombre del esquema  | Lector de diario                             |



 

 

 



