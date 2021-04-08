---
title: Propiedad Description (características heredadas del entorno de Windows)
description: Description (propiedad)
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078704"
---
# <a name="description-property-legacy-windows-environment-features"></a><span data-ttu-id="2e874-103">Propiedad Description (características heredadas del entorno de Windows)</span><span class="sxs-lookup"><span data-stu-id="2e874-103">Description Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="2e874-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e874-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2e874-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="2e874-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2e874-106">Devuelve o establece una cadena que especifica la descripción del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="2e874-106">Returns or sets a string that specifies the description for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="2e874-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="2e874-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2e874-108">*agente*. **Caracteres ("**_CharacterID_*_")._* \[  =  *Cadena* de Descripción\]</span><span class="sxs-lookup"><span data-stu-id="2e874-108">*agent*.**Characters("**_CharacterID_*_").Description_* \[ = *string*\]</span></span>



| <span data-ttu-id="2e874-109">Parte</span><span class="sxs-lookup"><span data-stu-id="2e874-109">Part</span></span>     | <span data-ttu-id="2e874-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e874-110">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e874-111">*string*</span><span class="sxs-lookup"><span data-stu-id="2e874-111">*string*</span></span> | <span data-ttu-id="2e874-112">Un valor de cadena correspondiente a la descripción del carácter (en la configuración de idioma actual).</span><span class="sxs-lookup"><span data-stu-id="2e874-112">A string value corresponding to the character's description (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e874-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e874-113">Remarks</span></span>

<span data-ttu-id="2e874-114">La **Descripción** de un carácter puede depender del valor de **LanguageID** del carácter.</span><span class="sxs-lookup"><span data-stu-id="2e874-114">A character's **Description** may depend on the character's **LanguageID** setting.</span></span> <span data-ttu-id="2e874-115">El nombre de un carácter en un idioma puede ser diferente o utilizar caracteres distintos a los de otro.</span><span class="sxs-lookup"><span data-stu-id="2e874-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="2e874-116">La **Descripción** predeterminada del carácter para un idioma específico se define cuando el carácter se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2e874-116">The character's default **Description** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

> [!Note]  
> <span data-ttu-id="2e874-117">El valor de la propiedad **Description** es opcional y es posible que no se proporcione para todos los caracteres.</span><span class="sxs-lookup"><span data-stu-id="2e874-117">The **Description** property setting is optional and may not be supplied for all characters.</span></span>

 

 

 




