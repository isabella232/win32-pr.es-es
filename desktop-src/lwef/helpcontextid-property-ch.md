---
title: Propiedad HelpContextID (objeto Characters)
description: Propiedad HelpContextID
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42006f74cc3668f8df9af2c2ffcd2515614ec735
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421797"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="0037e-103">Propiedad HelpContextID (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="0037e-103">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="0037e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0037e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0037e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="0037e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0037e-106">Devuelve o establece un número de contexto asociado para el carácter.</span><span class="sxs-lookup"><span data-stu-id="0037e-106">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="0037e-107">Se utiliza para proporcionar ayuda contextual para el carácter.</span><span class="sxs-lookup"><span data-stu-id="0037e-107">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="0037e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="0037e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0037e-109">\*Caracteres Agent. \***("**_CharacterID_\*_")._ \*  \[  =  *Número* de HelpContextID\]</span><span class="sxs-lookup"><span data-stu-id="0037e-109">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="0037e-110">Parte</span><span class="sxs-lookup"><span data-stu-id="0037e-110">Part</span></span>     | <span data-ttu-id="0037e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0037e-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="0037e-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="0037e-112">*Number*</span></span> | <span data-ttu-id="0037e-113">Entero que especifica un número de contexto válido.</span><span class="sxs-lookup"><span data-stu-id="0037e-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0037e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0037e-114">Remarks</span></span>

<span data-ttu-id="0037e-115">Para admitir la ayuda contextual para el carácter, asigne el número de contexto al carácter que se usa para el tema de ayuda asociado al compilar el archivo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="0037e-115">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="0037e-116">Esta propiedad solo se aplica al cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres del cliente.</span><span class="sxs-lookup"><span data-stu-id="0037e-116">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="0037e-117">Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el agente llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario hace clic en el carácter.</span><span class="sxs-lookup"><span data-stu-id="0037e-117">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="0037e-118">Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual.</span><span class="sxs-lookup"><span data-stu-id="0037e-118">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="0037e-119">El número de contexto actual es el valor de **HelpContextID** para el carácter.</span><span class="sxs-lookup"><span data-stu-id="0037e-119">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="0037e-120">La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0037e-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0037e-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0037e-121">See Also</span></span>

[<span data-ttu-id="0037e-122">**HelpFile (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="0037e-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 




