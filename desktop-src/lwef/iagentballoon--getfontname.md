---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419112"
---
# <a name="iagentballoongetfontname"></a><span data-ttu-id="39fd0-103">IAgentBalloon::GetFontName</span><span class="sxs-lookup"><span data-stu-id="39fd0-103">IAgentBalloon::GetFontName</span></span>

<span data-ttu-id="39fd0-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="39fd0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

<span data-ttu-id="39fd0-105">Recupera el valor de la fuente mostrada en un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="39fd0-105">Retrieves the value for the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="39fd0-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="39fd0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="39fd0-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="39fd0-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="39fd0-108">Dirección de un BSTR que recibe el nombre de fuente mostrado en un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="39fd0-108">The address of a BSTR that receives the font name displayed in a word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="39fd0-109">La fuente predeterminada utilizada en un globo de palabras de caracteres se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39fd0-109">The default font used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="39fd0-110">Puede cambiarlo con [**IAgentBalloon:: SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span><span class="sxs-lookup"><span data-stu-id="39fd0-110">You can change it with [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span></span> <span data-ttu-id="39fd0-111">El usuario puede invalidar la configuración de fuente para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39fd0-111">The user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

 

 




