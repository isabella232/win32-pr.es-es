---
description: Proporciona información (x, y) para los puntos inicial y final de la línea base de un párrafo en el documento Journal. El espacio de coordenadas utilizado para estos valores es HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Elemento Baseline
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bc64f332608b4bd0281ae2a7f29db96101e9d2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579501"
---
# <a name="baseline-element"></a>Elemento Baseline

Proporciona información (x, y) para los puntos inicial y final de la línea base de un párrafo en el documento Journal. El espacio de coordenadas utilizado para estos valores es **HIMETRIC.**

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



|                  | Value                                                         |
|------------------|---------------------------------------------------------------|
| **Tipo de elemento** | [**BaselineType**](baselinetype-complex-type.md) complexType |
| **Espacio de nombres**    | urn:schemas-microsoft-com:tabletpc:richink                    |
| **Nombre del esquema**  | Lector de diario                                                |



 

 

 



