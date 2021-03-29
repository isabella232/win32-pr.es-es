---
title: HelpFile (propiedad)
description: HelpFile (propiedad)
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776458"
---
# <a name="helpfile-property"></a><span data-ttu-id="403f6-103">HelpFile (propiedad)</span><span class="sxs-lookup"><span data-stu-id="403f6-103">HelpFile Property</span></span>

<span data-ttu-id="403f6-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="403f6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="403f6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="403f6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="403f6-106">Devuelve o establece la ruta de acceso y el nombre de archivo de un archivo de ayuda contextual de Microsoft Windows proporcionado por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="403f6-106">Returns or sets the path and filename for a Microsoft Windows context-sensitive Help file supplied by the client application.</span></span>

</dd> <dt>

<span data-ttu-id="403f6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="403f6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="403f6-108">\*agente. ***Caracteres ("*** CharacterID \* *").* \*  \[  =  *Nombre de archivo* de HelpFile\]</span><span class="sxs-lookup"><span data-stu-id="403f6-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Helpfile** \[ = *Filename*\]</span></span>



| <span data-ttu-id="403f6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="403f6-109">Part</span></span>       | <span data-ttu-id="403f6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="403f6-110">Description</span></span>                                                                    |
|------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="403f6-111">*Nombre de archivo*</span><span class="sxs-lookup"><span data-stu-id="403f6-111">*Filename*</span></span> | <span data-ttu-id="403f6-112">Expresión de cadena que especifica la ruta de acceso y el nombre del archivo de ayuda de Windows.</span><span class="sxs-lookup"><span data-stu-id="403f6-112">A string expression specifying the path and filename of the Windows Help file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="403f6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="403f6-113">Remarks</span></span>

<span data-ttu-id="403f6-114">Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad **HelpFile** del carácter, el agente llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario hace clic en el carácter o selecciona un comando en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="403f6-114">If you've created a Windows Help file for your application and set the character's **HelpFile** property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="403f6-115">Si especificó un número de contexto en la propiedad [**IDDelContextoDeAyuda**](helpcontextid-property.md) del comando seleccionado, la ayuda de muestra un tema correspondiente al contexto de ayuda actual. en caso contrario, se muestra "no hay ningún tema de ayuda asociado a este elemento".</span><span class="sxs-lookup"><span data-stu-id="403f6-115">If you specified a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="403f6-116">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="403f6-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="403f6-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="403f6-117">See Also</span></span>

<span data-ttu-id="403f6-118">[**Propiedad HelpModeOn**](helpmodeon-property.md), [ **propiedad HelpContextID**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="403f6-118">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

 




