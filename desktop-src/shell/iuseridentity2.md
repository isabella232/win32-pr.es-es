---
description: IUserIdentity2 no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Interfaz IUserIdentity2 (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539484"
---
# <a name="iuseridentity2-interface"></a><span data-ttu-id="a8e49-104">Interfaz IUserIdentity2</span><span class="sxs-lookup"><span data-stu-id="a8e49-104">IUserIdentity2 interface</span></span>

<span data-ttu-id="a8e49-105">\[**IUserIdentity2** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="a8e49-105">\[**IUserIdentity2** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a8e49-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="a8e49-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="a8e49-107">Expone métodos que proporcionan nombres, contraseñas y controles ordinales para una identidad de usuario específica.</span><span class="sxs-lookup"><span data-stu-id="a8e49-107">Exposes methods that provide naming, password, and ordinal control for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="a8e49-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8e49-108">Members</span></span>

<span data-ttu-id="a8e49-109">La interfaz **IUserIdentity2** hereda de [**IUserIdentity**](iuseridentity.md).</span><span class="sxs-lookup"><span data-stu-id="a8e49-109">The **IUserIdentity2** interface inherits from [**IUserIdentity**](iuseridentity.md).</span></span> <span data-ttu-id="a8e49-110">**IUserIdentity2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a8e49-110">**IUserIdentity2** also has these types of members:</span></span>

-   [<span data-ttu-id="a8e49-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8e49-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a8e49-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a8e49-112">Methods</span></span>

<span data-ttu-id="a8e49-113">La interfaz **IUserIdentity2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a8e49-113">The **IUserIdentity2** interface has these methods.</span></span>



| <span data-ttu-id="a8e49-114">Método</span><span class="sxs-lookup"><span data-stu-id="a8e49-114">Method</span></span>                                                  | <span data-ttu-id="a8e49-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8e49-115">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="a8e49-116">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="a8e49-116">**ChangePassword**</span></span>](iuseridentity2-changepassword.md) | <span data-ttu-id="a8e49-117">En desuso.</span><span class="sxs-lookup"><span data-stu-id="a8e49-117">Deprecated.</span></span> <span data-ttu-id="a8e49-118">Establece una nueva contraseña para la identidad.</span><span class="sxs-lookup"><span data-stu-id="a8e49-118">Sets a new password for the identity.</span></span><br/>      |
| [<span data-ttu-id="a8e49-119">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="a8e49-119">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)         | <span data-ttu-id="a8e49-120">En desuso.</span><span class="sxs-lookup"><span data-stu-id="a8e49-120">Deprecated.</span></span> <span data-ttu-id="a8e49-121">Obtiene el número ordinal de esta identidad.</span><span class="sxs-lookup"><span data-stu-id="a8e49-121">Gets the ordinal number for this identity.</span></span><br/> |
| [<span data-ttu-id="a8e49-122">**SetName**</span><span class="sxs-lookup"><span data-stu-id="a8e49-122">**SetName**</span></span>](iuseridentity2-setname.md)               | <span data-ttu-id="a8e49-123">En desuso.</span><span class="sxs-lookup"><span data-stu-id="a8e49-123">Deprecated.</span></span> <span data-ttu-id="a8e49-124">Establece el nombre para mostrar de la identidad.</span><span class="sxs-lookup"><span data-stu-id="a8e49-124">Sets the display name of the identity.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="a8e49-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8e49-125">Remarks</span></span>

<span data-ttu-id="a8e49-126">Esta interfaz también proporciona los métodos de la interfaz [**IUserIdentity**](iuseridentity.md) , de la que hereda.</span><span class="sxs-lookup"><span data-stu-id="a8e49-126">This interface also provides the methods of the [**IUserIdentity**](iuseridentity.md) interface, from which it inherits.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e49-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8e49-127">Requirements</span></span>



| <span data-ttu-id="a8e49-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8e49-128">Requirement</span></span> | <span data-ttu-id="a8e49-129">Value</span><span class="sxs-lookup"><span data-stu-id="a8e49-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e49-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8e49-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e49-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a8e49-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a8e49-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8e49-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e49-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a8e49-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a8e49-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a8e49-134">End of client support</span></span><br/>    | <span data-ttu-id="a8e49-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a8e49-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a8e49-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a8e49-136">End of server support</span></span><br/>    | <span data-ttu-id="a8e49-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a8e49-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a8e49-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8e49-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8e49-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e49-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8e49-140">IDL</span><span class="sxs-lookup"><span data-stu-id="a8e49-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8e49-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8e49-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8e49-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8e49-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8e49-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8e49-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8e49-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8e49-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e49-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="a8e49-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> </dl>

 

 




