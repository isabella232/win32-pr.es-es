---
description: Obtenga información sobre cómo PrintTicket e PrintCapabilities controlan las opciones parametrizadas y sin parámetros.
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: Opciones parametrizadas frente a opciones no parametrizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c788eaf2fa08f4f29a541a775d2bcbf523aa51
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407228"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>Opciones parametrizadas frente a opciones no parametrizadas

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los proveedores PrintCapabilities y PrintTicket deben controlar correctamente las instancias option parametrizadas durante el proceso de validación de PrintTicket. Como se describe en Definiciones de opciones [,](option-definitions.md)un paso realizado en la validación de PrintTicket es buscar la opción en el documento PrintCapabilities del dispositivo actual (la opción candidata) que mejor coincida con la opción especificada en PrintTicket (la opción de referencia). Cuando se parametrizan una o ambas instancias de Option, hay tres posibles casos que el proceso de puntuación definido por el controlador de dispositivo debe controlar: el caso en el que se parametrizan ambas instancias de Option y los dos casos en los que una opción tiene parámetros y la otra no. En los casos siguientes se supone que hay una correspondencia entre las instancias scoredProperty parametrizadas en la opción PrintTicket y una propiedad ScoredProperty determinada en la opción PrintCapabilities. Si no hay ninguna correspondencia, el proceso de puntuación puede tratar estas instancias de ScoredProperty de la misma manera que trata cualquier otra instancia de ScoredProperty que no sea de corrección.

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>Caso 1: Opciones de documento PrintTicket e PrintCapabilities parametrizadas

En este caso, se parametrizan tanto la opción de referencia (en PrintTicket) como la opción candidata (en el documento PrintCapabilities). Acceda a la instancia parameterDef a la que hace referencia la opción candidata (ambas en el documento PrintCapabilities) y determine si el valor ParameterInit especificado en PrintTicket se encuentra en el intervalo permitido por la instancia de ParameterDef. Si es así, considere que scoredProperty es una coincidencia. De lo contrario, scoredProperty no es una coincidencia.

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>Caso 2: opción PrintTicket parametrizada, opción de documento PrintCapabilities no parametrizada

En este caso, PrintTicket contiene una característica con una opción parametrizada, mientras que la característica correspondiente del documento PrintCapabilities contiene al menos una opción que no está parametrizada. Incluso si el documento PrintCapabilities también contiene otras instancias de Option con parámetros, el proceso de puntuación debe aplicarse a cada opción, ya que el objetivo es identificar la mejor opción de coincidencia. El cliente debe poder comparar candidatos de opción no parametrizada con una opción de referencia con parámetros.

Dado que la opción parametrizada aparece en PrintTicket, las instancias parameterInit también deben estar presentes como se muestra en el caso anterior. El proceso de puntuación simplemente puede reemplazar cualquier instancia parameterRef de la opción parametrizada de PrintTicket por el valor especificado por la instancia ParameterInit de PrintTicket. Esto convierte eficazmente una opción parametrizada en una que no está parametrizada. En este momento se puede usar el proceso de coincidencia convencional.

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>Caso 3: opción PrintTicket no parametrizada, opción de documento PrintCapabilities parametrizada

En este caso, la opción de referencia de PrintTicket no está parametrizada, mientras que la opción candidata del documento PrintCapabilities está parametrizada. Acceda a la instancia parameterDef del documento PrintCapabilities a la que hace referencia la instancia ParameterRef de la opción candidata en PrintTicket y determine si el valor definido en la opción de referencia para la scoredProperty correspondiente se encuentra dentro del intervalo permitido por la instancia de ParameterDef. Si es así, considere que scoredProperty es una coincidencia. Si no es así, ScoredProperty no es una coincidencia.

Debe destacarse que se realiza la determinación de la coincidencia de dos instancias de Option por el número (y la importancia) de las instancias scoredProperty que coinciden, independientemente de si las instancias scoredProperty contienen instancias value explícitas o instancias ParameterRef. Es posible que una opción candidata sea la mejor coincidencia, aunque contenga varias instancias de propiedad que no coincidan con las de la opción de referencia o que no tengan ninguna propiedad correspondiente en la opción de referencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



