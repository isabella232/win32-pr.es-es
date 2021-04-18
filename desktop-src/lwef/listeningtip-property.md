---
title: Propiedad ListeningTip
description: Propiedad ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695446"
---
# <a name="listeningtip-property"></a><span data-ttu-id="81b76-103">Propiedad ListeningTip</span><span class="sxs-lookup"><span data-stu-id="81b76-103">ListeningTip Property</span></span>

<span data-ttu-id="81b76-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="81b76-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="81b76-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="81b76-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="81b76-106">Devuelve un valor booleano que indica la configuración del usuario actual para la sugerencia de escucha.</span><span class="sxs-lookup"><span data-stu-id="81b76-106">Returns a Boolean indicating the current user setting for the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="81b76-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="81b76-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="81b76-108">*agente \* \* *. SpeechInput.ListeningTip**</span><span class="sxs-lookup"><span data-stu-id="81b76-108">*agent\*\*\*.SpeechInput.ListeningTip*\*</span></span>



| <span data-ttu-id="81b76-109">Value</span><span class="sxs-lookup"><span data-stu-id="81b76-109">Value</span></span>     | <span data-ttu-id="81b76-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="81b76-110">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="81b76-111">**True**</span><span class="sxs-lookup"><span data-stu-id="81b76-111">**True**</span></span>  | <span data-ttu-id="81b76-112">La sugerencia de escucha está habilitada.</span><span class="sxs-lookup"><span data-stu-id="81b76-112">The Listening Tip is enabled.</span></span>  |
| <span data-ttu-id="81b76-113">**False**</span><span class="sxs-lookup"><span data-stu-id="81b76-113">**False**</span></span> | <span data-ttu-id="81b76-114">La sugerencia de escucha está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="81b76-114">The Listening Tip is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81b76-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81b76-115">Remarks</span></span>

<span data-ttu-id="81b76-116">La propiedad **ListeningTip** indica si está habilitada la opción Mostrar sugerencia de escucha en la hoja de propiedades del agente de Microsoft (opciones avanzadas de caracteres).</span><span class="sxs-lookup"><span data-stu-id="81b76-116">The **ListeningTip** property indicates whether the Display Listening Tip option in the Microsoft Agent property sheet (Advanced Character Options) is enabled.</span></span> <span data-ttu-id="81b76-117">Cuando **ListeningTip** devuelve **true** y la entrada de voz está habilitada, el servidor muestra la ventana de sugerencia cuando el usuario presiona la tecla de escucha.</span><span class="sxs-lookup"><span data-stu-id="81b76-117">When **ListeningTip** returns **True** and speech input is enabled, the server displays the tip window when the user presses the Listening key.</span></span>

## <a name="see-also"></a><span data-ttu-id="81b76-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="81b76-118">See Also</span></span>

[<span data-ttu-id="81b76-119">**Evento AgentPropertyChange**</span><span class="sxs-lookup"><span data-stu-id="81b76-119">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




