---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementos ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c0e145e99b1ee705d63449cf693c6fc87f6463
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104083602"
---
# <a name="parameterref-elements"></a>Elementos ParameterRef

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los elementos ParameterRef se aplican específicamente a los elementos Option, lo que permite que ese elemento OPTION haga referencia a un elemento ParameterDef determinado. Para estos elementos Option, un elemento ScoredProperty que caracteriza la opción no está codificado de forma rígida en el documento PrintCapabilities como un valor, sino que es variable. Para habilitar esta variabilidad, estos elementos ScoredProperty contienen un elemento ParameterRef. Un elemento ScoredProperty no puede contener un elemento Value y un elemento ParameterRef. Los elementos de opción que contienen uno o más elementos ParameterRef se denominan elementos de opción parametrizados.

El marco de trabajo de esquema de impresión permite que un elemento OPTION contenga cualquier número de elementos ScoredProperty que hagan referencia a elementos de parámetro, junto con cualquier número de elementos ScoredProperty que contengan elementos de valor. El marco de trabajo también permite que cualquier número de elementos de característica contengan elementos de opción parametrizados, y se permite cualquier número de elementos de opción con parámetros para cada elemento de característica. Además, se puede hacer referencia a la misma construcción de parámetro mediante varios elementos de opción diferentes, elementos de opción que pueden pertenecer a los mismos elementos de característica o a otros distintos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



