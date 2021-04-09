---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149234"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a><span data-ttu-id="5fc88-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="5fc88-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="5fc88-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5fc88-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

<span data-ttu-id="5fc88-105">Establece la propiedad [**habilitada**](enabled-property.md) para la gramática de voz de los comandos globales de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5fc88-105">Sets the [**Enabled**](enabled-property.md) property for the voice grammar of Microsoft Agent's global commands.</span></span>

-   <span data-ttu-id="5fc88-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5fc88-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5fc88-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span><span class="sxs-lookup"><span data-stu-id="5fc88-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span></span>
</dt> <dd>

<span data-ttu-id="5fc88-108">Valor booleano que establece si está habilitada la gramática de voz de los comandos globales del agente.</span><span class="sxs-lookup"><span data-stu-id="5fc88-108">A Boolean value that sets whether the voice grammar of Agent's global commands is enabled.</span></span> <span data-ttu-id="5fc88-109">**True** habilita la gramática de voz; **False** lo deshabilita.</span><span class="sxs-lookup"><span data-stu-id="5fc88-109">**True** enables the voice grammar; **False** disables it.</span></span>

</dd> </dl>

<span data-ttu-id="5fc88-110">El agente de Microsoft agrega automáticamente parámetros de voz (gramática) para abrir y cerrar la ventana comandos de voz y para mostrar y ocultar el carácter.</span><span class="sxs-lookup"><span data-stu-id="5fc88-110">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="5fc88-111">Cuando se establece en **false**, el agente deshabilita los parámetros de voz para estos comandos, así como los parámetros de voz para el [**título**](caption-property.md) de los objetos de [**comando**](/windows/desktop/lwef/the-command-object) de otros clientes.</span><span class="sxs-lookup"><span data-stu-id="5fc88-111">When set to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Command**](/windows/desktop/lwef/the-command-object) objects.</span></span> <span data-ttu-id="5fc88-112">Esto le permite eliminarlos de la gramática activa actual del cliente.</span><span class="sxs-lookup"><span data-stu-id="5fc88-112">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="5fc88-113">Sin embargo, dado que esto potencialmente bloquea el acceso de voz a otros clientes, restablezca esta propiedad en **true** después de procesar la entrada de voz del usuario.</span><span class="sxs-lookup"><span data-stu-id="5fc88-113">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="5fc88-114">Deshabilitar la propiedad no afecta al menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="5fc88-114">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="5fc88-115">Los comandos globales agregados por el servidor seguirán apareciendo.</span><span class="sxs-lookup"><span data-stu-id="5fc88-115">The global commands added by the server will still appear.</span></span> <span data-ttu-id="5fc88-116">No se pueden quitar del menú emergente.</span><span class="sxs-lookup"><span data-stu-id="5fc88-116">You cannot remove them from the pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fc88-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5fc88-117">See Also</span></span>

[<span data-ttu-id="5fc88-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5fc88-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 