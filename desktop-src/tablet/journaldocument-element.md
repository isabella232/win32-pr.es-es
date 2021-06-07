---
description: Elemento de nivel superior de un archivo XML de nota de diario.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432177"
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



| Atributo             | Tipo                      | Requerido | Descripción                                                      | Valores posibles           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Versión**           | **xs:string**             | Requerido | La versión del documento Journal representada en el archivo XML. | 1.0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | Requerido | Ancho predeterminado de la página para el documento Journal.          | Cualquier entero no negativo. |
| **DefaultPageHeight** | **xs:nonNegativeInteger** | Requerido | Alto predeterminado de la página para el documento Journal.         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|--------------------------------------------|
| Tipo de elemento | **JournalDocument**                        |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink |
| Nombre del esquema  | Lector de diario                             |



 

 

 



