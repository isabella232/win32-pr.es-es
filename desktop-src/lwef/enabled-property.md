---
title: Propiedad Enabled (objeto Balloon)
description: Propiedad Enabled
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695824"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="6552b-103">Propiedad Enabled (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="6552b-103">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="6552b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6552b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6552b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="6552b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6552b-106">Devuelve si el globo de palabras está habilitado para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="6552b-106">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="6552b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="6552b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6552b-108">\*agente \***. Caracteres ("**_CharacterID_*_"). Globo. Enabled_*</span><span class="sxs-lookup"><span data-stu-id="6552b-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="6552b-109">Value</span><span class="sxs-lookup"><span data-stu-id="6552b-109">Value</span></span>     | <span data-ttu-id="6552b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6552b-110">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="6552b-111">**True**</span><span class="sxs-lookup"><span data-stu-id="6552b-111">**True**</span></span>  | <span data-ttu-id="6552b-112">El globo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6552b-112">The balloon is enabled.</span></span>  |
| <span data-ttu-id="6552b-113">**False**</span><span class="sxs-lookup"><span data-stu-id="6552b-113">**False**</span></span> | <span data-ttu-id="6552b-114">El globo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="6552b-114">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6552b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6552b-115">Remarks</span></span>

<span data-ttu-id="6552b-116">La propiedad **Enabled** devuelve un valor booleano que especifica si el globo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6552b-116">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="6552b-117">El estado predeterminado de globo de palabras se establece como parte de la definición de un carácter cuando el carácter se compila en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6552b-117">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="6552b-118">Si se define un carácter para que no admita el globo de palabras, esta propiedad siempre será **false** para el carácter.</span><span class="sxs-lookup"><span data-stu-id="6552b-118">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




