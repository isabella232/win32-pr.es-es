---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cc462895ff9f19f7e722660608a268af13446f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120210"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="c6f76-103">IAgentBalloon::SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="c6f76-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="c6f76-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6f76-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="c6f76-105">Establece el juego de caracteres de la fuente que se muestra en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="c6f76-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="c6f76-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c6f76-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c6f76-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="c6f76-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="c6f76-108">Juego de caracteres de la fuente.</span><span class="sxs-lookup"><span data-stu-id="c6f76-108">The character set of the font.</span></span> <span data-ttu-id="c6f76-109">A continuación se muestra una configuración común para value:</span><span class="sxs-lookup"><span data-stu-id="c6f76-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="c6f76-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c6f76-110">Value</span></span>    | <span data-ttu-id="c6f76-111">Juego de caracteres</span><span class="sxs-lookup"><span data-stu-id="c6f76-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f76-112">0</span><span class="sxs-lookup"><span data-stu-id="c6f76-112">0</span></span>   | <span data-ttu-id="c6f76-113">Caracteres estándar de Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c6f76-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="c6f76-114">1</span><span class="sxs-lookup"><span data-stu-id="c6f76-114">1</span></span>   | <span data-ttu-id="c6f76-115">Juego de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c6f76-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="c6f76-116">2</span><span class="sxs-lookup"><span data-stu-id="c6f76-116">2</span></span>   | <span data-ttu-id="c6f76-117">Juego de caracteres de símbolo.</span><span class="sxs-lookup"><span data-stu-id="c6f76-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="c6f76-118">128</span><span class="sxs-lookup"><span data-stu-id="c6f76-118">128</span></span> | <span data-ttu-id="c6f76-119">Juego de caracteres de doble byte (DBCS) único para la versión japonesa de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6f76-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="c6f76-120">129</span><span class="sxs-lookup"><span data-stu-id="c6f76-120">129</span></span> | <span data-ttu-id="c6f76-121">Juego de caracteres de doble byte (DBCS) único para la versión en coreano de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6f76-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="c6f76-122">134</span><span class="sxs-lookup"><span data-stu-id="c6f76-122">134</span></span> | <span data-ttu-id="c6f76-123">Juego de caracteres de doble byte (DBCS) único para la versión en chino simplificado de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6f76-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="c6f76-124">136</span><span class="sxs-lookup"><span data-stu-id="c6f76-124">136</span></span> | <span data-ttu-id="c6f76-125">Juego de caracteres de doble byte (DBCS) único para la versión en chino tradicional de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6f76-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="c6f76-126">255</span><span class="sxs-lookup"><span data-stu-id="c6f76-126">255</span></span> | <span data-ttu-id="c6f76-127">Normalmente, las aplicaciones MS-DOS muestran caracteres extendidos.</span><span class="sxs-lookup"><span data-stu-id="c6f76-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="c6f76-128">Para otros valores de juego de caracteres, consulte la documentación del SDK de plataforma.</span><span class="sxs-lookup"><span data-stu-id="c6f76-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="c6f76-129">El juego de caracteres predeterminado utilizado en el globo de palabras de un carácter se define en el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c6f76-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="c6f76-130">Puede cambiarlo con [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span><span class="sxs-lookup"><span data-stu-id="c6f76-130">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="c6f76-131">Sin embargo, el usuario puede invalidar la configuración del juego de caracteres para todos los caracteres mediante la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c6f76-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="c6f76-132">Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c6f76-132">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6f76-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c6f76-133">See Also</span></span>

[<span data-ttu-id="c6f76-134">**IAgentBalloon::GetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="c6f76-134">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




