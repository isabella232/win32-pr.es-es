---
description: Representar atributos como construcciones de características o opciones o como parámetros. Este tema no está al día. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Representar atributos como construcciones de características o opciones o como parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a1d1923eb019ae1985b2000896389fa9c945b25430eda77e59e9c673d8ba9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091695"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a>Representar atributos como construcciones de características o opciones o como parámetros

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El autor de un documento PrintCapabilities define los atributos de dispositivo que la configuración. En el documento PrintCapabilities, el autor puede elegir representar un atributo de dispositivo como una construcción de característica o opción o como una construcción de parámetros.

Si un atributo de dispositivo tiene un número relativamente pequeño de estados posibles que no entran en ningún tipo de patrón obvio, una construcción característica/opción suele ser la mejor opción. Por ejemplo, si los valores permitidos para el atributo de dispositivo PageMediaSize son los valores Letter, Legal, A4ISO, Tabloid y Envelope10, una construcción característica/opción sería la mejor opción para la representación. Debido a la dificultad y ambigüedad asociadas a la expresión de los valores permitidos sin enumeración explícita, la construcción del parámetro no es adecuada para el atributo PageMediaSize.

Si un atributo de dispositivo se puede representar mediante un intervalo de enteros, la representación de parámetros suele ser la mejor opción, especialmente para los intervalos que incluyen muchos valores. Por ejemplo, si el atributo de dispositivo CopyCount para un modelo determinado de impresora puede oscilar entre 1 y 99 9999, este atributo se debe clasificar como un parámetro mediante la definición de una instancia parameterDef. Asigne valores a las instancias de propiedad estándar MinValue y MaxValue del elemento ParameterDef para definir el intervalo de valores para el atributo JobCopyCount. Debido al gran número de valores que se deben enumerar explícitamente como elementos Option, la representación Feature/Option no es adecuada para el atributo de dispositivo JobCopyCount.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



