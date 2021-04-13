---
description: Contiene un conjunto de elementos&\# 8212; Paragraph, InkWord, Drawing, Text, Image o Flag&\# 8212; que se agrupan en la nota de Journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento Groupnode BizTalk
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648208"
---
# <a name="groupnode-element"></a>Elemento Groupnode BizTalk

Contiene un conjunto de elementos ([**paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md)o [**Flag**](flag-element.md)) que se agrupan en la nota de Journal.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

## <a name="child-elements"></a>Elementos secundarios

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Dibujo**](drawing-element.md)

[**Texto**](text-element.md)

[**Impresión**](docimage-element.md)

[**Marca**](flag-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Obligatorio | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | [**GroupNodeType**](groupnodetype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                      |
| Nombre del esquema  | Lector de diario                                                  |



 

 

 



