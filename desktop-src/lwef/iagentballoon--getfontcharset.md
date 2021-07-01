---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120410"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="b6cf9-103">IAgentBalloon::GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="b6cf9-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="b6cf9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b6cf9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="b6cf9-105">Indica el juego de caracteres de la fuente que se muestra en un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="b6cf9-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b6cf9-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="b6cf9-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="b6cf9-108">Dirección de un valor que recibe el juego de caracteres de la fuente.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="b6cf9-109">A continuación se muestra una configuración común para value:</span><span class="sxs-lookup"><span data-stu-id="b6cf9-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="b6cf9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b6cf9-110">Value</span></span>    | <span data-ttu-id="b6cf9-111">Juego de caracteres</span><span class="sxs-lookup"><span data-stu-id="b6cf9-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6cf9-112">0</span><span class="sxs-lookup"><span data-stu-id="b6cf9-112">0</span></span>   | <span data-ttu-id="b6cf9-113">Caracteres estándar de Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b6cf9-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="b6cf9-114">1</span><span class="sxs-lookup"><span data-stu-id="b6cf9-114">1</span></span>   | <span data-ttu-id="b6cf9-115">Juego de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="b6cf9-116">2</span><span class="sxs-lookup"><span data-stu-id="b6cf9-116">2</span></span>   | <span data-ttu-id="b6cf9-117">Juego de caracteres de símbolo.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="b6cf9-118">128</span><span class="sxs-lookup"><span data-stu-id="b6cf9-118">128</span></span> | <span data-ttu-id="b6cf9-119">Juego de caracteres de doble byte (DBCS) único para la versión japonesa de Windows.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="b6cf9-120">129</span><span class="sxs-lookup"><span data-stu-id="b6cf9-120">129</span></span> | <span data-ttu-id="b6cf9-121">Juego de caracteres de doble byte (DBCS) único para la versión en coreano de Windows.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="b6cf9-122">134</span><span class="sxs-lookup"><span data-stu-id="b6cf9-122">134</span></span> | <span data-ttu-id="b6cf9-123">Juego de caracteres de doble byte (DBCS) único para la versión en chino simplificado de Windows.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="b6cf9-124">136</span><span class="sxs-lookup"><span data-stu-id="b6cf9-124">136</span></span> | <span data-ttu-id="b6cf9-125">Juego de caracteres de doble byte (DBCS) único para la versión en chino tradicional de Windows.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="b6cf9-126">255</span><span class="sxs-lookup"><span data-stu-id="b6cf9-126">255</span></span> | <span data-ttu-id="b6cf9-127">Normalmente, las aplicaciones MS-DOS muestran caracteres extendidos.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="b6cf9-128">Para otros valores de juego de caracteres, consulte la documentación del SDK de plataforma.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="b6cf9-129">El juego de caracteres predeterminado utilizado en el globo de palabras de un carácter se define en el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="b6cf9-130">Puede cambiarlo mediante [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span><span class="sxs-lookup"><span data-stu-id="b6cf9-130">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="b6cf9-131">Sin embargo, el usuario puede invalidar la configuración del juego de caracteres para todos los caracteres mediante la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b6cf9-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6cf9-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b6cf9-132">See Also</span></span>

[<span data-ttu-id="b6cf9-133">**IAgentBalloon::SetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="b6cf9-133">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




