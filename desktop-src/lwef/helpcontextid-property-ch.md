---
title: Propiedad HelpContextID (objeto Characters)
description: Obtenga información sobre la propiedad HelpContextID del objeto Characters. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068192"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="ad3ff-104">Propiedad HelpContextID (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="ad3ff-104">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="ad3ff-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ad3ff-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ad3ff-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad3ff-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ad3ff-107">Devuelve o establece un número de contexto asociado para el carácter.</span><span class="sxs-lookup"><span data-stu-id="ad3ff-107">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="ad3ff-108">Se usa para proporcionar ayuda contextual para el carácter.</span><span class="sxs-lookup"><span data-stu-id="ad3ff-108">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="ad3ff-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="ad3ff-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ad3ff-110">*agent.\***Characters("**_CharacterID_*_"). HelpContextID_ \*  \[  =  *Number*\]</span><span class="sxs-lookup"><span data-stu-id="ad3ff-110">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="ad3ff-111">Parte</span><span class="sxs-lookup"><span data-stu-id="ad3ff-111">Part</span></span>     | <span data-ttu-id="ad3ff-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad3ff-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="ad3ff-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="ad3ff-113">*Number*</span></span> | <span data-ttu-id="ad3ff-114">Entero que especifica un número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="ad3ff-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad3ff-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad3ff-115">Remarks</span></span>

<span data-ttu-id="ad3ff-116">Para admitir la Ayuda contextual para el carácter, asigne el número de contexto al carácter que usa para el tema de Ayuda asociado al compilar el archivo de Ayuda.</span><span class="sxs-lookup"><span data-stu-id="ad3ff-116">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="ad3ff-117">Esta propiedad solo se aplica al cliente del carácter; la configuración no afecta a otros clientes del carácter ni a otros caracteres del cliente.</span><span class="sxs-lookup"><span data-stu-id="ad3ff-117">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="ad3ff-118">Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el Agente llama automáticamente a la Ayuda cuando [**HelpModeOn**](helpmodeon-property.md) se establece en **True** y el usuario hace clic en el carácter.</span><span class="sxs-lookup"><span data-stu-id="ad3ff-118">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="ad3ff-119">Si hay un número de contexto en [**HelpContextID,**](helpcontextid-property.md)el Agente llama a la Ayuda y busca el tema identificado por el número de contexto actual.</span><span class="sxs-lookup"><span data-stu-id="ad3ff-119">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="ad3ff-120">El número de contexto actual es el valor **de HelpContextID** para el carácter.</span><span class="sxs-lookup"><span data-stu-id="ad3ff-120">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="ad3ff-121">La compilación de un archivo de Ayuda requiere el compilador de Ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ad3ff-121">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="ad3ff-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ad3ff-122">See Also</span></span>

[<span data-ttu-id="ad3ff-123">**Propiedad HelpFile**</span><span class="sxs-lookup"><span data-stu-id="ad3ff-123">**HelpFile property**</span></span>](helpfile-property.md)


 

 




