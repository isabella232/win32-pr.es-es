---
description: Define un grupo que contiene un conjunto de contenido agrupado en una nota de diario.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Grupo contentgroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432617"
---
# <a name="contentgroup-group"></a>Grupo contentgroup

Define un grupo que contiene un conjunto de contenido agrupado en una nota de diario.

## <a name="definition"></a>Definición

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Elementos secundarios

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Dibujo**](drawing-element.md)

[**Texto**](text-element.md)

[**Imagen**](docimage-element.md)

[**Marca**](flag-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Requerido | Descripción                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento.<br/> | Cualquier número entero.<br/>              |
| **Top** (Principales)    | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.<br/>  | Cualquier número entero.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite para el elemento.<br/>                                          | Cualquier entero no negativo.<br/> |
| **Height** | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite para el elemento.<br/>                                         | Cualquier entero no negativo.<br/> |



 

## <a name="type-information"></a>Información de tipo



|  Elemento     | Value                                                     |
|-------------|--------------------------------------------|
| Espacio de nombres   | urn:schemas-microsoft-com:tabletpc:richink |
| Nombre del esquema | Lector de diario                             |



 

 

 




