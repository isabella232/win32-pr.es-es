---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Instancias de ScoredProperty anidadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1bfed09c48bc0ac6e93e09f96dc8116e8b0a91
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689691"
---
# <a name="nested-scoredproperty-instances"></a>Instancias de ScoredProperty anidadas

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Tenga en cuenta que no está restringido a la adición de instancias de ScoredProperty como elementos secundarios de una instancia de opción. Las instancias de ScoredProperty también se pueden anidar dentro de otras instancias de ScoredProperty. Esto resulta útil cuando una propiedad de dispositivo es compleja y se representa mejor mediante varias subpropiedades. Agregar subpropiedades a una propiedad (o pública) existente o ScoredProperty es una buena forma de mejorar una opción, a la vez que conserva la portabilidad con las instancias de opción existentes. Por ejemplo, las instancias de opción estándar de la característica MediaType contienen un ScoredProperty que describe el peso del medio como ligero, medio, pesado o extrapesado. Si desea obtener descripciones más precisas de la ponderación, puede Agregar una subpropiedad (GramsPer100Sheets en el ejemplo siguiente) que contenga el peso real (en gramos) de 100 hojas de medios. La opción mejorada podría ser similar a la del ejemplo siguiente.

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

Una comparación de las instancias de opciones originales y mejoradas genera una coincidencia casi perfecta, ya que la opción mejorada es un supraconjunto del original, y se conservan las ubicaciones y los valores de cada una de las instancias de ScoredProperty originales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



