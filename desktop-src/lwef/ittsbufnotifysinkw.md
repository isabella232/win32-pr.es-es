---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994530"
---
# <a name="ittsbufnotifysinkw"></a><span data-ttu-id="af893-103">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="af893-103">ITTSBufNotifySinkW</span></span>

<span data-ttu-id="af893-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af893-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="af893-105">El motor debe llamar a través del **marcador**.</span><span class="sxs-lookup"><span data-stu-id="af893-105">The engine must call out through **BookMark**.</span></span> <span data-ttu-id="af893-106">Durante el preprocesamiento de la salida de voz, el código del agente de Microsoft inserta marcadores entre "palabras" y usa la llegada de esos marcadores para impulsar el ritmo del texto del globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="af893-106">During preprocessing of speech output, Microsoft Agent code inserts bookmarks between "words" and uses the arrival of those bookmarks to drive the pacing of text in the word balloon.</span></span> <span data-ttu-id="af893-107">Aunque SAPI no requiere nada más que la llegada de esos marcadores en algún momento antes del final del utterance, los marcadores se deben devolver de forma relativamente puntual para admitir Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="af893-107">While SAPI does not require anything more than the arrival of those bookmarks at some time before the end of the utterance, the bookmarks must be returned in a relatively timely fashion to support Microsoft Agent.</span></span>

<span data-ttu-id="af893-108">Tenga en cuenta que no hay un concepto estricto de "Word" en algunos lenguajes, como el japonés.</span><span class="sxs-lookup"><span data-stu-id="af893-108">Note that there is no strict concept of "word" in some languages, such as Japanese.</span></span> <span data-ttu-id="af893-109">El método [**Speak**](speak-method.md) de Microsoft Agent define una "palabra" como una cadena de símbolos conectada que tiene un significado y una pronunciación aislada.</span><span class="sxs-lookup"><span data-stu-id="af893-109">Microsoft Agent's [**Speak**](speak-method.md) method defines a "word" as a connected string of symbols that has a meaning and pronunciation in isolation.</span></span> <span data-ttu-id="af893-110">El agente de Microsoft utiliza código de análisis bastante sencillo para determinar qué es una "palabra": busca símbolos separados por espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="af893-110">Microsoft Agent uses fairly simple parsing code to determine what a "word" is: it looks for symbols separated by white space.</span></span> <span data-ttu-id="af893-111">Por lo tanto, hay tres "palabras" en la cadena inglesa "The 101 Dalmatians": "The", "101" y "Dalmatians".</span><span class="sxs-lookup"><span data-stu-id="af893-111">Thus, there are three "words" in the English string "The 101 Dalmatians": "the", "one hundred and one", and "Dalmatians".</span></span> <span data-ttu-id="af893-112">El texto incluido en la etiqueta de mapa del agente de Microsoft se trata como una única "palabra" para la presentación.</span><span class="sxs-lookup"><span data-stu-id="af893-112">Text included in the Microsoft Agent Map tag is treated as a single "word" for display purposes.</span></span>

 

 




