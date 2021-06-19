---
description: Obtenga información sobre los elementos ParameterRef en el marco de esquema de impresión. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementos ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396530"
---
# <a name="parameterref-elements"></a>Elementos ParameterRef

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los elementos ParameterRef se aplican específicamente a los elementos Option, lo que permite que ese elemento Option haga referencia a un elemento ParameterDef determinado. Para estos elementos Option, un elemento ScoredProperty que caracteriza a Option no está codificado de forma segura en el documento PrintCapabilities como un valor, sino que es variable. Para habilitar esta variabilidad, estos elementos ScoredProperty contienen un elemento ParameterRef. Un elemento ScoredProperty no puede contener un elemento Value ni un elemento ParameterRef. Los elementos option que contienen uno o varios elementos ParameterRef se denominan elementos Option con parámetros.

El marco de esquema de impresión permite que un elemento Option contenga cualquier número de elementos ScoredProperty que hacen referencia a elementos Parameter, junto con cualquier número de elementos ScoredProperty que contengan elementos Value. El marco también permite que cualquier número de elementos Feature contenga elementos Option con parámetros, y se permite cualquier número de elementos Option con parámetros para cada elemento Feature. Además, se puede hacer referencia a la misma construcción de parámetros mediante varios elementos Option diferentes, elementos Option que pueden pertenecer al mismo elemento Feature o a otro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



