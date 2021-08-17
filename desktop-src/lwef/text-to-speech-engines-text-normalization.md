---
title: Normalización de texto de motores de texto a voz
description: Normalización de texto de motores de texto a voz
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd195212d52d9107aa8112c156bfd8dd6b33d00d2161bec624d182f0f12f78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347925"
---
# <a name="text-to-speech-engines-text-normalization"></a>Normalización de texto de motores de texto a voz

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

La normalización es el proceso de identificar números, abreviaturas, acrónimos e idiomas y transformarlos en texto completo según sea necesario, normalmente en función del contexto de la frase.

Por ejemplo, mediante L&H TruVoice American English TTS Engine, la frase:

El padre Juan VI de Irlanda, fallecida el 6 de febrero de 1952.

se leerá en el **contexto normal** como:

   El padre Carlos V I de Francia, fallecida el seis de febrero, diecinueve cincuenta y dos.

Pero en **contexto de correo electrónico,** se leerá como:

   El sexto de Reino Unido, padre de Irlanda, fallecida el sexto de febrero, diecinueve cincuenta y dos.

Puede encontrar información sobre el uso **de la etiqueta De** voz de contexto en la documentación de programación del Agente [Etiquetas de salida de voz de Microsoft Agent](microsoft-agent-speech-output-tags.md).

 

 




