---
description: Proporciona información (x, y) de los puntos inicial y final de la línea de base de un párrafo en el documento de diario. El espacio de coordenadas usado para estos valores es HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Elemento Baseline
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275186"
---
# <a name="baseline-element"></a>Elemento Baseline

Proporciona información (x, y) de los puntos inicial y final de la línea de base de un párrafo en el documento de diario. El espacio de coordenadas usado para estos valores es **HIMETRIC**.

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
| **StartX** | **xs:nonNegativeInteger** | Obligatorio | Valor X del punto que marca el principio de la línea base. | Cualquier entero no negativo. |
| **Inicio** | **xs:nonNegativeInteger** | Obligatorio | Valor Y para el punto que marca el principio de la línea base. | Cualquier entero no negativo. |
| **EndX**   | **xs:nonNegativeInteger** | Obligatorio | Valor X del punto que marca el final de la línea base.       | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|              |                                                               |
|--------------|---------------------------------------------------------------|
| Tipo de elemento | [**BaselineType**](baselinetype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                    |
| Nombre del esquema  | Lector de diario                                                |



 

 

 



