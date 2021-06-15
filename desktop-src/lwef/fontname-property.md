---
title: Propiedad FontName (objeto Commands)
description: Obtenga información sobre la propiedad de objeto FontName Commands. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068261"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="0f26c-104">Propiedad FontName (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="0f26c-104">FontName Property (Commands Object)</span></span>

<span data-ttu-id="0f26c-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0f26c-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0f26c-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f26c-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0f26c-107">Devuelve o establece la fuente utilizada en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="0f26c-107">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="0f26c-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="0f26c-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0f26c-109">*agent.\***Caracteres("**_CharacterID_*_"). Commands.FontName_ \*  \[  =  *Font*\]</span><span class="sxs-lookup"><span data-stu-id="0f26c-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="0f26c-110">Parte</span><span class="sxs-lookup"><span data-stu-id="0f26c-110">Part</span></span>   | <span data-ttu-id="0f26c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f26c-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="0f26c-112">*Fuente*</span><span class="sxs-lookup"><span data-stu-id="0f26c-112">*Font*</span></span> | <span data-ttu-id="0f26c-113">Valor de cadena correspondiente al nombre de la fuente.</span><span class="sxs-lookup"><span data-stu-id="0f26c-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f26c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f26c-114">Remarks</span></span>

<span data-ttu-id="0f26c-115">La **propiedad FontName** define la fuente utilizada para mostrar texto en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="0f26c-115">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="0f26c-116">El valor predeterminado de la configuración de fuente se basa en la configuración de fuente del menú para la configuración **de LanguageID** del carácter o, si no se establece, en la configuración del identificador de idioma predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f26c-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="0f26c-117">Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0f26c-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




