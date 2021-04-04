---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076308"
---
# <a name="iagentballoongetnumcharsperline"></a><span data-ttu-id="e3024-103">IAgentBalloon::GetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="e3024-103">IAgentBalloon::GetNumCharsPerLine</span></span>

<span data-ttu-id="e3024-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3024-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

<span data-ttu-id="e3024-105">Recupera el valor para el promedio de caracteres por línea mostrado en un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="e3024-105">Retrieves the value for the average number of characters per line displayed in a word balloon.</span></span>

-   <span data-ttu-id="e3024-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3024-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e3024-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="e3024-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="e3024-108">Dirección de una variable que recibe el número de caracteres por línea.</span><span class="sxs-lookup"><span data-stu-id="e3024-108">The address of a variable that receives the number of characters per line.</span></span>

</dd> </dl>

<span data-ttu-id="e3024-109">El servidor de Microsoft Agent desplaza automáticamente las líneas que se muestran para la salida de voz en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="e3024-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="e3024-110">El número promedio de caracteres por línea para el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e3024-110">The average number of characters per line for a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e3024-111">No se puede cambiar por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e3024-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3024-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3024-112">See Also</span></span>

[<span data-ttu-id="e3024-113">**IAgentBalloon::GetNumLines**</span><span class="sxs-lookup"><span data-stu-id="e3024-113">**IAgentBalloon::GetNumLines**</span></span>](iagentballoon--getnumlines.md)


 

 




