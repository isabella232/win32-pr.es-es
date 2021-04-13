---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419109"
---
# <a name="iagentballoongetnumlines"></a><span data-ttu-id="45330-103">IAgentBalloon::GetNumLines</span><span class="sxs-lookup"><span data-stu-id="45330-103">IAgentBalloon::GetNumLines</span></span>

<span data-ttu-id="45330-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="45330-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

<span data-ttu-id="45330-105">Recupera el valor del número de líneas que se muestran en un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="45330-105">Retrieves the value of the number of lines displayed in a word balloon.</span></span>

-   <span data-ttu-id="45330-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="45330-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="45330-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span><span class="sxs-lookup"><span data-stu-id="45330-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span></span>
</dt> <dd>

<span data-ttu-id="45330-108">Dirección de una variable que recibe el número de líneas que se muestran.</span><span class="sxs-lookup"><span data-stu-id="45330-108">The address of a variable that receives the number of lines displayed.</span></span>

</dd> </dl>

<span data-ttu-id="45330-109">El servidor de Microsoft Agent desplaza automáticamente las líneas que se muestran para la salida de voz en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="45330-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="45330-110">El número de líneas de un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="45330-110">The number of lines for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="45330-111">No se puede cambiar por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="45330-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="45330-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="45330-112">See Also</span></span>

[<span data-ttu-id="45330-113">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="45330-113">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




