---
description: Contiene contenido clasificado por el analizador o el usuario como un dibujo.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Elemento Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44eab0f9feec4b80369a365663917ca1aea0f211bba70dd4b99e9161316c662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936595"
---
# <a name="drawing-element"></a>Elemento Drawing

Contiene contenido clasificado por el analizador o el usuario como un dibujo.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**ScalarTransform**](scalartransform-element.md)

[**CanReClassify**](canreclassify-element.md)

[**InkClass**](inkclass-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Requerido | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | [**DrawingType**](drawingtype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Nombre del esquema  | Lector de diario                                              |



 

 

 



