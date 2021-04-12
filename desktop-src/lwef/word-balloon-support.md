---
title: Compatibilidad con globos de palabras
description: Compatibilidad con globos de palabras
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268538"
---
# <a name="word-balloon-support"></a><span data-ttu-id="f6d36-103">Compatibilidad con globos de palabras</span><span class="sxs-lookup"><span data-stu-id="f6d36-103">Word Balloon Support</span></span>

<span data-ttu-id="f6d36-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6d36-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f6d36-105">La salida de voz también puede aparecer como una salida de texto en forma de globo de palabra animado.</span><span class="sxs-lookup"><span data-stu-id="f6d36-105">Spoken output can also appear as textual output in the form of a cartoon word balloon.</span></span> <span data-ttu-id="f6d36-106">Se puede utilizar para complementar la salida hablada de un carácter o como una alternativa a la salida de audio cuando se usa el método [**Speak**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d36-106">This can be used to supplement the spoken output of a character or as an alternative to audio output when you use the [**Speak**](speak-method.md) method.</span></span>

![sí, globo de palabra maestra](images/f3ballon.gif)

<span data-ttu-id="f6d36-108">También puede usar un globo de palabras para comunicar qué es un carácter "pensando" con el método de [**reflexión**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d36-108">You can also use a word balloon to communicate what a character is "thinking" using the [**Think**](think-method.md) method.</span></span> <span data-ttu-id="f6d36-109">Esto muestra el texto que se proporciona en un globo "pensamiento" todavía.</span><span class="sxs-lookup"><span data-stu-id="f6d36-109">This displays the text you supply in a still "thought" balloon.</span></span> <span data-ttu-id="f6d36-110">El método de **reflexión** también difiere del método [**Speak**](speak-method.md) en que no genera ninguna salida de audio.</span><span class="sxs-lookup"><span data-stu-id="f6d36-110">The **Think** method also differs from the [**Speak**](speak-method.md) method in that it produces no audio output.</span></span>

<span data-ttu-id="f6d36-111">Los globos de palabra solo admiten la comunicación con leyenda del carácter, no los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f6d36-111">Word balloons support only captioned communication from the character, not user input.</span></span> <span data-ttu-id="f6d36-112">Por lo tanto, el globo de palabras no admite controles de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6d36-112">Therefore, the word balloon does not support input controls.</span></span> <span data-ttu-id="f6d36-113">Sin embargo, puede proporcionar fácilmente datos proporcionados por el usuario para un carácter, mediante interfaces del lenguaje de programación u otros servicios de entrada proporcionados por el agente de Microsoft, como el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="f6d36-113">However, you can easily provide user input for a character, using interfaces from your programming language or the other input services provided by Microsoft Agent, such as the pop-up menu.</span></span>

<span data-ttu-id="f6d36-114">Al definir un carácter, puede especificar si desea incluir la compatibilidad con globos de palabras.</span><span class="sxs-lookup"><span data-stu-id="f6d36-114">When you define a character, you can specify whether to include word balloon support.</span></span> <span data-ttu-id="f6d36-115">Sin embargo, si usa un carácter que incluye compatibilidad con globos de palabras, no puede deshabilitar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="f6d36-115">However, if you use a character that includes word balloon support, you cannot disable the support.</span></span>

 

 




