---
description: Las instancias de ScoredProperty también se pueden anidar dentro de otras instancias de ScoredProperty o como elementos secundarios de una instancia de Option.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Instancias scoredProperty anidadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a80d291fa59b2f36191f42b2f99ea9d22789a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408608"
---
# <a name="nested-scoredproperty-instances"></a>Instancias scoredProperty anidadas

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Tenga en cuenta que no está restringido a agregar instancias de ScoredProperty como elementos secundarios de una instancia de Option. Las instancias de ScoredProperty también se pueden anidar dentro de otras instancias de ScoredProperty. Esto resulta útil cuando una propiedad de dispositivo es compleja y se representa mejor mediante varias subpropiedades. Agregar subpropiedades a una propiedad existente (o pública) o ScoredProperty es una buena manera de mejorar una opción, al tiempo que se conserva la portabilidad con las instancias de option existentes. Por ejemplo, las instancias de opción estándar para la característica MediaType contienen una propiedad ScoredProperty que describe el peso del medio como Light, Medium, Heavy o ExtraHeavy. Si desea descripciones más precisas del peso, puede agregar una subpropiedad (GramsPer100Sheets en el ejemplo siguiente) que contenga el peso real (en gramas) de 100 hojas de medios. La opción mejorada podría ser como la del ejemplo siguiente.

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

Una comparación de las instancias de opción original y mejorada genera una coincidencia casi perfecta, porque la opción mejorada es un superconjunto del original y se conservan las ubicaciones y los valores de cada una de las instancias de ScoredProperty originales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



