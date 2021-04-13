---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420635"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a><span data-ttu-id="e1fc8-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1fc8-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="e1fc8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e1fc8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

<span data-ttu-id="e1fc8-105">Recupera si la gramática de voz para los comandos globales del agente está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e1fc8-105">Retrieves whether the voice grammar for Agent's global commands is enabled.</span></span>

-   <span data-ttu-id="e1fc8-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e1fc8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e1fc8-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="e1fc8-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="e1fc8-108">La dirección que recibe **true** si la gramática de voz para los comandos globales del agente está habilitada, **false** si está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="e1fc8-108">The address that receives **True** if the voice grammar for Agent's global commands is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="e1fc8-109">El agente de Microsoft agrega automáticamente parámetros de voz (gramática) para abrir y cerrar la ventana comandos de voz y para mostrar y ocultar el carácter.</span><span class="sxs-lookup"><span data-stu-id="e1fc8-109">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="e1fc8-110">Cuando este método devuelve **false**, los parámetros de voz para estos comandos, así como los parámetros de voz para el [**título**](caption-property.md) de los objetos de [**comando**](/windows/desktop/lwef/the-command-object) de otros clientes, no se incluyen en la gramática.</span><span class="sxs-lookup"><span data-stu-id="e1fc8-110">When this method returns **False**, any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other clients' [**Command**](/windows/desktop/lwef/the-command-object) objects are not included in the grammar.</span></span> <span data-ttu-id="e1fc8-111">Esto le permite eliminarlos de la gramática activa actual del cliente.</span><span class="sxs-lookup"><span data-stu-id="e1fc8-111">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="e1fc8-112">Sin embargo, esta configuración no refleja la inclusión de estos comandos en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="e1fc8-112">However, this setting does not reflect the inclusion of these commands in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1fc8-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e1fc8-113">See Also</span></span>

[<span data-ttu-id="e1fc8-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e1fc8-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 