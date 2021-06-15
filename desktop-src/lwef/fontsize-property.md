---
title: Propiedad FontSize (objeto Commands)
description: Obtenga información sobre la propiedad de objeto FontSize Commands. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d4e32bf57d129e7bf1d7b45f97846a1fe90756
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068212"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="04950-104">Propiedad FontSize (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="04950-104">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="04950-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04950-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="04950-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04950-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="04950-107">Devuelve o establece el tamaño de fuente utilizado en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="04950-107">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="04950-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="04950-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="04950-109">*agent.\***Characters("**_CharacterID_*_"). Commands.FontSize_ \*  \[  =  *Points*\]</span><span class="sxs-lookup"><span data-stu-id="04950-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="04950-110">Parte</span><span class="sxs-lookup"><span data-stu-id="04950-110">Part</span></span>     | <span data-ttu-id="04950-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="04950-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="04950-112">*Puntos*</span><span class="sxs-lookup"><span data-stu-id="04950-112">*Points*</span></span> | <span data-ttu-id="04950-113">Valor entero Long que especifica el tamaño de fuente en puntos.</span><span class="sxs-lookup"><span data-stu-id="04950-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04950-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04950-114">Remarks</span></span>

<span data-ttu-id="04950-115">La **propiedad FontSize** define el tamaño de punto de la fuente utilizada para mostrar texto en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="04950-115">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="04950-116">El valor predeterminado de la configuración de fuente se basa en la configuración de fuente del menú para la configuración **de LanguageID** del carácter o, si no se establece, en la configuración de idioma predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="04950-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="04950-117">Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter ni a otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="04950-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




