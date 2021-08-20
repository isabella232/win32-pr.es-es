---
description: Proporciona información (x, y) para los puntos inicial y final de la línea base de un párrafo en el documento journal. El espacio de coordenadas utilizado para estos valores es HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Elemento Baseline
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d97e5bd5aecf6833ef4e0bc5b3298442c911838ed714740448ae82305dd00eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118046199"
---
# <a name="baseline-element"></a>Elemento Baseline

Proporciona información (x, y) para los puntos inicial y final de la línea base de un párrafo en el documento journal. El espacio de coordenadas utilizado para estos valores es **HIMETRIC.**

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a>Elementos primarios

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Obligatorio | Descripción                                                      | Valores posibles           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Startx** | **xs:nonNegativeInteger** | Obligatorio | Valor X del punto que marca el principio de la línea base. | Cualquier entero no negativo. |
| **StartY** | **xs:nonNegativeInteger** | Obligatorio | Valor Y del punto que marca el principio de la línea base. | Cualquier entero no negativo. |
| **EndX**   | **xs:nonNegativeInteger** | Obligatorio | Valor X del punto que marca el final de la línea base.       | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|                  | Valor                                                         |
|------------------|---------------------------------------------------------------|
| **Tipo de elemento** | [**BaselineType**](baselinetype-complex-type.md) complexType |
| **Espacio de nombres**    | urn:schemas-microsoft-com:tabletpc:richink                    |
| **Nombre del esquema**  | Lector de diario                                                |



 

 

 



