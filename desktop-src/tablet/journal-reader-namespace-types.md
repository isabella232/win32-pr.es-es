---
description: En esta sección se documenta los tipos XML utilizados por el componente Lector de diario.
ms.assetid: 08b45fe0-a505-4cc0-9791-764a87e8f1eb
title: Tipos de espacios de nombres de lector de diario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4951f1d87e62c94d7b78cb2ccfded5b9b059fd1c1175775e6f9b5e365b288269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883435"
---
# <a name="journal-reader-namespace-types"></a>Tipos de espacios de nombres de lector de diario

En esta sección se documenta los tipos XML utilizados por el componente Lector de diario.

## <a name="in-this-section"></a>En esta sección



| Tipo                                                                                  | Descripción                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternatesListType complexType**](alternateslisttype-complex-type.md)             | Define el tipo que contiene la lista de alternativas de reconocimiento para una palabra de entrada de lápiz.<br/>                                                                                                                  |
| [**BackgroundImageType complexType**](backgroundimagetype-complex-type.md)           | Define el tipo que contiene información sobre la imagen de fondo utilizada por la nota de diario, si existe.<br/>                                                                                                |
| [**BackgroundType complexType**](backgroundtype-complex-type.md)                     | Define el tipo que contiene la información en segundo plano de la nota de diario.<br/>                                                                                                                     |
| [**BaselineType complexType**](baselinetype-complex-type.md)                         | Define el tipo que contiene información sobre la línea base de un párrafo.<br/>                                                                                                                       |
| [BoundsType attributeGroup](boundstype-attributegroup.md)                            | Define un grupo de atributos utilizado por diversos elementos de un archivo XML de diario.<br/>                                                                                                             |
| [**ColorType simpleType**](colortype-simple-type.md)                                 | Define el tipo que se usa para especificar valores válidos para el color de determinados elementos de un archivo XML de diario.<br/>                                                                                      |
| [Grupo de contenido](contentgroup-group.md)                                          | Define el tipo que contiene un conjunto de contenido agrupado en una nota de diario.<br/>                                                                                                                          |
| [**ContentType complexType**](contenttype-complex-type.md)                           | Define el tipo que contiene algún tipo de contenido dentro de un archivo XML de diario.<br/>                                                                                                                      |
| [**ContentTypeType simpleType**](contenttypetype-simple-type.md)                     | Define el tipo que define los valores válidos para el **atributo Type** del elemento Content Lector [de \[ diario. \]](content-element--journal-reader.md)<br/>                                             |
| [**DrawingType complexType**](drawingtype-complex-type.md)                           | Define el tipo que contiene la entrada de lápiz clasificada por el motor de análisis de diario como un elemento [Drawing](drawing-element.md) (en lugar de un [elemento InkWord](inkword-element.md)).<br/>  |
| [**FlagType complexType**](flagtype-complex-type.md)                                 | Define el tipo que contiene la imagen binaria codificada y la información de posición de una marca incrustada en un documento de diario.<br/>                                                                         |
| [**GroupNodeType complexType**](groupnodetype-complex-type.md)                       | Define el tipo que contiene un conjunto de contenido agrupado en una nota de diario.<br/>                                                                                                                          |
| [**HorizontalType complexType**](horizontaltype-complex-type.md)                     | Define el tipo que contiene información sobre las líneas horizontales utilizadas por la papelería en una nota de diario.<br/>                                                                                         |
| [**ImageType complexType**](imagetype-complex-type.md)                               | Define el tipo que contiene la información binaria de una imagen en una nota de diario. Vea también [**BackgroundImageType complexType**](backgroundimagetype-complex-type.md).<br/>                     |
| [**InkWordType complexType**](inkwordtype-complex-type.md)                           | Define el tipo que contiene los datos de entrada de lápiz, las alternativas y la confianza para el contenido de entrada de lápiz que es un [elemento InkWord](inkword-element.md) (en lugar de un [elemento Drawing](drawing-element.md)).<br/> |
| [**JournalPageType complexType**](journalpagetype-complex-type.md)                   | Define el tipo que contiene una página individual en una nota de diario.<br/>                                                                                                                                |
| [**LineLayoutType complexType**](linelayouttype-complex-type.md)                     | Define el tipo que contiene información sobre las líneas que se usan en la papelería de una nota de diario determinada.<br/>                                                                                      |
| [**LineLayoutStyleType simpleType**](linelayoutstyletype-simple-type.md)             | Define los valores válidos para el **atributo Style** del [elemento LineLayout](linelayout-element.md).<br/>                                                                                           |
| [**LineType complexType**](linetype-complex-type.md)                                 | Define el tipo que contiene una línea de párrafo.<br/>                                                                                                                                                 |
| [**MarginType complexType**](margintype-complex-type.md)                             | Define el tipo que contiene los detalles sobre los márgenes de la nota de diario, como el estilo, el color y la posición.<br/>                                                                               |
| [**MarginTypeType simpleType**](margintypetype-simple-type.md)                       | Define el tipo que contiene valores válidos para el **atributo Type** para el [elemento Margin](margin-element.md).<br/>                                                                                |
| [**ParagraphType complexType**](paragraphtype-complex-type.md)                       | Define el tipo que contiene un párrafo en una nota de diario.<br/>                                                                                                                                          |
| [**ParagraphLineMetricsType complexType**](paragraphlinemetricstype-complex-type.md) | Define el tipo que contiene información sobre las métricas de línea de un párrafo, como la línea base.<br/>                                                                                             |
| [**ReflowType complexType**](reflowtype-complex-type.md)                             | Define el tipo que indica que el grupo se ha refluido.<br/>                                                                                                                                        |
| [**ScalarTransformType complexType**](scalartransformtype-complex-type.md)           | Define el tipo que contiene la información sobre cualquier transformación aplicada a la entrada de lápiz.<br/>                                                                                                                |
| [**StationeryType complexType**](stationerytype-complex-type.md)                     | Define el tipo que contiene la papelería utilizada por la nota de diario.<br/>                                                                                                                             |
| [**TextType complexType**](texttype-complex-type.md)                                 | Define el tipo que contiene el valor de texto de un [elemento Content Lector de \[ diario. \] ](content-element--journal-reader.md)<br/>                                                                       |
| [**TitleAreaType complexType**](titleareatype-complex-type.md)                       | Define el tipo que contiene información de posición y límites para el título en una nota de diario.<br/>                                                                                                     |
| [**TitleInfoType complexType**](titleinfotype-complex-type.md)                       | Define el tipo que contiene información sobre el título en una nota de diario.<br/>                                                                                                                       |
| [**TitleType complexType**](titletype-complex-type.md)                               | Define el tipo que contiene información de título para la nota de diario.<br/>                                                                                                                              |
| [**VerticalType complexType**](verticaltype-complex-type.md)                         | Define el tipo que contiene detalles sobre las líneas verticales usadas en la papelería de una nota de diario.<br/>                                                                                                |



 

 

 




