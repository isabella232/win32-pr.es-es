---
title: IAgentCommandsEx SetDefaultID
description: IAgentCommandsEx SetDefaultID
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420616"
---
# <a name="iagentcommandsexsetdefaultid"></a><span data-ttu-id="b1dc3-103">IAgentCommandsEx::SetDefaultID</span><span class="sxs-lookup"><span data-stu-id="b1dc3-103">IAgentCommandsEx::SetDefaultID</span></span>

<span data-ttu-id="b1dc3-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b1dc3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

<span data-ttu-id="b1dc3-105">Establece el identificador del comando predeterminado en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="b1dc3-105">Sets the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="b1dc3-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1dc3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b1dc3-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="b1dc3-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="b1dc3-108">IDENTIFICADOR del [**comando**](/windows/desktop/lwef/the-command-object) que se va a establecer como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b1dc3-108">The ID for the [**Command**](/windows/desktop/lwef/the-command-object) to be set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="b1dc3-109">Esta propiedad establece el conjunto de objetos de [**comando**](/windows/desktop/lwef/the-command-object) predeterminado en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="b1dc3-109">This property sets the default [**Command**](/windows/desktop/lwef/the-command-object) object set in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="b1dc3-110">El comando predeterminado está en negrita en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="b1dc3-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="b1dc3-111">Sin embargo, el establecimiento del comando predeterminado no cambia realmente el control de comandos ni los eventos de doble clic.</span><span class="sxs-lookup"><span data-stu-id="b1dc3-111">However, setting the default command does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="b1dc3-112">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="b1dc3-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1dc3-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b1dc3-113">See Also</span></span>

[<span data-ttu-id="b1dc3-114">**IAgentCommandsEx::GetDefaultID**</span><span class="sxs-lookup"><span data-stu-id="b1dc3-114">**IAgentCommandsEx::GetDefaultID**</span></span>](iagentcommandsex--getdefaultid.md)


 

 