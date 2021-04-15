---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714179"
---
# <a name="iagentballoongetfontitalic"></a><span data-ttu-id="931b4-103">IAgentBalloon::GetFontItalic</span><span class="sxs-lookup"><span data-stu-id="931b4-103">IAgentBalloon::GetFontItalic</span></span>

<span data-ttu-id="931b4-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="931b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

<span data-ttu-id="931b4-105">Indica si la fuente utilizada en un globo de palabras está en cursiva.</span><span class="sxs-lookup"><span data-stu-id="931b4-105">Indicates whether the font used in a word balloon is italic.</span></span>

-   <span data-ttu-id="931b4-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="931b4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="931b4-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span><span class="sxs-lookup"><span data-stu-id="931b4-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span></span>
</dt> <dd>

<span data-ttu-id="931b4-108">La dirección de un valor que recibe **true** si la fuente es cursiva y **false** si no está en cursiva.</span><span class="sxs-lookup"><span data-stu-id="931b4-108">The address of a value that receives **True** if the font is italic and **False** if not italic.</span></span>

</dd> </dl>

<span data-ttu-id="931b4-109">El estilo de fuente utilizado en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="931b4-109">The font style used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="931b4-110">No se puede cambiar por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="931b4-110">It cannot be changed by an application.</span></span> <span data-ttu-id="931b4-111">Sin embargo, el usuario puede invalidar la configuración de fuente para todos los caracteres a través de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="931b4-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




