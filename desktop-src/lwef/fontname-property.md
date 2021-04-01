---
title: FontName (propiedad, objeto Commands)
description: FontName (propiedad)
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b04fa386958a75b55f9cfc50a9149de454d48f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149819"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="eb02a-103">FontName (propiedad, objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="eb02a-103">FontName Property (Commands Object)</span></span>

<span data-ttu-id="eb02a-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb02a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="eb02a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="eb02a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="eb02a-106">Devuelve o establece la fuente utilizada en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="eb02a-106">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="eb02a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="eb02a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="eb02a-108">\*Caracteres Agent. \***("**_CharacterID_\*_"). Fuente Commands. FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="eb02a-108">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="eb02a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="eb02a-109">Part</span></span>   | <span data-ttu-id="eb02a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb02a-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="eb02a-111">*Fuente*</span><span class="sxs-lookup"><span data-stu-id="eb02a-111">*Font*</span></span> | <span data-ttu-id="eb02a-112">Valor de cadena que corresponde al nombre de la fuente.</span><span class="sxs-lookup"><span data-stu-id="eb02a-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb02a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb02a-113">Remarks</span></span>

<span data-ttu-id="eb02a-114">La propiedad **FontName** define la fuente utilizada para mostrar texto en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="eb02a-114">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="eb02a-115">El valor predeterminado de la configuración de fuente se basa en la configuración de fuente de menú para la configuración de **LanguageID** del carácter, o bien, si no se establece, la configuración de identificador de idioma predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="eb02a-115">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="eb02a-116">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="eb02a-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




