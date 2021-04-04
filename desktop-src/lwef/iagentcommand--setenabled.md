---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077626"
---
# <a name="iagentcommandsetenabled"></a><span data-ttu-id="412e2-103">IAgentCommand:: SetEnabled</span><span class="sxs-lookup"><span data-stu-id="412e2-103">IAgentCommand::SetEnabled</span></span>

<span data-ttu-id="412e2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="412e2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

<span data-ttu-id="412e2-105">Establece la propiedad [**Enabled**](enabled-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="412e2-105">Sets the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="412e2-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="412e2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="412e2-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="412e2-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="412e2-108">Valor booleano que establece el valor de la configuración [**habilitada**](enabled-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="412e2-108">A Boolean value that sets the value of the [**Enabled**](enabled-property.md) setting of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="412e2-109">**True** habilita el **comando**; **False** lo deshabilita.</span><span class="sxs-lookup"><span data-stu-id="412e2-109">**True** enables the **Command**; **False** disables it.</span></span> <span data-ttu-id="412e2-110">No se puede seleccionar un **comando** deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="412e2-110">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

<span data-ttu-id="412e2-111">Un [**comando**](/windows/desktop/lwef/the-command-object) debe tener la propiedad [**Enabled**](enabled-property.md) establecida en **true** para poder seleccionarse.</span><span class="sxs-lookup"><span data-stu-id="412e2-111">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Enabled**](enabled-property.md) property set to **True** to be selectable.</span></span> <span data-ttu-id="412e2-112">También debe tener establecida la propiedad [**Caption**](caption-property.md) y su propiedad [**visible**](visible-property.md) establecida en **true** para que aparezca en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="412e2-112">It also must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear in the character's pop-up menu.</span></span> <span data-ttu-id="412e2-113">Para que el **comando** aparezca en la **ventana comandos de voz**, debe establecer su propiedad [**Voice**](voice-property.md).</span><span class="sxs-lookup"><span data-stu-id="412e2-113">To make the **Command** appear in the **Voice Commands Window**, you must set its [**Voice**](voice-property.md)property.</span></span>

## <a name="see-also"></a><span data-ttu-id="412e2-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="412e2-114">See Also</span></span>

<span data-ttu-id="412e2-115">[**IAgentCommand:: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="412e2-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 