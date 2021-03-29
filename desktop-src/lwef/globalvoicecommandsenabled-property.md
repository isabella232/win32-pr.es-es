---
title: Propiedad GlobalVoiceCommandsEnabled
description: Propiedad GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995265"
---
# <a name="globalvoicecommandsenabled-property"></a><span data-ttu-id="17c1a-103">Propiedad GlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="17c1a-103">GlobalVoiceCommandsEnabled Property</span></span>

<span data-ttu-id="17c1a-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17c1a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="17c1a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="17c1a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="17c1a-106">Devuelve o establece si la voz está habilitada para los comandos globales del agente.</span><span class="sxs-lookup"><span data-stu-id="17c1a-106">Returns or sets whether voice is enabled for Agent's global commands.</span></span>

</dd> <dt>

<span data-ttu-id="17c1a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="17c1a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="17c1a-108">*directivas. ***Caracteres ("*** CharacterID \* *"). Commands. GlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="17c1a-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Commands.GlobalVoiceCommandsEnabled**</span></span>

<span data-ttu-id="17c1a-109">\[ = *booleano*\]</span><span class="sxs-lookup"><span data-stu-id="17c1a-109">\[ = *boolean*\]</span></span>



| <span data-ttu-id="17c1a-110">Parte</span><span class="sxs-lookup"><span data-stu-id="17c1a-110">Part</span></span>      | <span data-ttu-id="17c1a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="17c1a-111">Description</span></span>                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c1a-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="17c1a-112">*boolean*</span></span> | <span data-ttu-id="17c1a-113">Una expresión booleana que indica si están habilitados los parámetros de voz para los comandos globales del agente.</span><span class="sxs-lookup"><span data-stu-id="17c1a-113">A Boolean expression that indicates whether voice parameters for Agent's global commands are enabled.</span></span> <span data-ttu-id="17c1a-114">**True** (valor predeterminado) los parámetros de voz están habilitados.</span><span class="sxs-lookup"><span data-stu-id="17c1a-114">**True** (Default) Voice parameters are enabled.</span></span> <br/> <span data-ttu-id="17c1a-115">**False** Los parámetros de voz están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="17c1a-115">**False** Voice parameters are disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17c1a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17c1a-116">Remarks</span></span>

<span data-ttu-id="17c1a-117">El agente de Microsoft agrega automáticamente parámetros de voz (gramática) para abrir y cerrar la ventana comandos de voz y para mostrar y ocultar el carácter.</span><span class="sxs-lookup"><span data-stu-id="17c1a-117">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="17c1a-118">Si establece **GlobalVoiceCommandsEnabled** en **false**, el agente deshabilita los parámetros de voz para estos comandos, así como los parámetros de voz para el [**título**](caption-property.md) de los objetos de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de otros clientes.</span><span class="sxs-lookup"><span data-stu-id="17c1a-118">If you set **GlobalVoiceCommandsEnabled** to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Commands**](/windows/desktop/lwef/the-commands-collection-object) objects.</span></span> <span data-ttu-id="17c1a-119">Esto le permite eliminarlos de la gramática activa actual del cliente.</span><span class="sxs-lookup"><span data-stu-id="17c1a-119">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="17c1a-120">Sin embargo, dado que esto potencialmente bloquea el acceso de voz a otros clientes, restablezca esta propiedad en **true** después de procesar la entrada de voz del usuario.</span><span class="sxs-lookup"><span data-stu-id="17c1a-120">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="17c1a-121">Deshabilitar la propiedad no afecta al menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="17c1a-121">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="17c1a-122">Los comandos globales agregados por el servidor seguirán apareciendo.</span><span class="sxs-lookup"><span data-stu-id="17c1a-122">The global commands added by the server will still appear.</span></span> <span data-ttu-id="17c1a-123">No se pueden quitar del menú emergente.</span><span class="sxs-lookup"><span data-stu-id="17c1a-123">You cannot remove them from the pop-up menu.</span></span>

 

