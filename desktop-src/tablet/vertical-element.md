---
description: Contiene la información que describe el componente vertical de las líneas de la papelería utilizada por la nota de diario. Se usa, por ejemplo, cuando la nota tiene líneas de cuadrícula.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento Vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6f05ab8a2160dbf6b987177957e8285385fe4db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362910"
---
# <a name="vertical-element"></a>Elemento Vertical

Contiene la información que describe el componente vertical de las líneas de la papelería utilizada por la nota de diario. Se usa, por ejemplo, cuando la nota tiene líneas de cuadrícula.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos




| Atributo | Tipo | Obligatorio | Descripción | Valores posibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Estilo</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType | Obligatorio | Especifica el tipo de línea que se va a dibujar. | <ul><li>Ninguno</li><li>Sólido</li><li>Guión</li><li>Punto</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>Color</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType | Opcionales | Color del elemento. | Valor RGB hexadecimal. Coincide con la siguiente expresión regular: #[0-9a-zA-Z] {6} . Por ejemplo, #4a79B5.<br /> | 
| <strong>SpacingBefore</strong> | <strong>xs:nonNegativeInteger</strong> | Opcional | Espaciado delante del elemento . | Cualquier entero no negativo. | 
| <strong>SpacingBetween</strong> | <strong>xs:nonNegativeInteger</strong> | Opcionales | Espaciado entre este elemento y los elementos circundantes. | Cualquier entero no negativo. | 




 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                         |
|--------------|---------------------------------------------------------------|
| Tipo de elemento | [**VerticalType**](verticaltype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                    |
| Nombre del esquema  | Lector de diario                                                |



 

 

 




