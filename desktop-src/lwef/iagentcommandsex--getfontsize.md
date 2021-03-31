---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418807"
---
# <a name="iagentcommandsexgetfontsize"></a><span data-ttu-id="8add2-103">IAgentCommandsEx::GetFontSize</span><span class="sxs-lookup"><span data-stu-id="8add2-103">IAgentCommandsEx::GetFontSize</span></span>

<span data-ttu-id="8add2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8add2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

<span data-ttu-id="8add2-105">Recupera el valor para el tamaño de la fuente que se muestra en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="8add2-105">Retrieves the value for the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="8add2-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8add2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8add2-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span><span class="sxs-lookup"><span data-stu-id="8add2-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="8add2-108">Dirección de un valor que recibe el tamaño de la fuente.</span><span class="sxs-lookup"><span data-stu-id="8add2-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="8add2-109">El tamaño en puntos de la fuente devuelta corresponde al tamaño definido para mostrar texto en el menú emergente del carácter cuando el cliente es de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="8add2-109">The point size of the font returned corresponds to the size defined to display text in the character's pop-up menu when your client is input-active.</span></span> <span data-ttu-id="8add2-110">El valor predeterminado de la configuración de fuente se basa en la configuración de fuente de menú para la configuración de identificador de idioma del carácter, o si no se establece, la configuración de idioma predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="8add2-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language setting.</span></span>

<span data-ttu-id="8add2-111">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="8add2-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="8add2-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8add2-112">See Also</span></span>

<span data-ttu-id="8add2-113">[**IAgentCommandsEx:: SetFontSize**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx:: SetFontName**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="8add2-113">[**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 




