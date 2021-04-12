---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357565"
---
# <a name="iagentballoonexsetnumcharsperline"></a><span data-ttu-id="bee65-103">IAgentBalloonEx::SetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="bee65-103">IAgentBalloonEx::SetNumCharsPerLine</span></span>

<span data-ttu-id="bee65-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bee65-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

<span data-ttu-id="bee65-105">Establece el número de caracteres por línea que se pueden mostrar en el globo de palabras del carácter.</span><span class="sxs-lookup"><span data-stu-id="bee65-105">Sets the number of characters per line that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="bee65-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bee65-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="bee65-107">Devuelve E \_ INVALIDARG si el parámetro es menor que ocho.</span><span class="sxs-lookup"><span data-stu-id="bee65-107">Returns E\_INVALIDARG if the parameter is less than eight.</span></span>

<dl> <dt>

<span data-ttu-id="bee65-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="bee65-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="bee65-109">Número de líneas que se van a mostrar en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="bee65-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="bee65-110">El valor mínimo es 8 y el máximo es 255.</span><span class="sxs-lookup"><span data-stu-id="bee65-110">The minimum setting is 8 and the maximum is 255.</span></span> <span data-ttu-id="bee65-111">Si el texto especificado en el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) supera el tamaño del globo actual, el agente desplaza automáticamente el texto del globo.</span><span class="sxs-lookup"><span data-stu-id="bee65-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="bee65-112">La configuración predeterminada se basa en la configuración cuando el carácter se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bee65-112">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="bee65-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bee65-113">See Also</span></span>

[<span data-ttu-id="bee65-114">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="bee65-114">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




