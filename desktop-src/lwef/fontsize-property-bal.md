---
title: Propiedad FontSize (objeto Balloon)
description: Obtenga información sobre la propiedad de objeto FontSize Balloon. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a2c13708d3066faaf396a3a451c9be01d177
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068223"
---
# <a name="fontsize-property-balloon-object"></a><span data-ttu-id="09967-104">Propiedad FontSize (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="09967-104">FontSize Property (Balloon Object)</span></span>

<span data-ttu-id="09967-105">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09967-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="09967-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="09967-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="09967-107">Devuelve o establece el tamaño de fuente admitido para el globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="09967-107">Returns or sets the font size supported for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="09967-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="09967-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="09967-109">*agent.:Characters* \*  **("**_CharacterID_*_"). Puntos Balloon.FontSize_* \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="09967-109">*agent.\*\*\*Characters*\* **("**_CharacterID_*_").Balloon.FontSize_* \[ = *Points*\]</span></span>



| <span data-ttu-id="09967-110">Parte</span><span class="sxs-lookup"><span data-stu-id="09967-110">Part</span></span>     | <span data-ttu-id="09967-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="09967-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="09967-112">*Puntos*</span><span class="sxs-lookup"><span data-stu-id="09967-112">*Points*</span></span> | <span data-ttu-id="09967-113">Valor entero Long que especifica el tamaño de fuente en puntos.</span><span class="sxs-lookup"><span data-stu-id="09967-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09967-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09967-114">Remarks</span></span>

<span data-ttu-id="09967-115">La [**propiedad FontSize**](fontsize-property.md) devuelve un valor entero Long que especifica el tamaño de fuente actual en puntos.</span><span class="sxs-lookup"><span data-stu-id="09967-115">The [**FontSize**](fontsize-property.md) property returns a Long integer value specifying the current font size in points.</span></span> <span data-ttu-id="09967-116">El valor máximo de **FontSize** es 2160 puntos.</span><span class="sxs-lookup"><span data-stu-id="09967-116">The maximum value for **FontSize** is 2160 points.</span></span>

<span data-ttu-id="09967-117">El valor predeterminado de la configuración de fuente del globo de palabras de un carácter se establece en el Editor de caracteres de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="09967-117">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="09967-118">Además, el usuario puede invalidar la configuración de fuente de todos los caracteres de la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="09967-118">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




