---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Representar atributos como construcciones de características/opciones o como parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104083600"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a>Representar atributos como construcciones de características/opciones o como parámetros

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El autor de un documento de PrintCapabilities define los atributos de dispositivo que componen la configuración. En el documento de PrintCapabilities, el autor puede elegir representar un atributo de dispositivo como una construcción de característica/opción o como una construcción de parámetro.

Si un atributo de dispositivo tiene un número relativamente pequeño de Estados posibles que no entran en ningún tipo de patrón obvio, una construcción de característica/opción suele ser la mejor opción. Por ejemplo, si los valores permitidos para el atributo de dispositivo PageMediaSize son los valores Letter, legal, A4ISO, tabloide y Envelope10, una construcción de característica/opción sería la mejor opción para la representación. Debido a la dificultad y la ambigüedad asociadas a la expresión de los valores permitidos sin enumeración explícita, la construcción del parámetro no es adecuada para el atributo PageMediaSize.

Si un atributo de dispositivo se puede representar mediante un intervalo de enteros, la representación de los parámetros suele ser la mejor opción, especialmente en el caso de los intervalos que incluyen muchos valores. Por ejemplo, si el atributo de dispositivo CopyCount para un modelo determinado de impresora puede oscilar entre 1 y 99.999, este atributo se debe clasificar como un parámetro, definiendo una instancia de ParameterDef. Asigne valores a las instancias de propiedad estándar MinValue y MaxValue del elemento ParameterDef para definir el intervalo de valores para el atributo JobCopyCount. Debido al gran número de valores que se deben enumerar explícitamente como elementos de opción, la representación de características y opciones no es adecuada para el atributo de dispositivo JobCopyCount.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



