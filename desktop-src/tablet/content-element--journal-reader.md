---
description: Contiene el contenido de una página De diario.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Elemento Content [Lector de diario]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d544aebac1292a81c9a4acd05cb25da80977027e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478111"
---
# <a name="content-element-journal-reader"></a>Lector del diario \[ de elementos content\]

Contiene el contenido de una página De diario.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos primarios

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Dibujo**](drawing-element.md)

[**Texto**](text-element.md)

[**Imagen**](image-element.md)

[**Marca**](flag-element.md)

## <a name="attributes"></a>Atributos




| Atributo | Tipo | Requerido | Descripción | PossibleValues | 
|-----------|------|----------|-------------|----------------|
| <strong>Tipo</strong> | <a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a> | Requerido | Si el tipo es "Inert", no se puede modificar el contenido.<br /> | <ul><li>Normal</li><li>Inerte</li></ul> | 




 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | [**ContentType**](contenttype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Nombre del esquema  | Lector de diario                                              |



 

 

 




