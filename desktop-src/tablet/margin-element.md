---
description: Define las líneas de margen dibujadas en la página.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c264c2470d070353d1fd19340a161cf765bc05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579421"
---
# <a name="margin-element"></a>Elemento Margin

Define las líneas de margen dibujadas en la página.

## <a name="definition"></a>Definición

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Elementos primarios

Ninguno.

## <a name="child-elements"></a>Elementos secundarios

Ninguno..

## <a name="attributes"></a>Atributos




| Atributo | Tipo | Obligatorio | Descripción | Valores posibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Estilo</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType | Obligatorio | Especifica el tipo de línea que se va a dibujar. | <ul><li>None</li><li>Sólido</li><li>Guión</li><li>Punto</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>Color</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType | Opcional | Color del elemento. | Valor RGB hexadecimal. Coincide con la siguiente expresión regular: #[0-9a-zA-Z] {6} . Por ejemplo, #4a79B5.<br /> | 
| <strong>Tipo</strong> | <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType | Opcional | Indica el margen izquierdo o derecho. | <ul><li>Left</li><li>Right</li></ul> | 
| <strong>Espaciado</strong> | <strong>xs:nonNegativeInteger</strong> | Opcional | Espaciado entre el borde de la página y el margen. | Cualquier entero no negativo. | 




 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|-----------------------------------------------------------|
| Tipo de elemento | [**MarginType**](margintype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                |
| Nombre del esquema  | Lector de diario                                            |



 

 

 




