---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definiciones de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5a71bfc5a5111a826b5d221ff1436ecf921dd2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279873"
---
# <a name="parameter-definitions"></a>Definiciones de parámetros

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En esta sección se describen las definiciones de parámetros públicos que pueden aparecer en un documento de PrintCapabilities.

Los parámetros se usan para describir un intervalo de valores aceptable, en lugar de una enumeración discreta de valores.

## <a name="parameterdef"></a>ParameterDef

Para obtener un resumen del tipo de elemento ParameterDef, consulte la sección [ParameterDef](parameterdef.md) .

Para obtener más información sobre la interacción entre los elementos ParameterDef y ParameterInit, consulte la sección [elementos ParameterDef y ParameterInit](./parameterdef-and-parameterinit-elements.md) .

Los elementos ParameterDef que se definen en las palabras clave del esquema de impresión deben estar totalmente definidos en un documento de PrintCapabilities.

## <a name="parameterref"></a>ParameterRef

Para obtener un resumen del tipo de elemento ParameterRef, consulte la sección [ParameterRef](parameterref.md) .

Una palabra clave de elemento configurable por el usuario puede contener una referencia a un parámetro. Los elementos ParameterRef se especifican como un elemento secundario de un elemento ScoredProperty para obtener más información, consulte la sección [elementos de referencia de parámetros](parameter-reference-elements.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
