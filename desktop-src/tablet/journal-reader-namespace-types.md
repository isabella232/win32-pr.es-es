---
description: En esta sección se documentan los tipos XML utilizados por el componente lector de Journal.
ms.assetid: 08b45fe0-a505-4cc0-9791-764a87e8f1eb
title: Tipos de espacio de nombres del lector de Journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e8e3d812eea879ca9dd31680aa2834d6dfe50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277210"
---
# <a name="journal-reader-namespace-types"></a>Tipos de espacio de nombres del lector de Journal

En esta sección se documentan los tipos XML utilizados por el componente lector de Journal.

## <a name="in-this-section"></a>En esta sección



| Tipo                                                                                  | Descripción                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternatesListType complexType**](alternateslisttype-complex-type.md)             | Define el tipo que contiene la lista de alternativas de reconocimiento para una palabra de tinta.<br/>                                                                                                                  |
| [**BackgroundImageType complexType**](backgroundimagetype-complex-type.md)           | Define el tipo que contiene información sobre la imagen de fondo utilizada por la nota de Journal, si existe.<br/>                                                                                                |
| [**BackgroundType complexType**](backgroundtype-complex-type.md)                     | Define el tipo que contiene la información de fondo de la nota de Journal.<br/>                                                                                                                     |
| [**BaselineType complexType**](baselinetype-complex-type.md)                         | Define el tipo que contiene información sobre la línea de base de un párrafo.<br/>                                                                                                                       |
| [BoundsType attributeGroup](boundstype-attributegroup.md)                            | Define un grupo de atributos que se utiliza en una variedad de elementos de un archivo XML de diario.<br/>                                                                                                             |
| [**SimpleType de ColorType**](colortype-simple-type.md)                                 | Define el tipo que se utiliza para especificar los valores válidos para el color de determinados elementos de un archivo XML de diario.<br/>                                                                                      |
| [Grupo ContentGroup](contentgroup-group.md)                                          | Define el tipo que contiene un conjunto de contenido agrupado en una nota de Journal.<br/>                                                                                                                          |
| [**ComplexType de ContentType**](contenttype-complex-type.md)                           | Define el tipo que contiene alguna forma de contenido dentro de un archivo XML de diario.<br/>                                                                                                                      |
| [**SimpleType ContentTypeType**](contenttypetype-simple-type.md)                     | Define el tipo que define los valores válidos para el atributo de **tipo** del [ \[ lector \] de diario del elemento de contenido](content-element--journal-reader.md).<br/>                                             |
| [**DrawingType complexType**](drawingtype-complex-type.md)                           | Define el tipo que contiene la tinta que ha sido clasificada por el motor de análisis de diario como un [elemento de dibujo](drawing-element.md) (en oposición a un [elemento InkWord](inkword-element.md)).<br/>  |
| [**FlagType complexType**](flagtype-complex-type.md)                                 | Define el tipo que contiene la imagen binaria codificada y la información de posición de una marca insertada en un documento de diario.<br/>                                                                         |
| [**GroupNodeType complexType**](groupnodetype-complex-type.md)                       | Define el tipo que contiene un conjunto de contenido agrupado en una nota de Journal.<br/>                                                                                                                          |
| [**HorizontalType complexType**](horizontaltype-complex-type.md)                     | Define el tipo que contiene información sobre las líneas horizontales utilizadas por el diseño de fondo de una nota de Journal.<br/>                                                                                         |
| [**ImageType complexType**](imagetype-complex-type.md)                               | Define el tipo que contiene la información binaria de una imagen en una nota de Journal. Vea también el [**complexType BackgroundImageType**](backgroundimagetype-complex-type.md).<br/>                     |
| [**InkWordType complexType**](inkwordtype-complex-type.md)                           | Define el tipo que contiene los datos de tinta, alternativas y confianza para el contenido de la entrada de lápiz que es un [elemento InkWord](inkword-element.md) (en lugar de un [elemento de dibujo](drawing-element.md)).<br/> |
| [**JournalPageType complexType**](journalpagetype-complex-type.md)                   | Define el tipo que contiene una página individual en una nota de Journal.<br/>                                                                                                                                |
| [**LineLayoutType complexType**](linelayouttype-complex-type.md)                     | Define el tipo que contiene información sobre las líneas que se usan en el diseño de fondo de una nota de Journal determinada.<br/>                                                                                      |
| [**SimpleType LineLayoutStyleType**](linelayoutstyletype-simple-type.md)             | Define los valores válidos para el atributo de **estilo** del [elemento LineLayout](linelayout-element.md).<br/>                                                                                           |
| [**LineType complexType**](linetype-complex-type.md)                                 | Define el tipo que contiene una línea de párrafo.<br/>                                                                                                                                                 |
| [**MarginType complexType**](margintype-complex-type.md)                             | Define el tipo que contiene los detalles sobre los márgenes de la nota de Journal, como estilo, color y posición.<br/>                                                                               |
| [**SimpleType MarginTypeType**](margintypetype-simple-type.md)                       | Define el tipo que contiene los valores válidos para el atributo de **tipo** para el [elemento margin](margin-element.md).<br/>                                                                                |
| [**ParagraphType complexType**](paragraphtype-complex-type.md)                       | Define el tipo que contiene un párrafo en una nota de Journal.<br/>                                                                                                                                          |
| [**ParagraphLineMetricsType complexType**](paragraphlinemetricstype-complex-type.md) | Define el tipo que contiene información sobre las métricas de línea de un párrafo, como la línea de base.<br/>                                                                                             |
| [**ReflowType complexType**](reflowtype-complex-type.md)                             | Define el tipo que indica que se ha rebordado el grupo.<br/>                                                                                                                                        |
| [**ScalarTransformType complexType**](scalartransformtype-complex-type.md)           | Define el tipo que contiene la información sobre cualquier transformación aplicada a la entrada de lápiz.<br/>                                                                                                                |
| [**StationeryType complexType**](stationerytype-complex-type.md)                     | Define el tipo que contiene el diseño de fondo utilizado por la nota de Journal.<br/>                                                                                                                             |
| [**TextType complexType**](texttype-complex-type.md)                                 | Define el tipo que contiene el valor de texto en un [ \[ lector \] de diario de elementos de contenido](content-element--journal-reader.md).<br/>                                                                       |
| [**TitleAreaType complexType**](titleareatype-complex-type.md)                       | Define el tipo que contiene información de posición y de límites para el título de una nota de Journal.<br/>                                                                                                     |
| [**TitleInfoType complexType**](titleinfotype-complex-type.md)                       | Define el tipo que contiene información sobre el título en una nota de Journal.<br/>                                                                                                                       |
| [**TitleType complexType**](titletype-complex-type.md)                               | Define el tipo que contiene la información de título de la nota de Journal.<br/>                                                                                                                              |
| [**VerticalType complexType**](verticaltype-complex-type.md)                         | Define el tipo que contiene los detalles sobre las líneas verticales usadas en el diseño de fondo de una nota de Journal.<br/>                                                                                                |



 

 

 




