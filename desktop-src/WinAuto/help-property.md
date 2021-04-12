---
title: Propiedad Help
description: La propiedad Help proporciona información que indica al usuario sobre la función de un objeto.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357034"
---
# <a name="help-property"></a><span data-ttu-id="da789-103">Propiedad Help</span><span class="sxs-lookup"><span data-stu-id="da789-103">Help Property</span></span>

<span data-ttu-id="da789-104">La propiedad **Help** proporciona información que indica al usuario sobre la función de un objeto.</span><span class="sxs-lookup"><span data-stu-id="da789-104">The **Help** property provides information that tells the user about the function of an object.</span></span>

<span data-ttu-id="da789-105">La propiedad **Help** se recupera llamando a [**IAccessible:: get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span><span class="sxs-lookup"><span data-stu-id="da789-105">The **Help** property is retrieved by calling [**IAccessible::get\_accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span></span>

<span data-ttu-id="da789-106">Esta propiedad contiene información de estilo de globo (como se encuentra en la información sobre herramientas) que se usa para describir lo que hace el objeto o cómo utilizarlo.</span><span class="sxs-lookup"><span data-stu-id="da789-106">This property contains balloon-style information (as found in ToolTips) that is used either to describe what the object does or how to use it.</span></span> <span data-ttu-id="da789-107">Por ejemplo, la propiedad **ayuda** de un botón de la barra de herramientas que muestra una impresora puede proporcionar el texto siguiente: "imprime el documento actual".</span><span class="sxs-lookup"><span data-stu-id="da789-107">For example, the **Help** property for a toolbar button that shows a printer might provide the following text: "Prints the current document."</span></span>

<span data-ttu-id="da789-108">No es necesario que el texto de la propiedad de **ayuda** sea único dentro de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="da789-108">The text for the **Help** property does not have to be unique within the user interface.</span></span>

## <a name="when-to-support-the-help-property"></a><span data-ttu-id="da789-109">Cuándo se debe admitir la propiedad Help</span><span class="sxs-lookup"><span data-stu-id="da789-109">When to Support the Help Property</span></span>

<span data-ttu-id="da789-110">Los servidores no admiten la propiedad **Help** si otras propiedades proporcionan información suficiente sobre el propósito del objeto y las acciones que realiza el objeto.</span><span class="sxs-lookup"><span data-stu-id="da789-110">Servers do not support the **Help** property if other properties provide sufficient information about the object's purpose and the actions the object performs.</span></span> <span data-ttu-id="da789-111">Los objetos accesibles que exponen controles proporcionados por el sistema no admiten la propiedad **Help** .</span><span class="sxs-lookup"><span data-stu-id="da789-111">Accessible objects that expose system-provided controls do not support the **Help** property.</span></span>

 

 




