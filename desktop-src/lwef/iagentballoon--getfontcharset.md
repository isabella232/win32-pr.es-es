---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f544df6c09fb00d346015b610751dd23738820
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268948"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="a91e9-103">IAgentBalloon::GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="a91e9-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="a91e9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a91e9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="a91e9-105">Indica el juego de caracteres de la fuente que se muestra en un globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="a91e9-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="a91e9-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a91e9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a91e9-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="a91e9-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="a91e9-108">Dirección de un valor que recibe el juego de caracteres de la fuente.</span><span class="sxs-lookup"><span data-stu-id="a91e9-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="a91e9-109">A continuación se muestran algunos valores de configuración comunes para el valor:</span><span class="sxs-lookup"><span data-stu-id="a91e9-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a91e9-110">0</span><span class="sxs-lookup"><span data-stu-id="a91e9-110">0</span></span>   | <span data-ttu-id="a91e9-111">Caracteres estándar de Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a91e9-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="a91e9-112">1</span><span class="sxs-lookup"><span data-stu-id="a91e9-112">1</span></span>   | <span data-ttu-id="a91e9-113">Juego de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a91e9-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="a91e9-114">2</span><span class="sxs-lookup"><span data-stu-id="a91e9-114">2</span></span>   | <span data-ttu-id="a91e9-115">Juego de caracteres de símbolos.</span><span class="sxs-lookup"><span data-stu-id="a91e9-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="a91e9-116">128</span><span class="sxs-lookup"><span data-stu-id="a91e9-116">128</span></span> | <span data-ttu-id="a91e9-117">Juego de caracteres de doble byte (DBCS) único para la versión en japonés de Windows.</span><span class="sxs-lookup"><span data-stu-id="a91e9-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="a91e9-118">129</span><span class="sxs-lookup"><span data-stu-id="a91e9-118">129</span></span> | <span data-ttu-id="a91e9-119">Juego de caracteres de doble byte (DBCS) único para la versión coreana de Windows.</span><span class="sxs-lookup"><span data-stu-id="a91e9-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="a91e9-120">134</span><span class="sxs-lookup"><span data-stu-id="a91e9-120">134</span></span> | <span data-ttu-id="a91e9-121">Juego de caracteres de doble byte (DBCS) único para la versión de chino simplificado de Windows.</span><span class="sxs-lookup"><span data-stu-id="a91e9-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="a91e9-122">136</span><span class="sxs-lookup"><span data-stu-id="a91e9-122">136</span></span> | <span data-ttu-id="a91e9-123">Juego de caracteres de doble byte (DBCS) único para la versión en chino tradicional de Windows.</span><span class="sxs-lookup"><span data-stu-id="a91e9-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="a91e9-124">255</span><span class="sxs-lookup"><span data-stu-id="a91e9-124">255</span></span> | <span data-ttu-id="a91e9-125">Caracteres extendidos que suelen mostrar las aplicaciones de MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="a91e9-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="a91e9-126">Para otros valores de juego de caracteres, consulte la documentación del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a91e9-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="a91e9-127">El juego de caracteres predeterminado utilizado en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a91e9-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a91e9-128">Puede cambiarlo mediante [**IAgentBalloon:: SetFontCharSet**](iagentballoon--setfontcharset.md).</span><span class="sxs-lookup"><span data-stu-id="a91e9-128">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="a91e9-129">Sin embargo, el usuario puede invalidar el valor del juego de caracteres para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a91e9-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="a91e9-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a91e9-130">See Also</span></span>

[<span data-ttu-id="a91e9-131">**IAgentBalloon::SetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="a91e9-131">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




