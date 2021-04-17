---
title: Propiedad Name (objeto Characters)
description: Propiedad Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488729"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="bd08b-103">Propiedad Name (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="bd08b-103">Name Property (Characters Object)</span></span>

<span data-ttu-id="bd08b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bd08b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bd08b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="bd08b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bd08b-106">Devuelve o establece una cadena que especifica el nombre predeterminado del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="bd08b-106">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="bd08b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="bd08b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bd08b-108">\*agente \***. Caracteres ("**_CharacterID_\*_")._ \*  \[  =  *Cadena* de nombre\]</span><span class="sxs-lookup"><span data-stu-id="bd08b-108">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="bd08b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="bd08b-109">Part</span></span>     | <span data-ttu-id="bd08b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd08b-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd08b-111">*string*</span><span class="sxs-lookup"><span data-stu-id="bd08b-111">*string*</span></span> | <span data-ttu-id="bd08b-112">Valor de cadena que corresponde al nombre del carácter (en la configuración de idioma actual).</span><span class="sxs-lookup"><span data-stu-id="bd08b-112">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd08b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd08b-113">Remarks</span></span>

<span data-ttu-id="bd08b-114">El **nombre** de un carácter puede depender del valor de [**LanguageID**](languageid-property.md) del carácter.</span><span class="sxs-lookup"><span data-stu-id="bd08b-114">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="bd08b-115">El nombre de un carácter en un idioma puede ser diferente o utilizar caracteres distintos a los de otro.</span><span class="sxs-lookup"><span data-stu-id="bd08b-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="bd08b-116">El **nombre** predeterminado del carácter para un idioma específico se define cuando el carácter se compila con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bd08b-116">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="bd08b-117">Evite cambiar el nombre de un carácter, especialmente cuando se usa en un escenario en el que otras aplicaciones cliente pueden utilizar el mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="bd08b-117">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="bd08b-118">Además, el agente usa el **nombre** del carácter para crear automáticamente comandos para ocultar y mostrar el carácter.</span><span class="sxs-lookup"><span data-stu-id="bd08b-118">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




