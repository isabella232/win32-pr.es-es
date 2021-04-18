---
title: Propiedad FontStrikeThru
description: Propiedad FontStrikeThru
ms.assetid: 2d87fded-2f3e-44cd-b2a5-5f9c76ca1cf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e1ac8874a11832025dd225aa4df4afa91b4d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105720077"
---
# <a name="fontstrikethru-property"></a><span data-ttu-id="142f7-103">Propiedad FontStrikeThru</span><span class="sxs-lookup"><span data-stu-id="142f7-103">FontStrikeThru Property</span></span>

<span data-ttu-id="142f7-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="142f7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="142f7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="142f7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="142f7-106">Devuelve el estilo de fuente que se muestra actualmente en la ventana de globo de palabras para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="142f7-106">Returns the font style currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="142f7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="142f7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="142f7-108">*agente ***. Caracteres ("*** CharacterID \* *"). Balloon. FontStrikeThru**</span><span class="sxs-lookup"><span data-stu-id="142f7-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontStrikeThru*\*</span></span>



| <span data-ttu-id="142f7-109">Value</span><span class="sxs-lookup"><span data-stu-id="142f7-109">Value</span></span>     | <span data-ttu-id="142f7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="142f7-110">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="142f7-111">**True**</span><span class="sxs-lookup"><span data-stu-id="142f7-111">**True**</span></span>  | <span data-ttu-id="142f7-112">La fuente del globo utiliza el efecto de tachado.</span><span class="sxs-lookup"><span data-stu-id="142f7-112">The balloon font uses the strikethrough effect.</span></span>         |
| <span data-ttu-id="142f7-113">**False**</span><span class="sxs-lookup"><span data-stu-id="142f7-113">**False**</span></span> | <span data-ttu-id="142f7-114">La fuente del globo no utiliza el efecto de tachado.</span><span class="sxs-lookup"><span data-stu-id="142f7-114">The balloon font does not use the strikethrough effect.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="142f7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="142f7-115">Remarks</span></span>

<span data-ttu-id="142f7-116">El valor predeterminado de la configuración de fuente del globo de palabras de un carácter se establece en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="142f7-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="142f7-117">Además, el usuario puede invalidar la configuración de fuente para todos los caracteres de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="142f7-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




