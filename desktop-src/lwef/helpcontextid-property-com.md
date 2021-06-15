---
title: Propiedad HelpContextID (objeto Command)
description: Obtenga información sobre la propiedad HelpContextID del objeto Command. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068521"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="36ac6-104">Propiedad HelpContextID (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="36ac6-104">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="36ac6-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="36ac6-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="36ac6-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36ac6-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="36ac6-107">Devuelve o establece un número de contexto asociado para el [**objeto Command.**](/windows/desktop/lwef/the-command-object)</span><span class="sxs-lookup"><span data-stu-id="36ac6-107">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="36ac6-108">Se usa para proporcionar ayuda contextual para el **objeto Command.**</span><span class="sxs-lookup"><span data-stu-id="36ac6-108">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="36ac6-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="36ac6-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="36ac6-110">*agent.\***Caracteres("**_CharacterID_*_"). Commands(""). HelpContextID_ \*  \[  =  *Number*\]</span><span class="sxs-lookup"><span data-stu-id="36ac6-110">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="36ac6-111">Parte</span><span class="sxs-lookup"><span data-stu-id="36ac6-111">Part</span></span>     | <span data-ttu-id="36ac6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="36ac6-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="36ac6-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="36ac6-113">*Number*</span></span> | <span data-ttu-id="36ac6-114">Entero que especifica un número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="36ac6-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36ac6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36ac6-115">Remarks</span></span>

<span data-ttu-id="36ac6-116">Si ha creado un archivo de Ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter en el archivo, el Agente llama automáticamente a help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **True** y el usuario selecciona el comando.</span><span class="sxs-lookup"><span data-stu-id="36ac6-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="36ac6-117">Si establece un número de contexto en [**HelpContextID,**](helpcontextid-property.md)el Agente llama a la Ayuda y busca el tema identificado por el número de contexto actual.</span><span class="sxs-lookup"><span data-stu-id="36ac6-117">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="36ac6-118">El número de contexto actual es el valor de **HelpContextID** para el comando.</span><span class="sxs-lookup"><span data-stu-id="36ac6-118">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="36ac6-119">Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="36ac6-119">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="36ac6-120">La compilación de un archivo de Ayuda requiere el compilador de Ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="36ac6-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="36ac6-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="36ac6-121">See Also</span></span>

[<span data-ttu-id="36ac6-122">**HelpFile, propiedad**</span><span class="sxs-lookup"><span data-stu-id="36ac6-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 
