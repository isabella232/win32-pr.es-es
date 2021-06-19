---
title: Propiedad VoiceCaption (objeto Commands)
description: Obtenga información sobre la propiedad VoiceCaption del objeto Commands, que devuelve o establece el texto que se muestra para el objeto Commands en la ventana Comandos de voz.
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a2113e0a952f253df901d192b42466fa30350
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396130"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="e4eb8-103">Propiedad VoiceCaption (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="e4eb8-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="e4eb8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e4eb8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e4eb8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e4eb8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e4eb8-106">Devuelve o establece el texto que se muestra para el [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) en la ventana Comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="e4eb8-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="e4eb8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="e4eb8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e4eb8-108">*agent.\***Caracteres("**_CharacterID_*_"). Cadena Commands.VoiceCaption_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="e4eb8-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="e4eb8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e4eb8-109">Part</span></span>     | <span data-ttu-id="e4eb8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4eb8-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="e4eb8-111">*string*</span><span class="sxs-lookup"><span data-stu-id="e4eb8-111">*string*</span></span> | <span data-ttu-id="e4eb8-112">Expresión de cadena que se evalúa como el texto mostrado.</span><span class="sxs-lookup"><span data-stu-id="e4eb8-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4eb8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4eb8-113">Remarks</span></span>

<span data-ttu-id="e4eb8-114">Si establece la [**propiedad Voice**](voice-property.md) de la [**colección Commands,**](/windows/desktop/lwef/the-commands-collection-object) normalmente también establecerá su **propiedad VoiceCaption.**</span><span class="sxs-lookup"><span data-stu-id="e4eb8-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="e4eb8-115">La **configuración de texto VoiceCaption** aparece en la ventana Comandos de voz cuando la aplicación cliente está activa en la entrada y el carácter está visible.</span><span class="sxs-lookup"><span data-stu-id="e4eb8-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="e4eb8-116">Si no se establece esta propiedad, la configuración de la propiedad [**Caption**](caption-property.md) de la colección **Commands** determina el texto mostrado.</span><span class="sxs-lookup"><span data-stu-id="e4eb8-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="e4eb8-117">Cuando no se establece la propiedad **VoiceCaption** o **Caption,** los comandos de la colección aparecen en la ventana Comandos de voz en "(undefined command)" cuando la aplicación cliente se convierte en input-active.</span><span class="sxs-lookup"><span data-stu-id="e4eb8-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="e4eb8-118">El **valor VoiceCaption** también determina el texto que se muestra en la sugerencia de escucha para indicar los comandos para los que escucha el carácter.</span><span class="sxs-lookup"><span data-stu-id="e4eb8-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4eb8-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e4eb8-119">See Also</span></span>

[<span data-ttu-id="e4eb8-120">Propiedad Caption</span><span class="sxs-lookup"><span data-stu-id="e4eb8-120">Caption property</span></span>](caption-property.md)


 

 
