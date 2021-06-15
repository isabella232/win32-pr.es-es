---
title: Propiedad HelpContextID (objeto de colección Commands)
description: Obtenga información sobre la propiedad HelpContextID del objeto Commands Collection. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed6ccf40545e15b3603ce5abe80ef94ff4272a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068241"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="97e31-104">Propiedad HelpContextID (objeto de colección Commands)</span><span class="sxs-lookup"><span data-stu-id="97e31-104">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="97e31-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="97e31-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="97e31-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="97e31-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="97e31-107">Devuelve o establece un número de contexto asociado para el [**objeto Commands.**](/windows/desktop/lwef/the-commands-collection-object)</span><span class="sxs-lookup"><span data-stu-id="97e31-107">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="97e31-108">Se usa para proporcionar ayuda contextual para el **objeto Commands.**</span><span class="sxs-lookup"><span data-stu-id="97e31-108">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="97e31-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="97e31-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="97e31-110">*agent.\***Caracteres("**_CharacterID_*_"). Commands("_*_name_*_"). HelpContextID_ \*  \[  =  *Number*\]</span><span class="sxs-lookup"><span data-stu-id="97e31-110">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="97e31-111">Parte</span><span class="sxs-lookup"><span data-stu-id="97e31-111">Part</span></span>     | <span data-ttu-id="97e31-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="97e31-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="97e31-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="97e31-113">*Number*</span></span> | <span data-ttu-id="97e31-114">Entero que especifica un número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="97e31-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97e31-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97e31-115">Remarks</span></span>

<span data-ttu-id="97e31-116">Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el Agente llama automáticamente a help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario selecciona el objeto [**Commands.**](/windows/desktop/lwef/the-commands-collection-object)</span><span class="sxs-lookup"><span data-stu-id="97e31-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="97e31-117">Si establece un número de contexto en **HelpContextID,** el Agente llama a la Ayuda y busca el tema identificado por ese número de contexto.</span><span class="sxs-lookup"><span data-stu-id="97e31-117">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="97e31-118">Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="97e31-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="97e31-119">La compilación de un archivo de Ayuda requiere el compilador de Ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="97e31-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="97e31-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="97e31-120">See Also</span></span>

[<span data-ttu-id="97e31-121">**HelpFile, propiedad**</span><span class="sxs-lookup"><span data-stu-id="97e31-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
