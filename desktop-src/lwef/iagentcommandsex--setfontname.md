---
title: IAgentCommandsEx SetFontName
description: IAgentCommandsEx SetFontName
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773693"
---
# <a name="iagentcommandsexsetfontname"></a><span data-ttu-id="ce5e8-103">IAgentCommandsEx::SetFontName</span><span class="sxs-lookup"><span data-stu-id="ce5e8-103">IAgentCommandsEx::SetFontName</span></span>

<span data-ttu-id="ce5e8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ce5e8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

<span data-ttu-id="ce5e8-105">Establece la fuente mostrada en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="ce5e8-105">Sets the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="ce5e8-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ce5e8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ce5e8-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="ce5e8-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="ce5e8-108">BSTR que establece la fuente mostrada en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="ce5e8-108">A BSTR that sets the font displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="ce5e8-109">Esta propiedad determina la fuente usada para mostrar texto en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="ce5e8-109">This property determines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="ce5e8-110">El valor predeterminado de la configuración de fuente se basa en el valor de fuente de menú para la configuración de identificador de idioma del carácter, o bien, si no se establece, la configuración de identificador de idioma predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="ce5e8-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language ID setting.</span></span>

<span data-ttu-id="ce5e8-111">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="ce5e8-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce5e8-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ce5e8-112">See Also</span></span>

<span data-ttu-id="ce5e8-113">[**IAgentCommandsEx:: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: SetFontSize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="ce5e8-113">[**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




