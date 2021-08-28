---
description: Contiene información de título sobre la nota de diario.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05661be8566cf4136194af4e08d8f9774d3413dc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473141"
---
# <a name="title-element"></a>Elemento Title

Contiene información de título sobre la nota de diario.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Diseño de fondo**](stationery-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**TitleArea**](titlearea-element.md)

## <a name="attributes"></a>Atributos




| Atributo | Tipo | Requerido | Descripción | Valores posibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Estilo</strong> | <strong>xs:string</strong> | Requerido | Especifica el tipo de borde que rodea el título de la nota. | <ul><li>Ninguno</li><li>SolidSquare</li><li>OutlineSquare</li><li>SolidRoundRect</li><li>OutlineRoundRect</li><li>SolidRoundRectDottedBaseline</li></ul> | 
| <strong>DateStyle</strong> | <strong>xs:string</strong> | Requerido | Define si el título incluye una fecha o no. | <ul><li>Ninguno</li><li>Short</li></ul> | 
| <strong>Color</strong> | <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a> | Opcionales | Especifica el color del fondo. | Vea <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>. | 




 

## <a name="element-information"></a>Información de elemento



| Elemento      | Value                                                   |
|--------------|---------------------------------------------------------|
| Tipo de elemento | [**TitleType**](titletype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink              |
| Nombre del esquema  | Lector de diario                                          |



 

 

 



