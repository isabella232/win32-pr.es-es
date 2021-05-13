---
description: Obtiene el estado de la cuenta del usuario.
title: Propiedad DIDiskQuotaUser.AccountStatus
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
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841656"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="80e43-103">Propiedad DIDiskQuotaUser.AccountStatus</span><span class="sxs-lookup"><span data-stu-id="80e43-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="80e43-104">Obtiene el estado de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="80e43-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="80e43-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80e43-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e43-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80e43-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="80e43-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="80e43-107">Property value</span></span>

<span data-ttu-id="80e43-108">Esta propiedad puede tomar uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="80e43-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="80e43-109">Estado</span><span class="sxs-lookup"><span data-stu-id="80e43-109">Status</span></span>            | <span data-ttu-id="80e43-110">Value</span><span class="sxs-lookup"><span data-stu-id="80e43-110">Value</span></span> | <span data-ttu-id="80e43-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="80e43-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="80e43-112">dqAcctResolved</span><span class="sxs-lookup"><span data-stu-id="80e43-112">dqAcctResolved</span></span>    | <span data-ttu-id="80e43-113">0</span><span class="sxs-lookup"><span data-stu-id="80e43-113">0</span></span>     | <span data-ttu-id="80e43-114">Se resuelve la información de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="80e43-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="80e43-115">dqAcctUnavailable</span><span class="sxs-lookup"><span data-stu-id="80e43-115">dqAcctUnavailable</span></span> | <span data-ttu-id="80e43-116">1</span><span class="sxs-lookup"><span data-stu-id="80e43-116">1</span></span>     | <span data-ttu-id="80e43-117">La información de la cuenta no está disponible.</span><span class="sxs-lookup"><span data-stu-id="80e43-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="80e43-118">dqAcctDeleted</span><span class="sxs-lookup"><span data-stu-id="80e43-118">dqAcctDeleted</span></span>     | <span data-ttu-id="80e43-119">2</span><span class="sxs-lookup"><span data-stu-id="80e43-119">2</span></span>     | <span data-ttu-id="80e43-120">Se ha eliminado la cuenta.</span><span class="sxs-lookup"><span data-stu-id="80e43-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="80e43-121">dqAcctInvalid</span><span class="sxs-lookup"><span data-stu-id="80e43-121">dqAcctInvalid</span></span>     | <span data-ttu-id="80e43-122">3</span><span class="sxs-lookup"><span data-stu-id="80e43-122">3</span></span>     | <span data-ttu-id="80e43-123">La cuenta no es válida.</span><span class="sxs-lookup"><span data-stu-id="80e43-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="80e43-124">dqAcctUnknown</span><span class="sxs-lookup"><span data-stu-id="80e43-124">dqAcctUnknown</span></span>     | <span data-ttu-id="80e43-125">4</span><span class="sxs-lookup"><span data-stu-id="80e43-125">4</span></span>     | <span data-ttu-id="80e43-126">No se encuentra la cuenta.</span><span class="sxs-lookup"><span data-stu-id="80e43-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="80e43-127">dqAcctUnresolved</span><span class="sxs-lookup"><span data-stu-id="80e43-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="80e43-128">5</span><span class="sxs-lookup"><span data-stu-id="80e43-128">5</span></span>     | <span data-ttu-id="80e43-129">La información de la cuenta no está resuelta.</span><span class="sxs-lookup"><span data-stu-id="80e43-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="80e43-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80e43-130">Requirements</span></span>



| <span data-ttu-id="80e43-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e43-131">Requirement</span></span> | <span data-ttu-id="80e43-132">Value</span><span class="sxs-lookup"><span data-stu-id="80e43-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e43-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80e43-133">Minimum supported client</span></span><br/> | <span data-ttu-id="80e43-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="80e43-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80e43-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80e43-135">Minimum supported server</span></span><br/> | <span data-ttu-id="80e43-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="80e43-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="80e43-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80e43-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80e43-138"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="80e43-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80e43-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="80e43-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e43-140">**DIDiskQuotaUser (objeto)**</span><span class="sxs-lookup"><span data-stu-id="80e43-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




