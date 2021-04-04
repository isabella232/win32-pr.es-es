---
title: Propiedad VoiceCaption (objeto Commands)
description: Propiedad VoiceCaption
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800758"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="318eb-103">Propiedad VoiceCaption (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="318eb-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="318eb-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="318eb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="318eb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="318eb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="318eb-106">Devuelve o establece el texto que se muestra para el objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) en la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="318eb-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="318eb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="318eb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="318eb-108">\*Caracteres Agent. \***("**_CharacterID_\*_"). Cadena Commands. VoiceCaption_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="318eb-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="318eb-109">Parte</span><span class="sxs-lookup"><span data-stu-id="318eb-109">Part</span></span>     | <span data-ttu-id="318eb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="318eb-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="318eb-111">*string*</span><span class="sxs-lookup"><span data-stu-id="318eb-111">*string*</span></span> | <span data-ttu-id="318eb-112">Expresión de cadena que se evalúa como el texto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="318eb-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="318eb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="318eb-113">Remarks</span></span>

<span data-ttu-id="318eb-114">Si establece la propiedad [**Voice**](voice-property.md) de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , normalmente también establecerá su propiedad **VoiceCaption** .</span><span class="sxs-lookup"><span data-stu-id="318eb-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="318eb-115">La configuración de texto **VoiceCaption** aparece en la ventana comandos de voz cuando la aplicación cliente es de entrada-activa y el carácter está visible.</span><span class="sxs-lookup"><span data-stu-id="318eb-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="318eb-116">Si no se establece esta propiedad, el valor de la propiedad [**título**](caption-property.md) de la colección de **comandos** determina el texto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="318eb-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="318eb-117">Cuando no se establece la propiedad **VoiceCaption** o **Caption** , los comandos de la colección aparecen en la ventana comandos de voz en "(comando no definido)" cuando la aplicación cliente pasa a ser de entrada activa.</span><span class="sxs-lookup"><span data-stu-id="318eb-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="318eb-118">La configuración **VoiceCaption** también determina el texto que se muestra en la sugerencia de escucha para indicar los comandos para los que el carácter realiza escuchas.</span><span class="sxs-lookup"><span data-stu-id="318eb-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="318eb-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="318eb-119">See Also</span></span>

[<span data-ttu-id="318eb-120">Propiedad Caption</span><span class="sxs-lookup"><span data-stu-id="318eb-120">Caption property</span></span>](caption-property.md)


 

 
