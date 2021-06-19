---
description: Obtenga información sobre las definiciones de parámetros en un documento PrintCapabilities. Este tema no está actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definiciones de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc8ad2bed3a972202bc0a5bb07cbdd4ef9d8f44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396580"
---
# <a name="parameter-definitions"></a>Definiciones de parámetros

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En esta sección se describen las definiciones de parámetros públicos que pueden aparecer en un documento PrintCapabilities.

Los parámetros se usan para describir un intervalo aceptable de valores, en lugar de una enumeración discreta de valores.

## <a name="parameterdef"></a>ParameterDef

Para obtener un resumen del tipo de elemento ParameterDef, consulte la [sección ParameterDef.](parameterdef.md)

Para obtener más información sobre la interacción entre los elementos ParameterDef y los elementos ParameterInit, consulte la sección [ParameterDef y ParameterInit Elements.](./parameterdef-and-parameterinit-elements.md)

Los elementos ParameterDef que se definen en las palabras clave de esquema de impresión deben estar totalmente definidos en un documento PrintCapabilities.

## <a name="parameterref"></a>ParameterRef

Para obtener un resumen del tipo de elemento ParameterRef, consulte la [sección ParameterRef.](parameterref.md)

Una palabra clave de elemento configurable por el usuario puede contener una referencia a un parámetro . Los elementos ParameterRef se especifican como elementos secundarios de un elemento ScoredProperty. Para más información, consulte la sección [Elementos de referencia de](parameter-reference-elements.md) parámetros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
