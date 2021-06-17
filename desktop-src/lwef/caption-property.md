---
title: Propiedad Caption (objeto Command)
description: Obtenga información sobre la propiedad Caption del objeto Command. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262557"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="b525d-104">Propiedad Caption (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="b525d-104">Caption Property (Command Object)</span></span>

<span data-ttu-id="b525d-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b525d-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b525d-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b525d-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b525d-107">Determina el texto que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en el menú emergente del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="b525d-107">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="b525d-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="b525d-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b525d-109">*agent\***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_"). Cadena de_ \*  \[  =  *título*\]</span><span class="sxs-lookup"><span data-stu-id="b525d-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="b525d-110">Parte</span><span class="sxs-lookup"><span data-stu-id="b525d-110">Part</span></span>     | <span data-ttu-id="b525d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b525d-111">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b525d-112">*string*</span><span class="sxs-lookup"><span data-stu-id="b525d-112">*string*</span></span> | <span data-ttu-id="b525d-113">Expresión de cadena que se evalúa como el texto mostrado como título del **comando**.</span><span class="sxs-lookup"><span data-stu-id="b525d-113">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b525d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b525d-114">Remarks</span></span>

<span data-ttu-id="b525d-115">Para especificar una clave de acceso (mnemotécnica sin línea) para el título **,** incluya un carácter de yerba (&) antes de ese carácter.</span><span class="sxs-lookup"><span data-stu-id="b525d-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="b525d-116">Si no define **voiceCaption para** el comando, se usará la configuración de título. </span><span class="sxs-lookup"><span data-stu-id="b525d-116">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
