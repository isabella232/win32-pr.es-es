---
title: IAgentCommandsEx SetFontSize
description: IAgentCommandsEx SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487591"
---
# <a name="iagentcommandsexsetfontsize"></a><span data-ttu-id="38e73-103">IAgentCommandsEx::SetFontSize</span><span class="sxs-lookup"><span data-stu-id="38e73-103">IAgentCommandsEx::SetFontSize</span></span>

<span data-ttu-id="38e73-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38e73-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

<span data-ttu-id="38e73-105">Establece el tamaño de la fuente que se muestra en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="38e73-105">Sets the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="38e73-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="38e73-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="38e73-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="38e73-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="38e73-108">Tamaño de la fuente.</span><span class="sxs-lookup"><span data-stu-id="38e73-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="38e73-109">Esta propiedad determina el tamaño en puntos de la fuente usada para mostrar texto en el menú emergente del carácter cuando la aplicación cliente es de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="38e73-109">This property determines the point size of the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="38e73-110">El valor predeterminado de la configuración de fuente se basa en el valor de fuente de menú para la configuración de identificador de idioma del carácter, o bien, si no está establecido, es la configuración de idioma predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="38e73-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language setting.</span></span> <span data-ttu-id="38e73-111">Si no es de entrada-activo, el texto de la [**leyenda**](caption-property.md) de [**comandos**](/windows/desktop/lwef/the-command-object) de la aplicación cliente aparece en el tamaño de punto especificado para el cliente de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="38e73-111">If not input-active, your client application's [**Command**](/windows/desktop/lwef/the-command-object) [**Caption**](caption-property.md) text appears in the point size specified for the input-active client.</span></span>

<span data-ttu-id="38e73-112">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="38e73-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="38e73-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38e73-113">See Also</span></span>

<span data-ttu-id="38e73-114">[**IAgentCommandsEx:: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: SetFontName**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="38e73-114">[**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 