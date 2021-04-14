---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: Opciones parametrizadas frente a opciones no parametrizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c1da2aba2515662be79da0c3831762de66463d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361968"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>Opciones parametrizadas frente a opciones no parametrizadas

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los proveedores de PrintCapabilities y PrintTicket deben controlar correctamente las instancias de la opción parametrizada durante el proceso de validación de PrintTicket. Como se describe en [definiciones de opciones](option-definitions.md), un paso que se realiza en la validación de PrintTicket es encontrar la opción en el documento de PrintCapabilities del dispositivo actual (la opción candidata) que mejor coincida con la opción especificada en PrintTicket (la opción de referencia). Cuando una o ambas instancias de opción tienen parámetros, hay tres casos posibles que debe controlar el proceso de puntuación definido por el controlador de dispositivo: el caso en el que ambas instancias de opción tienen parámetros y los dos casos en los que una opción está parametrizada y la otra no. En los siguientes casos se supone que hay una correspondencia entre las instancias de ScoredProperty con parámetros en la opción PrintTicket y un ScoredProperty determinado en la opción PrintCapabilities. Si no hay ninguna correspondencia, el proceso de puntuación puede tratar estas instancias de ScoredProperty de la misma manera que trata cualquier otra instancia de ScoredProperty no correspondiente.

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>Caso 1: opciones de documento de PrintTicket y PrintCapabilities con parámetros

En este caso, se parametrizan tanto la opción de referencia (en PrintTicket) como la opción candidata (en el documento de PrintCapabilities). Acceda a la instancia de ParameterDef a la que hace referencia la opción Candidate (en el documento de PrintCapabilities) y determine si el valor de ParameterInit especificado en el PrintTicket pertenece al intervalo permitido por la instancia de ParameterDef. Si es así, considere que esta ScoredProperty es una coincidencia. De lo contrario, este ScoredProperty no es una coincidencia.

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>Caso 2: opción de PrintTicket con parámetros, opción de documento de PrintCapabilities sin parámetros

En este caso, el PrintTicket contiene una característica con una opción parametrizada, mientras que la característica correspondiente en el documento de PrintCapabilities contiene al menos una opción que no tiene parámetros. Incluso si el documento de PrintCapabilities también contiene otras instancias de opción con parámetros, el proceso de puntuación debe aplicarse a cada opción, ya que el objetivo es identificar la mejor opción coincidente. El cliente debe ser capaz de comparar los candidatos de opción sin parámetros con una opción de referencia que está parametrizada.

Dado que la opción con parámetros aparece en el PrintTicket, las instancias de ParameterInit también deben estar presentes como se muestra en el caso anterior. El proceso de puntuación puede reemplazar simplemente cualquier instancia de ParameterRef de la opción parametrizada de PrintTicket por el valor especificado por la instancia de ParameterInit de PrintTicket. Esto convierte eficazmente una opción parametrizada en una que no tiene parámetros. En este momento se puede usar el proceso de coincidencia convencional.

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>Caso 3: opción de PrintTicket sin parámetros, opción de documento PrintCapabilities con parámetros

En este caso, la opción Reference de PrintTicket no tiene parámetros, mientras que la opción Candidate del documento PrintCapabilities tiene parámetros. Acceda a la instancia de ParameterDef en el documento de PrintCapabilities a la que hace referencia la instancia de ParameterRef de la opción candidata en el PrintTicket y determine si el valor definido en la opción de referencia del ScoredProperty correspondiente se encuentra en el intervalo permitido por la instancia de ParameterDef. Si es así, considere que esta ScoredProperty es una coincidencia. Si no es así, esta ScoredProperty no es una coincidencia.

Debe resaltarse que se determina el grado de coincidencia de dos instancias de opciones según el número (y la importancia) de las instancias de ScoredProperty que coinciden, independientemente de si las instancias de ScoredProperty contienen instancias de valor explícito o instancias de ParameterRef. Es posible que una opción candidata sea la mejor coincidencia, aunque contenga varias instancias de propiedad que no coincidan con las de la opción de referencia, o que no tengan ninguna propiedad correspondiente en la opción de referencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



