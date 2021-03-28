---
description: Obtiene el estado de la cuenta del usuario.
title: Propiedad DIDiskQuotaUser. Estados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: 155ae627d70c5125fd0d1d501062224450fc8e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984290"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="5a39c-103">Propiedad DIDiskQuotaUser. Estados</span><span class="sxs-lookup"><span data-stu-id="5a39c-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="5a39c-104">Obtiene el estado de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="5a39c-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="5a39c-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5a39c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a39c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a39c-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="5a39c-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5a39c-107">Property value</span></span>

<span data-ttu-id="5a39c-108">Esta propiedad puede tomar uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5a39c-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="5a39c-109">Estado</span><span class="sxs-lookup"><span data-stu-id="5a39c-109">Status</span></span>            | <span data-ttu-id="5a39c-110">Value</span><span class="sxs-lookup"><span data-stu-id="5a39c-110">Value</span></span> | <span data-ttu-id="5a39c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a39c-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="5a39c-112">dqAcctResolved</span><span class="sxs-lookup"><span data-stu-id="5a39c-112">dqAcctResolved</span></span>    | <span data-ttu-id="5a39c-113">0</span><span class="sxs-lookup"><span data-stu-id="5a39c-113">0</span></span>     | <span data-ttu-id="5a39c-114">Se resolvió la información de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="5a39c-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="5a39c-115">dqAcctUnavailable</span><span class="sxs-lookup"><span data-stu-id="5a39c-115">dqAcctUnavailable</span></span> | <span data-ttu-id="5a39c-116">1</span><span class="sxs-lookup"><span data-stu-id="5a39c-116">1</span></span>     | <span data-ttu-id="5a39c-117">La información de la cuenta no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5a39c-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="5a39c-118">dqAcctDeleted</span><span class="sxs-lookup"><span data-stu-id="5a39c-118">dqAcctDeleted</span></span>     | <span data-ttu-id="5a39c-119">2</span><span class="sxs-lookup"><span data-stu-id="5a39c-119">2</span></span>     | <span data-ttu-id="5a39c-120">Se ha eliminado la cuenta.</span><span class="sxs-lookup"><span data-stu-id="5a39c-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="5a39c-121">dqAcctInvalid</span><span class="sxs-lookup"><span data-stu-id="5a39c-121">dqAcctInvalid</span></span>     | <span data-ttu-id="5a39c-122">3</span><span class="sxs-lookup"><span data-stu-id="5a39c-122">3</span></span>     | <span data-ttu-id="5a39c-123">La cuenta no es válida.</span><span class="sxs-lookup"><span data-stu-id="5a39c-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="5a39c-124">dqAcctUnknown</span><span class="sxs-lookup"><span data-stu-id="5a39c-124">dqAcctUnknown</span></span>     | <span data-ttu-id="5a39c-125">4</span><span class="sxs-lookup"><span data-stu-id="5a39c-125">4</span></span>     | <span data-ttu-id="5a39c-126">No se encuentra la cuenta.</span><span class="sxs-lookup"><span data-stu-id="5a39c-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="5a39c-127">dqAcctUnresolved</span><span class="sxs-lookup"><span data-stu-id="5a39c-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="5a39c-128">5</span><span class="sxs-lookup"><span data-stu-id="5a39c-128">5</span></span>     | <span data-ttu-id="5a39c-129">La información de la cuenta no está resuelta.</span><span class="sxs-lookup"><span data-stu-id="5a39c-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="5a39c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a39c-130">Requirements</span></span>



| <span data-ttu-id="5a39c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a39c-131">Requirement</span></span> | <span data-ttu-id="5a39c-132">Value</span><span class="sxs-lookup"><span data-stu-id="5a39c-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a39c-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a39c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5a39c-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5a39c-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a39c-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a39c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5a39c-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a39c-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5a39c-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a39c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a39c-138"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5a39c-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a39c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a39c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a39c-140">**Objeto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="5a39c-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




