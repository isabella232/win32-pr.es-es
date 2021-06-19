---
title: Propiedad VoiceCaption (objeto Command)
description: Obtenga información sobre la propiedad VoiceCaption del objeto Command, que establece o devuelve el texto que se muestra para el objeto Command en la ventana Comandos de voz.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396170"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="a3d2e-103">Propiedad VoiceCaption (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="a3d2e-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="a3d2e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a3d2e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a3d2e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3d2e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a3d2e-106">Establece o devuelve el texto que se muestra para el [**objeto Command**](/windows/desktop/lwef/the-command-object) en la ventana Comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="a3d2e-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="a3d2e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="a3d2e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a3d2e-108">*agent.\***Caracteres("**_CharacterID_*_"). Commands("_*_Name_*_"). Cadena VoiceCaption_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="a3d2e-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="a3d2e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a3d2e-109">Part</span></span>     | <span data-ttu-id="a3d2e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3d2e-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="a3d2e-111">*string*</span><span class="sxs-lookup"><span data-stu-id="a3d2e-111">*string*</span></span> | <span data-ttu-id="a3d2e-112">Expresión de cadena que se evalúa como el texto mostrado.</span><span class="sxs-lookup"><span data-stu-id="a3d2e-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3d2e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3d2e-113">Remarks</span></span>

<span data-ttu-id="a3d2e-114">Si define un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una [**colección Commands**](https://www.bing.com/search?q=**Commands**) y establece su propiedad [**Voice,**](voice-property.md) normalmente también establecerá su [**propiedad VoiceCaption.**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="a3d2e-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="a3d2e-115">Este texto aparecerá en la ventana Comandos de voz cuando la aplicación cliente esté activa en la entrada y el carácter esté visible.</span><span class="sxs-lookup"><span data-stu-id="a3d2e-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="a3d2e-116">Si no se establece esta propiedad, la configuración de la [**propiedad Caption**](caption-property.md) determina el texto mostrado.</span><span class="sxs-lookup"><span data-stu-id="a3d2e-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="a3d2e-117">Cuando no se **establece la propiedad VoiceCaption** ni **Caption,** el comando no aparece en la ventana Comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="a3d2e-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="a3d2e-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3d2e-118">See Also</span></span>

[<span data-ttu-id="a3d2e-119">**Propiedad Caption**</span><span class="sxs-lookup"><span data-stu-id="a3d2e-119">**Caption property**</span></span>](caption-property.md)


 

 
