---
description: Un segmento de reconocimiento es la unidad de tinta básica que un reconocedor utiliza internamente para generar un resultado de reconocimiento para un objeto de entrada de lápiz determinado.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Segmentos de reconocimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707140"
---
# <a name="recognition-segments"></a><span data-ttu-id="db38a-103">Segmentos de reconocimiento</span><span class="sxs-lookup"><span data-stu-id="db38a-103">Recognition Segments</span></span>

<span data-ttu-id="db38a-104">Un segmento de reconocimiento es la unidad de tinta básica que un reconocedor utiliza internamente para generar un resultado de reconocimiento para un objeto de entrada de lápiz determinado.</span><span class="sxs-lookup"><span data-stu-id="db38a-104">A recognition segment is the basic ink unit that a recognizer uses internally to produce a recognition result for a particular Ink object.</span></span> <span data-ttu-id="db38a-105">Un segmento de reconocimiento es una colección de trazos de tinta.</span><span class="sxs-lookup"><span data-stu-id="db38a-105">A recognition segment is a collection of ink strokes.</span></span> <span data-ttu-id="db38a-106">Por ejemplo, un reconocedor que es capaz de reconocer escritura a mano cursiva en inglés podría usar una palabra como el segmento de reconocimiento básico.</span><span class="sxs-lookup"><span data-stu-id="db38a-106">For example, a recognizer that is capable of recognizing English cursive handwriting might use a word as the basic recognition segment.</span></span>

<span data-ttu-id="db38a-107">Otros reconocedores pueden usar partes de palabras compuestas como segmentos básicos.</span><span class="sxs-lookup"><span data-stu-id="db38a-107">Other recognizers may use parts of composite words as basic segments.</span></span> <span data-ttu-id="db38a-108">Por ejemplo, en español, las palabras cortas se combinan normalmente para proporcionar palabras compuestas más largas.</span><span class="sxs-lookup"><span data-stu-id="db38a-108">For example, in Spanish, short words are commonly combined to provide longer composite words.</span></span> <span data-ttu-id="db38a-109">"Damelo" es una palabra española que se compone de tres palabras "da me lo" (indíquelo), pero se escribe como una sola palabra.</span><span class="sxs-lookup"><span data-stu-id="db38a-109">"Damelo" is a Spanish word that is composed of three words "da me lo" (give me that), but it is written as a single word.</span></span> <span data-ttu-id="db38a-110">Un reconocedor de español podría reconocer cada subpalabra como un segmento.</span><span class="sxs-lookup"><span data-stu-id="db38a-110">A Spanish recognizer could recognize each subword as a segment.</span></span>

<span data-ttu-id="db38a-111">Un reconocedor puede encontrar varias maneras de dividir una muestra de entrada manuscrita en segmentos de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="db38a-111">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="db38a-112">Dado que la ambigüedad está implicada en el reconocimiento de la entrada prevista del usuario, el reconocedor puede devolver muchas coincidencias alternativas.</span><span class="sxs-lookup"><span data-stu-id="db38a-112">Because ambiguity is involved in recognizing the user's intended input, the recognizer can return many alternate matches.</span></span>

<span data-ttu-id="db38a-113">Para obtener más información acerca de los alternativos, vea [alternativas](alternates.md).</span><span class="sxs-lookup"><span data-stu-id="db38a-113">For more information about alternates, see [Alternates](alternates.md).</span></span>

 

 



