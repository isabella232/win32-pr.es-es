---
title: Propiedad fontSize (objeto Balloon)
description: Propiedad fontSize
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569c07e98fb8bf973a554e89655f71e816b4a51b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421845"
---
# <a name="fontsize-property-balloon-object"></a><span data-ttu-id="ed3b2-103">Propiedad fontSize (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="ed3b2-103">FontSize Property (Balloon Object)</span></span>

<span data-ttu-id="ed3b2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ed3b2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ed3b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="ed3b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ed3b2-106">Devuelve o establece el tamaño de fuente admitido para el globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-106">Returns or sets the font size supported for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="ed3b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="ed3b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ed3b2-108">Caracteres del agente *. \* \* \*\* \*  **("**_CharacterID_*_"). Globo. FontSize_\* \[  =  *Points*\]</span><span class="sxs-lookup"><span data-stu-id="ed3b2-108">*agent.\*\*\*Characters*\* **("**_CharacterID_*_").Balloon.FontSize_* \[ = *Points*\]</span></span>



| <span data-ttu-id="ed3b2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ed3b2-109">Part</span></span>     | <span data-ttu-id="ed3b2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed3b2-110">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="ed3b2-111">*Cima*</span><span class="sxs-lookup"><span data-stu-id="ed3b2-111">*Points*</span></span> | <span data-ttu-id="ed3b2-112">Valor entero largo que especifica el tamaño de fuente en puntos.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-112">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed3b2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed3b2-113">Remarks</span></span>

<span data-ttu-id="ed3b2-114">La propiedad [**FontSize**](fontsize-property.md) devuelve un valor entero largo que especifica el tamaño de fuente actual en puntos.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-114">The [**FontSize**](fontsize-property.md) property returns a Long integer value specifying the current font size in points.</span></span> <span data-ttu-id="ed3b2-115">El valor máximo de **FontSize** es 2160 puntos.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-115">The maximum value for **FontSize** is 2160 points.</span></span>

<span data-ttu-id="ed3b2-116">El valor predeterminado de la configuración de fuente del globo de palabras de un carácter se establece en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="ed3b2-117">Además, el usuario puede invalidar la configuración de fuente para todos los caracteres de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ed3b2-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




