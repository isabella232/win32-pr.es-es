---
description: Contiene un párrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents. h)
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
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660157"
---
# <a name="paragraph-element"></a>Elemento Paragraph

Contiene un párrafo.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

[**Groupnode BizTalk**](groupnode-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**Línea**](line-element.md)

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="attributes"></a>Atributos



| Atributo       | Tipo                      | Obligatorio | Descripción                                                                             | Valores posibles           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**        | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)         | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**       | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height**      | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |
| **BlockNumber** | **xs:nonNegativeInteger** | Obligatorio | Número de bloque.                                                                           | Cualquier entero no negativo. |
| **LineNumber**  | **xs:nonNegativeInteger** | Obligatorio | Línea en la que comienza el párrafo.                                                 | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | [**ParagraphType**](paragraphtype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                      |
| Nombre del esquema  | Lector de diario                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Windows.ui.xaml.documents. h</dt> </dl> |



 

 




