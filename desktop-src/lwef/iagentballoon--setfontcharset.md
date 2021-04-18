---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704785"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="bcadd-103">IAgentBalloon::SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="bcadd-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="bcadd-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bcadd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="bcadd-105">Establece el juego de caracteres de la fuente que se muestra en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="bcadd-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="bcadd-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bcadd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bcadd-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="bcadd-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="bcadd-108">Juego de caracteres de la fuente.</span><span class="sxs-lookup"><span data-stu-id="bcadd-108">The character set of the font.</span></span> <span data-ttu-id="bcadd-109">A continuación se muestran algunos valores de configuración comunes para el valor:</span><span class="sxs-lookup"><span data-stu-id="bcadd-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcadd-110">0</span><span class="sxs-lookup"><span data-stu-id="bcadd-110">0</span></span>   | <span data-ttu-id="bcadd-111">Caracteres estándar de Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bcadd-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="bcadd-112">1</span><span class="sxs-lookup"><span data-stu-id="bcadd-112">1</span></span>   | <span data-ttu-id="bcadd-113">Juego de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bcadd-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="bcadd-114">2</span><span class="sxs-lookup"><span data-stu-id="bcadd-114">2</span></span>   | <span data-ttu-id="bcadd-115">Juego de caracteres de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bcadd-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="bcadd-116">128</span><span class="sxs-lookup"><span data-stu-id="bcadd-116">128</span></span> | <span data-ttu-id="bcadd-117">Juego de caracteres de doble byte (DBCS) único para la versión en japonés de Windows.</span><span class="sxs-lookup"><span data-stu-id="bcadd-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="bcadd-118">129</span><span class="sxs-lookup"><span data-stu-id="bcadd-118">129</span></span> | <span data-ttu-id="bcadd-119">Juego de caracteres de doble byte (DBCS) único para la versión coreana de Windows.</span><span class="sxs-lookup"><span data-stu-id="bcadd-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="bcadd-120">134</span><span class="sxs-lookup"><span data-stu-id="bcadd-120">134</span></span> | <span data-ttu-id="bcadd-121">Juego de caracteres de doble byte (DBCS) único para la versión de chino simplificado de Windows.</span><span class="sxs-lookup"><span data-stu-id="bcadd-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="bcadd-122">136</span><span class="sxs-lookup"><span data-stu-id="bcadd-122">136</span></span> | <span data-ttu-id="bcadd-123">Juego de caracteres de doble byte (DBCS) único para la versión en chino tradicional de Windows.</span><span class="sxs-lookup"><span data-stu-id="bcadd-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="bcadd-124">255</span><span class="sxs-lookup"><span data-stu-id="bcadd-124">255</span></span> | <span data-ttu-id="bcadd-125">Caracteres extendidos que suelen mostrar las aplicaciones de MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="bcadd-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="bcadd-126">Para otros valores de juego de caracteres, consulte la documentación del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="bcadd-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="bcadd-127">El juego de caracteres predeterminado utilizado en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcadd-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="bcadd-128">Puede cambiarlo con [**IAgentBalloon:: SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span><span class="sxs-lookup"><span data-stu-id="bcadd-128">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="bcadd-129">Sin embargo, el usuario puede invalidar el valor del juego de caracteres para todos los caracteres mediante la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcadd-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="bcadd-130">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="bcadd-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcadd-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bcadd-131">See Also</span></span>

[<span data-ttu-id="bcadd-132">**IAgentBalloon::GetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="bcadd-132">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




