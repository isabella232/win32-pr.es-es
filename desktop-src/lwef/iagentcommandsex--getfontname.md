---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418808"
---
# <a name="iagentcommandsexgetfontname"></a><span data-ttu-id="53122-103">IAgentCommandsEx::GetFontName</span><span class="sxs-lookup"><span data-stu-id="53122-103">IAgentCommandsEx::GetFontName</span></span>

<span data-ttu-id="53122-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53122-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

<span data-ttu-id="53122-105">Recupera el valor de la fuente que se muestra en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="53122-105">Retrieves the value for the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="53122-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="53122-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="53122-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="53122-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="53122-108">Dirección de un BSTR que recibe el nombre de fuente mostrado en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="53122-108">The address of a BSTR that receives the font name displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="53122-109">El nombre de fuente devuelto corresponde a la fuente usada para mostrar texto en el menú emergente del carácter cuando la aplicación cliente es de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="53122-109">The font name returned corresponds to the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="53122-110">El valor predeterminado de la configuración de fuente se basa en la configuración de fuente de menú para la configuración de identificador de idioma del carácter, o si no se establece, la configuración de identificador de idioma predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="53122-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language ID setting.</span></span>

<span data-ttu-id="53122-111">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="53122-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="53122-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53122-112">See Also</span></span>

<span data-ttu-id="53122-113">[**IAgentCommandsEx:: SetFontName**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx:: SetFontSize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="53122-113">[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




