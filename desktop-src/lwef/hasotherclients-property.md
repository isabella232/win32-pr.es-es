---
title: Propiedad HasOtherClients
description: Propiedad HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075752"
---
# <a name="hasotherclients-property"></a><span data-ttu-id="493c4-103">Propiedad HasOtherClients</span><span class="sxs-lookup"><span data-stu-id="493c4-103">HasOtherClients Property</span></span>

<span data-ttu-id="493c4-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="493c4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="493c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="493c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="493c4-106">Devuelve si otras aplicaciones están usando el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="493c4-106">Returns whether the specified character is in use by other applications.</span></span>

</dd> <dt>

<span data-ttu-id="493c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="493c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="493c4-108">*agente*. **Caracteres ("***CharacterID***"). HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="493c4-108">*agent*.**Characters("***CharacterID***").HasOtherClients**</span></span>



| <span data-ttu-id="493c4-109">Value</span><span class="sxs-lookup"><span data-stu-id="493c4-109">Value</span></span>     | <span data-ttu-id="493c4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="493c4-110">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="493c4-111">**True**</span><span class="sxs-lookup"><span data-stu-id="493c4-111">**True**</span></span>  | <span data-ttu-id="493c4-112">El carácter tiene otros clientes.</span><span class="sxs-lookup"><span data-stu-id="493c4-112">The character has other clients.</span></span>           |
| <span data-ttu-id="493c4-113">**False**</span><span class="sxs-lookup"><span data-stu-id="493c4-113">**False**</span></span> | <span data-ttu-id="493c4-114">El carácter no tiene otros clientes.</span><span class="sxs-lookup"><span data-stu-id="493c4-114">The character does not have other clients.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="493c4-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="493c4-115">Remarks</span></span>

<span data-ttu-id="493c4-116">Puede usar esta propiedad para determinar si la aplicación es el único o el último cliente del carácter, cuando más de una aplicación comparte (ha cargado) el mismo carácter.</span><span class="sxs-lookup"><span data-stu-id="493c4-116">You can use this property to determine whether your application is the only or last client of the character, when more than one application is sharing (has loaded) the same character.</span></span>

 

 




