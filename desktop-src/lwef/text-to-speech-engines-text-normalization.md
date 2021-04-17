---
title: Normalización del texto de los motores de conversión de texto a voz
description: Normalización del texto de los motores de conversión de texto a voz
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7bda7cb8041e31ef8e741df4d3f5d807610f1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704647"
---
# <a name="text-to-speech-engines-text-normalization"></a>Normalización del texto de los motores de conversión de texto a voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

La normalización es el proceso de identificar números, abreviaturas, acrónimos y idiomatics y transformarlos en texto completo según sea necesario, normalmente basado en el contexto de la oración.

Por ejemplo, si usa&el motor de conversión de mayúsculas y minúsculas de TruVoice, la frase:

King George VI de Inglaterra Falleci el 6 de febrero de 1952.

se leerán en **contexto normal** como:

   Rey George V I de Inglaterra, muerto el seis de febrero de 19 52.

Pero en el **contexto de correo electrónico**, se leerá como:

   Rey George el sexto de Inglaterra, fallecido el sexto de febrero de 19 52.

Puede encontrar información sobre el uso de la etiqueta **Context** Speech en la documentación de programación del agente [etiquetas de salida de voz del agente de Microsoft](microsoft-agent-speech-output-tags.md).

 

 




