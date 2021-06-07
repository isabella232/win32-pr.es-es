---
description: Contiene un conjunto de elementos&\# 8212; Paragraph, InkWord, Drawing, Text, Image o Flag&8212; que se agrupan en \# la nota del diario.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento GroupNode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432577"
---
# <a name="groupnode-element"></a>Elemento GroupNode

Contiene un conjunto de elementos ([**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md)o [**Flag)**](flag-element.md)que se agrupan en la nota del diario.

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

[**Imagen**](docimage-element.md)

[**Marca**](flag-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Requerido | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | [**GroupNodeType**](groupnodetype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                      |
| Nombre del esquema  | Lector de diario                                                  |



 

 

 



