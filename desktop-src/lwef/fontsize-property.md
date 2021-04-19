---
title: Propiedad fontSize (objeto Commands)
description: Propiedad fontSize
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84d5eb966dd7d0605bd0e4f17674fe4499bab6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105720209"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="c3686-103">Propiedad fontSize (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="c3686-103">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="c3686-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3686-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c3686-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="c3686-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c3686-106">Devuelve o establece el tamaño de fuente utilizado en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="c3686-106">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="c3686-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="c3686-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c3686-108">\*Caracteres Agent. \***("**_CharacterID_\*_"). Commands. FontSize_( \*  \[  =  *puntos* )\]</span><span class="sxs-lookup"><span data-stu-id="c3686-108">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="c3686-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c3686-109">Part</span></span>     | <span data-ttu-id="c3686-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3686-110">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="c3686-111">*Cima*</span><span class="sxs-lookup"><span data-stu-id="c3686-111">*Points*</span></span> | <span data-ttu-id="c3686-112">Valor entero largo que especifica el tamaño de fuente en puntos.</span><span class="sxs-lookup"><span data-stu-id="c3686-112">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3686-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3686-113">Remarks</span></span>

<span data-ttu-id="c3686-114">La propiedad **FontSize** define el tamaño en puntos de la fuente utilizada para mostrar texto en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="c3686-114">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="c3686-115">El valor predeterminado de la configuración de fuente se basa en la configuración de fuente de menú para la configuración de **LanguageID** del carácter, o bien, si no está establecida, la configuración de idioma predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="c3686-115">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="c3686-116">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c3686-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




