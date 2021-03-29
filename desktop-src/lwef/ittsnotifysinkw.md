---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420337"
---
# <a name="ittsnotifysinkw"></a><span data-ttu-id="a96a9-103">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="a96a9-103">ITTSNotifySinkW</span></span>

<span data-ttu-id="a96a9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a96a9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a96a9-105">El motor debe llamar a a través de [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)y [**Visual**](https://www.bing.com/search?q=**Visual**).</span><span class="sxs-lookup"><span data-stu-id="a96a9-105">The engine must call out through [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**), and [**Visual**](https://www.bing.com/search?q=**Visual**).</span></span> <span data-ttu-id="a96a9-106">La devolución de llamada **Visual** debe proporcionar IPA fonemas.</span><span class="sxs-lookup"><span data-stu-id="a96a9-106">The **Visual** callback must provide IPA phonemes.</span></span> <span data-ttu-id="a96a9-107">(El alfabeto \[ fonético internacional IPA \] es una notación universal para describir el contenido fonético de la comunicación oral.</span><span class="sxs-lookup"><span data-stu-id="a96a9-107">(The International Phonetic Alphabet \[IPA\] is a universal notation for describing the phonetic content of spoken communication.</span></span> <span data-ttu-id="a96a9-108">Todos los fonemas que se hablan tienen representaciones en IPA.</span><span class="sxs-lookup"><span data-stu-id="a96a9-108">All speakable phonemes have representations in IPA.</span></span> <span data-ttu-id="a96a9-109">Los detalles de IPA se encuentran en la parte especificación de Microsoft Speech API \[ de la descarga de Speech SDK 4,0 \] en [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)</span><span class="sxs-lookup"><span data-stu-id="a96a9-109">Details of IPA are in the Microsoft Speech API specification \[part of the Speech SDK 4.0 download\] at [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx).)</span></span>

<span data-ttu-id="a96a9-110">Aunque la notificación [**Visual**](https://www.bing.com/search?q=**Visual**) es bastante enriquecida, Microsoft Agent solo usa el valor **cIPAPhoneme** para animar la boca a medida que el carácter habla.</span><span class="sxs-lookup"><span data-stu-id="a96a9-110">Although the [**Visual**](https://www.bing.com/search?q=**Visual**) notification is fairly rich, Microsoft Agent uses only the **cIPAPhoneme** value to animate the mouth as the character speaks.</span></span> <span data-ttu-id="a96a9-111">Cualquier motor compatible con agente de Microsoft debe proporcionar un flujo muy sincronizado de notificaciones **visuales** que reflejen el contenido fonético del utterance generado.</span><span class="sxs-lookup"><span data-stu-id="a96a9-111">Any Microsoft Agent-compatible engine must provide a closely synchronized stream of **Visual** notifications reflecting the phonetic content of the produced utterance.</span></span> <span data-ttu-id="a96a9-112">En este caso, "notificación relativamente puntual" no es adecuado, ya que los hablantes de los oradores son bastante sensibles a las discrepancias entre la posición de la boca y el contenido acústico.</span><span class="sxs-lookup"><span data-stu-id="a96a9-112">In this case, "relatively timely notification" is not adequate, because speaker-hearers are fairly sensitive to discrepancies between mouth position and acoustic content.</span></span> <span data-ttu-id="a96a9-113">Las notificaciones **visuales** deben devolverse rápidamente.</span><span class="sxs-lookup"><span data-stu-id="a96a9-113">**Visual** notifications need to be returned promptly.</span></span>

 

 




