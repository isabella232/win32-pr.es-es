---
description: Contiene un párrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432237"
---
# <a name="paragraph-element"></a>Elemento Paragraph

Contiene un párrafo.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**Línea**](line-element.md)

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>Atributos



| Atributo       | Tipo                      | Requerido | Descripción                                                                             | Valores posibles           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**        | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)         | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**       | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height**      | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite para el elemento.                                         | Cualquier entero no negativo. |
| **BlockNumber** | **xs:nonNegativeInteger** | Requerido | Número de bloque.                                                                           | Cualquier entero no negativo. |
| **LineNumber**  | **xs:nonNegativeInteger** | Requerido | Línea en la que comienza el párrafo.                                                 | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | [**ParagraphType**](paragraphtype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Nombre del esquema  | Lector de diario                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Windows.ui.xaml.documents.h</dt> </dl> |



 

 




