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
# <a name="text-to-speech-engines-text-normalization"></a><span data-ttu-id="854c5-103">Normalización del texto de los motores de conversión de texto a voz</span><span class="sxs-lookup"><span data-stu-id="854c5-103">Text-to-Speech Engines Text Normalization</span></span>

<span data-ttu-id="854c5-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="854c5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="854c5-105">La normalización es el proceso de identificar números, abreviaturas, acrónimos y idiomatics y transformarlos en texto completo según sea necesario, normalmente basado en el contexto de la oración.</span><span class="sxs-lookup"><span data-stu-id="854c5-105">Normalization is the process of identifying numbers, abbreviations, acronyms and idiomatics and transforming them into full text as needed, usually based on the context of the sentence.</span></span>

<span data-ttu-id="854c5-106">Por ejemplo, si usa&el motor de conversión de mayúsculas y minúsculas de TruVoice, la frase:</span><span class="sxs-lookup"><span data-stu-id="854c5-106">For example, using the L&H TruVoice American English TTS Engine, the sentence:</span></span>

<span data-ttu-id="854c5-107">King George VI de Inglaterra Falleci el 6 de febrero de 1952.</span><span class="sxs-lookup"><span data-stu-id="854c5-107">King George VI of England died on Feb 6, 1952.</span></span>

<span data-ttu-id="854c5-108">se leerán en **contexto normal** como:</span><span class="sxs-lookup"><span data-stu-id="854c5-108">will be read under **normal context** as:</span></span>

   <span data-ttu-id="854c5-109">Rey George V I de Inglaterra, muerto el seis de febrero de 19 52.</span><span class="sxs-lookup"><span data-stu-id="854c5-109">King George V I of England, died on February six, nineteen fifty-two.</span></span>

<span data-ttu-id="854c5-110">Pero en el **contexto de correo electrónico**, se leerá como:</span><span class="sxs-lookup"><span data-stu-id="854c5-110">But under **E-mail context**, it will be read as:</span></span>

   <span data-ttu-id="854c5-111">Rey George el sexto de Inglaterra, fallecido el sexto de febrero de 19 52.</span><span class="sxs-lookup"><span data-stu-id="854c5-111">King George the sixth of England, died on February sixth, nineteen fifty-two.</span></span>

<span data-ttu-id="854c5-112">Puede encontrar información sobre el uso de la etiqueta **Context** Speech en la documentación de programación del agente [etiquetas de salida de voz del agente de Microsoft](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="854c5-112">Information about using the **Context** speech tag can be found in the Agent programming documentation [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




