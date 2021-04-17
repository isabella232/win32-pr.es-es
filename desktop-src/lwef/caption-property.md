---
title: Propiedad Caption (objeto Command)
description: Propiedad Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714513"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="297fa-103">Propiedad Caption (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="297fa-103">Caption Property (Command Object)</span></span>

<span data-ttu-id="297fa-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="297fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="297fa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="297fa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="297fa-106">Determina el texto que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en el menú emergente del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="297fa-106">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="297fa-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="297fa-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="297fa-108">\*agente \***. Caracteres ("**_CharacterID_*_"). Comandos ("_*_Name_\*_")._ \*  \[  =  *Cadena* de leyenda\]</span><span class="sxs-lookup"><span data-stu-id="297fa-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="297fa-109">Parte</span><span class="sxs-lookup"><span data-stu-id="297fa-109">Part</span></span>     | <span data-ttu-id="297fa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="297fa-110">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="297fa-111">*string*</span><span class="sxs-lookup"><span data-stu-id="297fa-111">*string*</span></span> | <span data-ttu-id="297fa-112">Expresión de cadena que se evalúa como el texto que se muestra como título del **comando**.</span><span class="sxs-lookup"><span data-stu-id="297fa-112">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="297fa-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="297fa-113">Remarks</span></span>

<span data-ttu-id="297fa-114">Para especificar una tecla de acceso (tecla de acceso no alineada) para el **título**, incluya un carácter de y comercial (&) antes de ese carácter.</span><span class="sxs-lookup"><span data-stu-id="297fa-114">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="297fa-115">Si no define un **VoiceCaption** para el comando, se usará la configuración del **título** .</span><span class="sxs-lookup"><span data-stu-id="297fa-115">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
