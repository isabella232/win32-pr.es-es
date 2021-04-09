---
title: Requisitos para los motores de reconocimiento de voz
description: Requisitos para los motores de reconocimiento de voz
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994479"
---
# <a name="requirements-for-speech-recognition-engines"></a><span data-ttu-id="86597-103">Requisitos para los motores de reconocimiento de voz</span><span class="sxs-lookup"><span data-stu-id="86597-103">Requirements for Speech Recognition Engines</span></span>

<span data-ttu-id="86597-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="86597-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="86597-105">Un motor de reconocimiento de voz también debe ser un motor de controles y comandos totalmente compatible (C&C) según SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="86597-105">A speech recognition engine must also be a fully compliant Command and Control (C&C) engine according to SAPI 4.0.</span></span> <span data-ttu-id="86597-106">Debe admitir varias gramáticas en el formato binario que se describe en la especificación y permitir que dichas gramáticas se activen o desactiven en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="86597-106">It must support multiple grammars in the binary format described in the specification and allow those grammars to be activated or deactivated in real time.</span></span>

<span data-ttu-id="86597-107">Tenga en cuenta que SAPI 4,0 requiere que los motores de reconocimiento de voz admitan las interfaces Unicode de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="86597-107">Note that SAPI 4.0 requires that speech recognition engines support the wide character, Unicode interfaces.</span></span> <span data-ttu-id="86597-108">Sin embargo, para admitir estas interfaces, el motor no debe depender de la conversión de datos Unicode a ANSI, ya que es posible que el motor no funcione correctamente en algunos sistemas.</span><span class="sxs-lookup"><span data-stu-id="86597-108">However, in supporting these interfaces, the engine should not depend on converting Unicode data to ANSI, as the engine may not function correctly on some systems.</span></span> <span data-ttu-id="86597-109">Por ejemplo, un motor japonés que convierte Unicode en ANSI podría no funcionar en un sistema de Microsoft Windows 95 en inglés.</span><span class="sxs-lookup"><span data-stu-id="86597-109">For example, a Japanese engine that converts Unicode to ANSI may not work on an English-language Microsoft Windows 95 system.</span></span>

<span data-ttu-id="86597-110">Además, para que se considere conforme a Microsoft Agent, el motor debe devolver los objetos de resultados tras el reconocimiento correcto de una frase (a través de ISRGramNotifySinkW::P hraseFinish).</span><span class="sxs-lookup"><span data-stu-id="86597-110">In addition, to be considered Microsoft Agent-compliant, the engine must return results objects upon the successful recognition of a phrase (through ISRGramNotifySinkW::PhraseFinish).</span></span> <span data-ttu-id="86597-111">Estos objetos de resultados deben admitir ISRResBasic, como requiere la especificación.</span><span class="sxs-lookup"><span data-stu-id="86597-111">These results objects must support ISRResBasic, as the specification requires.</span></span> <span data-ttu-id="86597-112">Además, deben admitir ISRResScore.</span><span class="sxs-lookup"><span data-stu-id="86597-112">In addition, they should support ISRResScore.</span></span> <span data-ttu-id="86597-113">Aunque el agente de Microsoft se ejecutará con un motor que solo admita ISRResBasic, o incluso con un motor que no devuelva ningún objeto de resultados, el rendimiento suele ser mucho más pobre con dichos motores.</span><span class="sxs-lookup"><span data-stu-id="86597-113">Although Microsoft Agent will run with an engine that supports only ISRResBasic, or even with an engine that returns no results objects whatsoever, performance will usually be significantly poorer with such engines.</span></span> <span data-ttu-id="86597-114">Muchas aplicaciones usan los valores de confianza proporcionados por el motor para controlar cómo responden a varios comandos.</span><span class="sxs-lookup"><span data-stu-id="86597-114">Many applications use the confidence values provided by the engine to control how they respond to various commands.</span></span>

 

 




