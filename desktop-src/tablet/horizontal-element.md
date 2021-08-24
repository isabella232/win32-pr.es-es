---
description: Contiene información de formato para las líneas horizontales usadas para la papelería en una nota de diario.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b66e8557d73570ce1a0b7eb7217c02435c51a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482691"
---
# <a name="horizontal-element"></a>Elemento Horizontal

Contiene información de formato para las líneas horizontales usadas para la papelería en una nota de diario.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos




| Atributo | Tipo | Requerido | Descripción | Valores posibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Estilo</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType | Requerido | Especifica el tipo de línea que se va a dibujar. | <ul><li>Ninguno</li><li>Sólido</li><li>Guión</li><li>Punto</li><li>DashDot</li><li>DashDotDot</li><li>Doble</li></ul> | 
| <strong>Color</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType | Opcionales | Color del elemento. | Valor RGB hexadecimal. Coincide con la siguiente expresión regular: #[0-9a-zA-Z] {6} . Por ejemplo, #4a79B5.<br /> | 
| <strong>SpacingBefore</strong> | <strong>xs:nonNegativeInteger</strong> | Opcionales | Espaciado delante del elemento . | Cualquier entero no negativo. | 
| <strong>SpacingBetween</strong> | <strong>xs:nonNegativeInteger</strong> | Opcionales | Espaciado entre este elemento y los elementos circundantes. | Cualquier entero no negativo. | 




 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|-------------------------------------------------------------------|
| Tipo de elemento | [**HorizontalType complexType**](horizontaltype-complex-type.md) |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                        |
| Nombre del esquema  | Lector de diario                                                    |



 

 

 




