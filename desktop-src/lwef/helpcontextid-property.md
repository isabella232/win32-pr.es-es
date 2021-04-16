---
title: Propiedad HelpContextID (objeto de colección Commands)
description: Propiedad HelpContextID
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488813"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="28bd7-103">Propiedad HelpContextID (objeto de colección Commands)</span><span class="sxs-lookup"><span data-stu-id="28bd7-103">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="28bd7-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="28bd7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="28bd7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="28bd7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="28bd7-106">Devuelve o establece un número de contexto asociado para el objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="28bd7-106">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="28bd7-107">Se utiliza para proporcionar ayuda contextual para el objeto **Commands** .</span><span class="sxs-lookup"><span data-stu-id="28bd7-107">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="28bd7-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="28bd7-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="28bd7-109">\*Caracteres Agent. \***("**_CharacterID_*_"). Comandos ("_*_Name_\*_")._ \*  \[  =  *Número* de HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="28bd7-109">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="28bd7-110">Parte</span><span class="sxs-lookup"><span data-stu-id="28bd7-110">Part</span></span>     | <span data-ttu-id="28bd7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="28bd7-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="28bd7-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="28bd7-112">*Number*</span></span> | <span data-ttu-id="28bd7-113">Entero que especifica un número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="28bd7-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28bd7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28bd7-114">Remarks</span></span>

<span data-ttu-id="28bd7-115">Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el agente llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="28bd7-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="28bd7-116">Si establece un número de contexto en **HelpContextID**, el agente llama a help y busca el tema identificado por ese número de contexto.</span><span class="sxs-lookup"><span data-stu-id="28bd7-116">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="28bd7-117">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="28bd7-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="28bd7-118">La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="28bd7-118">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="28bd7-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28bd7-119">See Also</span></span>

[<span data-ttu-id="28bd7-120">**HelpFile (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="28bd7-120">**HelpFile property**</span></span>](helpfile-property.md)


 

 
