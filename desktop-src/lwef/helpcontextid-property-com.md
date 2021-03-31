---
title: Propiedad HelpContextID (objeto Command)
description: Propiedad HelpContextID
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef0fcfb24aee7aed75f8eb794e81291207ea24
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149830"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="0a1b2-103">Propiedad HelpContextID (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="0a1b2-103">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="0a1b2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a1b2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0a1b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="0a1b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0a1b2-106">Devuelve o establece un número de contexto asociado para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="0a1b2-106">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="0a1b2-107">Se utiliza para proporcionar ayuda contextual para el objeto de **comando** .</span><span class="sxs-lookup"><span data-stu-id="0a1b2-107">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="0a1b2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="0a1b2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0a1b2-109">\*Caracteres Agent. \***("**_CharacterID_\*_"). Comandos ("")._ \*  \[  =  *Número* de HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="0a1b2-109">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="0a1b2-110">Parte</span><span class="sxs-lookup"><span data-stu-id="0a1b2-110">Part</span></span>     | <span data-ttu-id="0a1b2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a1b2-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="0a1b2-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="0a1b2-112">*Number*</span></span> | <span data-ttu-id="0a1b2-113">Entero que especifica un número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="0a1b2-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a1b2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a1b2-114">Remarks</span></span>

<span data-ttu-id="0a1b2-115">Si ha creado un archivo de ayuda de Windows para la aplicación y establece la propiedad [**HelpFile**](helpfile-property.md) del carácter en el archivo, el agente llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el comando.</span><span class="sxs-lookup"><span data-stu-id="0a1b2-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="0a1b2-116">Si establece un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual.</span><span class="sxs-lookup"><span data-stu-id="0a1b2-116">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="0a1b2-117">El número de contexto actual es el valor de **HelpContextID** para el comando.</span><span class="sxs-lookup"><span data-stu-id="0a1b2-117">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="0a1b2-118">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0a1b2-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="0a1b2-119">La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0a1b2-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0a1b2-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a1b2-120">See Also</span></span>

[<span data-ttu-id="0a1b2-121">**HelpFile (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="0a1b2-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
