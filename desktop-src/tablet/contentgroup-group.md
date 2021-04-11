---
description: Define un grupo que contiene un conjunto de contenido agrupado en una nota de Journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Grupo ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083012"
---
# <a name="contentgroup-group"></a>Grupo ContentGroup

Define un grupo que contiene un conjunto de contenido agrupado en una nota de Journal.

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

[**Groupnode BizTalk**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Dibujo**](drawing-element.md)

[**Texto**](text-element.md)

[**Impresión**](docimage-element.md)

[**Marca**](flag-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Obligatorio | Descripción                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento.<br/> | Cualquier número entero.<br/>              |
| **Top** (Principales)    | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.<br/>  | Cualquier número entero.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.<br/>                                          | Cualquier entero no negativo.<br/> |
| **Height** | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.<br/>                                         | Cualquier entero no negativo.<br/> |



 

## <a name="type-information"></a>Información de tipo



|             |                                            |
|-------------|--------------------------------------------|
| Espacio de nombres   | urn: schemas-microsoft-com: TabletPC: richink |
| Nombre del esquema | Lector de diario                             |



 

 

 




