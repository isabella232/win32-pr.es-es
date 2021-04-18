---
description: TAPI 3,1 presenta la noción de un terminal Multipista, un terminal que, en esencia, es una colección de &\# 0034; realiza un seguimiento de&\# 0034; terminales.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminales multipista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677476"
---
# <a name="multitrack-terminals"></a><span data-ttu-id="779c8-103">Terminales multipista</span><span class="sxs-lookup"><span data-stu-id="779c8-103">Multitrack Terminals</span></span>

<span data-ttu-id="779c8-104">TAPI 3,1 presenta la noción de un terminal Multipista, un terminal que, en esencia, es una colección de terminales de "pista".</span><span class="sxs-lookup"><span data-stu-id="779c8-104">TAPI 3.1 introduces the notion of a multitrack terminal, a terminal that, in essence, is a collection of "track" terminals.</span></span> <span data-ttu-id="779c8-105">Los terminales multipista facilitan la carga del programador en situaciones en las que varios flujos multimedia están implicados en una sesión de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="779c8-105">Multitrack terminals ease the programmer's load in situations where multiple media streams are involved in a communications session.</span></span>

<span data-ttu-id="779c8-106">El [terminal de grabación de archivos](file-playback-terminal-and-file-recording-terminal.md) es un ejemplo de un terminal multipista.</span><span class="sxs-lookup"><span data-stu-id="779c8-106">The [File Recording Terminal](file-playback-terminal-and-file-recording-terminal.md) is an example of a multitrack terminal.</span></span> <span data-ttu-id="779c8-107">Consta de "pistas", donde cada "Track" es un terminal que corresponde a una secuencia en el archivo grabado.</span><span class="sxs-lookup"><span data-stu-id="779c8-107">It consists of "tracks," where each "track" is a terminal corresponding to a stream in the recorded file.</span></span>

<span data-ttu-id="779c8-108">Un [terminal de seguimiento](track-terminals.md) puede ser otro terminal Multipista o un terminal de una sola pista.</span><span class="sxs-lookup"><span data-stu-id="779c8-108">A [track terminal](track-terminals.md) can be another multitrack terminal or a single-track terminal.</span></span> <span data-ttu-id="779c8-109">Un terminal de una sola pista es un terminal que no tiene terminales de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="779c8-109">A single-track terminal is a terminal that does not have any track terminals.</span></span> <span data-ttu-id="779c8-110">Un terminal de una sola pista es un terminal en el sentido TAPI 3 de la palabra.</span><span class="sxs-lookup"><span data-stu-id="779c8-110">A single-track terminal is a terminal in the TAPI 3 sense of the word.</span></span>

<span data-ttu-id="779c8-111">Para obtener más información acerca de los terminales Multipista, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="779c8-111">For more information about multitrack terminals, see the following topics:</span></span>

-   [<span data-ttu-id="779c8-112">Acerca de los terminales multipista</span><span class="sxs-lookup"><span data-stu-id="779c8-112">About Multitrack Terminals</span></span>](about-multitrack-terminals.md)
-   [<span data-ttu-id="779c8-113">Mecanismo de selección de terminal predeterminado</span><span class="sxs-lookup"><span data-stu-id="779c8-113">Default Terminal Selection Mechanism</span></span>](default-terminal-selection-mechanism.md)
-   [<span data-ttu-id="779c8-114">Selección de terminal manual</span><span class="sxs-lookup"><span data-stu-id="779c8-114">Manual Terminal Selection</span></span>](manual-terminal-selection.md)
-   [<span data-ttu-id="779c8-115">Usar terminales multipista y el mecanismo de selección predeterminado</span><span class="sxs-lookup"><span data-stu-id="779c8-115">Using Multitrack Terminals and the Default Selection Mechanism</span></span>](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



