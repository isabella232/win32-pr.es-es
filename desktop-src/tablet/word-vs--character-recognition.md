---
description: Al establecer la propiedad Factoid en None, el reconocedor de caracteres reconoce la escritura a mano carácter a carácter.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Diferencias entre Word y el reconocimiento de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f521b8abf1064ef87c5c79c3293e725c44190ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154182"
---
# <a name="word-vs-character-recognition"></a><span data-ttu-id="0e57d-103">Diferencias entre Word y el reconocimiento de caracteres</span><span class="sxs-lookup"><span data-stu-id="0e57d-103">Word vs. Character Recognition</span></span>

<span data-ttu-id="0e57d-104">Al establecer la propiedad [Factoid](/previous-versions/ms835848(v=msdn.10)) en **None**, el reconocedor de caracteres reconoce la escritura a mano carácter a carácter.</span><span class="sxs-lookup"><span data-stu-id="0e57d-104">By setting the [Factoid](/previous-versions/ms835848(v=msdn.10)) property to **None**, the character recognizer recognizes handwriting on a character-by-character basis.</span></span>

<span data-ttu-id="0e57d-105">La propiedad [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) en Automation) especifica el número de milisegundos de retraso entre el último [trazo](/previous-versions/ms552692(v=vs.100)) y el final de la entrada de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="0e57d-105">The [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) property specifies the number of milliseconds of delay between the last [Stroke](/previous-versions/ms552692(v=vs.100)) and the end of handwriting input.</span></span> <span data-ttu-id="0e57d-106">Puede aumentar este valor para reconocer texto antes de que se escriban palabras completas o oraciones.</span><span class="sxs-lookup"><span data-stu-id="0e57d-106">You can increase this value to recognize text before entire words or sentences are written.</span></span> <span data-ttu-id="0e57d-107">También puede forzar el reconocimiento de la tinta de inmediato mediante el método [Recognize](/previous-versions/ms836275(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="0e57d-107">You can also force the recognition of ink immediately by using the [Recognize](/previous-versions/ms836275(v=msdn.10)) method.</span></span>

 

 
