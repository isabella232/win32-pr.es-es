---
title: Propiedad Name (objeto Characters)
description: Obtenga información sobre la propiedad Name del objeto Characters. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7365550d5d4d4071cf4292e505f16e7047628cf1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989330"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="7d5de-104">Propiedad Name (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="7d5de-104">Name Property (Characters Object)</span></span>

<span data-ttu-id="7d5de-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7d5de-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7d5de-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d5de-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7d5de-107">Devuelve o establece una cadena que especifica el nombre predeterminado del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="7d5de-107">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="7d5de-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="7d5de-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7d5de-109">*agent\***. Caracteres ("**_CharacterID_*_"). Cadena de_ \*  \[  =  *nombre*\]</span><span class="sxs-lookup"><span data-stu-id="7d5de-109">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="7d5de-110">Parte</span><span class="sxs-lookup"><span data-stu-id="7d5de-110">Part</span></span>     | <span data-ttu-id="7d5de-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d5de-111">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5de-112">*string*</span><span class="sxs-lookup"><span data-stu-id="7d5de-112">*string*</span></span> | <span data-ttu-id="7d5de-113">Valor de cadena correspondiente al nombre del carácter (en la configuración de idioma actual).</span><span class="sxs-lookup"><span data-stu-id="7d5de-113">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d5de-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d5de-114">Remarks</span></span>

<span data-ttu-id="7d5de-115">El nombre de un **carácter** puede depender de la configuración [**de LanguageID del**](languageid-property.md) carácter.</span><span class="sxs-lookup"><span data-stu-id="7d5de-115">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="7d5de-116">El nombre de un carácter en un idioma puede ser diferente o usar caracteres diferentes que en otro.</span><span class="sxs-lookup"><span data-stu-id="7d5de-116">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="7d5de-117">El nombre predeterminado del **carácter para** un idioma específico se define cuando el carácter se compila con el Editor de caracteres del Agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d5de-117">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="7d5de-118">Evite cambiar el nombre de un carácter, especialmente cuando se usa en un escenario en el que otras aplicaciones cliente pueden usar el mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="7d5de-118">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="7d5de-119">Además, el Agente usa el nombre **del** carácter para crear automáticamente comandos para ocultar y mostrar el carácter.</span><span class="sxs-lookup"><span data-stu-id="7d5de-119">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




