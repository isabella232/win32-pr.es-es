---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486951"
---
# <a name="iagentballoonexsetnumlines"></a><span data-ttu-id="c6f80-103">IAgentBalloonEx::SetNumLines</span><span class="sxs-lookup"><span data-stu-id="c6f80-103">IAgentBalloonEx::SetNumLines</span></span>

<span data-ttu-id="c6f80-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6f80-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

<span data-ttu-id="c6f80-105">Establece el número de líneas de salida de texto que se pueden mostrar en el globo de palabras del carácter.</span><span class="sxs-lookup"><span data-stu-id="c6f80-105">Sets the number of lines of text output that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="c6f80-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c6f80-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="c6f80-107">Devuelve E \_ INVALIDARG si el valor del parámetro es cero.</span><span class="sxs-lookup"><span data-stu-id="c6f80-107">Returns E\_INVALIDARG if the parameter is zero.</span></span>

<dl> <dt>

<span data-ttu-id="c6f80-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span><span class="sxs-lookup"><span data-stu-id="c6f80-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span></span>
</dt> <dd>

<span data-ttu-id="c6f80-109">Número de líneas que se van a mostrar en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="c6f80-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="c6f80-110">El valor mínimo es 1 y el máximo es 128.</span><span class="sxs-lookup"><span data-stu-id="c6f80-110">The minimum setting is 1 and maximum is 128.</span></span> <span data-ttu-id="c6f80-111">Si el texto especificado en el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) supera el tamaño del globo actual, el agente desplaza automáticamente el texto del globo.</span><span class="sxs-lookup"><span data-stu-id="c6f80-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="c6f80-112">Este método producirá un error si se establece el bit de estilo de globo **SizeToText** .</span><span class="sxs-lookup"><span data-stu-id="c6f80-112">This method will fail if the **SizeToText** balloon style bit is set.</span></span>

<span data-ttu-id="c6f80-113">La configuración predeterminada se basa en la configuración cuando el carácter se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6f80-113">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6f80-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c6f80-114">See Also</span></span>

<span data-ttu-id="c6f80-115">[**IAgentBalloon:: GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx:: getStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx:: setStyle**](iagentballoonex--setstyle.md)</span><span class="sxs-lookup"><span data-stu-id="c6f80-115">[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)</span></span>


 

 




