---
title: Evento DefaultCharacterChange
description: Evento DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418896"
---
# <a name="defaultcharacterchange-event"></a><span data-ttu-id="d8a7e-103">Evento DefaultCharacterChange</span><span class="sxs-lookup"><span data-stu-id="d8a7e-103">DefaultCharacterChange Event</span></span>

<span data-ttu-id="d8a7e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8a7e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d8a7e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="d8a7e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d8a7e-106">Se produce cuando el usuario cambia el carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d8a7e-106">Occurs when the user changes the default character.</span></span>

</dd> <dt>

<span data-ttu-id="d8a7e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="d8a7e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d8a7e-108">**Sub** *Agent. \* \* \* DefaultCharacterChange* \*  **(ByVal** *GUID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="d8a7e-108">**Sub** *agent.\*\*\*DefaultCharacterChange*\* **(ByVal** *GUID\*\*\*)*\*</span></span>



| <span data-ttu-id="d8a7e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d8a7e-109">Part</span></span>   | <span data-ttu-id="d8a7e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8a7e-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="d8a7e-111">*GUID*</span><span class="sxs-lookup"><span data-stu-id="d8a7e-111">*GUID*</span></span> | <span data-ttu-id="d8a7e-112">Devuelve el identificador único del carácter.</span><span class="sxs-lookup"><span data-stu-id="d8a7e-112">Returns the unique identifier for the character.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="d8a7e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8a7e-113">Remarks</span></span>

<span data-ttu-id="d8a7e-114">Este evento indica que el usuario ha cambiado el carácter asignado como el carácter predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="d8a7e-114">This event indicates when the user has changed the character assigned as the user's default character.</span></span> <span data-ttu-id="d8a7e-115">El servidor solo lo envía a los clientes que han cargado el carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d8a7e-115">The server sends this only to clients that have loaded the default character.</span></span>

<span data-ttu-id="d8a7e-116">Cuando aparece el nuevo carácter, se da por supuesto que tiene el mismo tamaño que cualquier instancia ya cargada del carácter o el carácter predeterminado anterior (en ese orden).</span><span class="sxs-lookup"><span data-stu-id="d8a7e-116">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

### <a name="see-also"></a><span data-ttu-id="d8a7e-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8a7e-117">See Also</span></span>

<span data-ttu-id="d8a7e-118">[**Método ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **Load (método** )](load-method.md)</span><span class="sxs-lookup"><span data-stu-id="d8a7e-118">[**ShowDefaultCharacterProperties method**](showdefaultcharacterproperties-method.md), [**Load method**](load-method.md)</span></span>


 

 




