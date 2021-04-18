---
description: IEnumUserIdentity no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Interfaz IEnumUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985411"
---
# <a name="ienumuseridentity-interface"></a><span data-ttu-id="16b0b-104">Interfaz IEnumUserIdentity</span><span class="sxs-lookup"><span data-stu-id="16b0b-104">IEnumUserIdentity interface</span></span>

<span data-ttu-id="16b0b-105">\[**IEnumUserIdentity** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="16b0b-105">\[**IEnumUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="16b0b-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="16b0b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="16b0b-107">Proporciona la enumeración de todas las identidades de usuario presentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="16b0b-107">Provides enumeration of all user identities present on the system.</span></span>

## <a name="members"></a><span data-ttu-id="16b0b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="16b0b-108">Members</span></span>

<span data-ttu-id="16b0b-109">La interfaz **IEnumUserIdentity** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="16b0b-109">The **IEnumUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="16b0b-110">**IEnumUserIdentity** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="16b0b-110">**IEnumUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="16b0b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="16b0b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="16b0b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="16b0b-112">Methods</span></span>

<span data-ttu-id="16b0b-113">La interfaz **IEnumUserIdentity** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="16b0b-113">The **IEnumUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="16b0b-114">Método</span><span class="sxs-lookup"><span data-stu-id="16b0b-114">Method</span></span>                                         | <span data-ttu-id="16b0b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="16b0b-115">Description</span></span>                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16b0b-116">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="16b0b-116">**Clone**</span></span>](ienumuseridentity-clone.md)       | <span data-ttu-id="16b0b-117">En desuso.</span><span class="sxs-lookup"><span data-stu-id="16b0b-117">Deprecated.</span></span> <span data-ttu-id="16b0b-118">Obtiene una copia de la enumeración actual.</span><span class="sxs-lookup"><span data-stu-id="16b0b-118">Gets a copy of the current enumeration.</span></span><br/>                                                               |
| [<span data-ttu-id="16b0b-119">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="16b0b-119">**GetCount**</span></span>](ienumuseridentity-getcount.md) | <span data-ttu-id="16b0b-120">En desuso.</span><span class="sxs-lookup"><span data-stu-id="16b0b-120">Deprecated.</span></span> <span data-ttu-id="16b0b-121">Obtiene el número de identidades de usuario actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="16b0b-121">Gets the count of user identities currently on the system.</span></span><br/>                                            |
| [<span data-ttu-id="16b0b-122">**Next**</span><span class="sxs-lookup"><span data-stu-id="16b0b-122">**Next**</span></span>](ienumuseridentity-next.md)         | <span data-ttu-id="16b0b-123">En desuso.</span><span class="sxs-lookup"><span data-stu-id="16b0b-123">Deprecated.</span></span> <span data-ttu-id="16b0b-124">Recupera una matriz de interfaces de identidad de usuario de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="16b0b-124">Retrieves an array of user identity interfaces from the enumeration.</span></span><br/>                                  |
| [<span data-ttu-id="16b0b-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="16b0b-125">**Reset**</span></span>](ienumuseridentity-reset.md)       | <span data-ttu-id="16b0b-126">En desuso.</span><span class="sxs-lookup"><span data-stu-id="16b0b-126">Deprecated.</span></span> <span data-ttu-id="16b0b-127">Restablece el recuento interno de interfaces recuperadas en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="16b0b-127">Resets the internal count of retrieved interfaces in the enumeration.</span></span><br/>                                 |
| [<span data-ttu-id="16b0b-128">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="16b0b-128">**Skip**</span></span>](ienumuseridentity-skip.md)         | <span data-ttu-id="16b0b-129">En desuso.</span><span class="sxs-lookup"><span data-stu-id="16b0b-129">Deprecated.</span></span> <span data-ttu-id="16b0b-130">Omite un número determinado de interfaces de identidad de usuario en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="16b0b-130">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="16b0b-131">Se utiliza al recuperar interfaces.</span><span class="sxs-lookup"><span data-stu-id="16b0b-131">Used when retrieving interfaces.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16b0b-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16b0b-132">Remarks</span></span>

<span data-ttu-id="16b0b-133">Para recuperar información sobre las identidades de usuario presentes en el sistema, puede usar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="16b0b-133">To retrieve information about user identities present on the system, you can use this interface.</span></span> <span data-ttu-id="16b0b-134">Desde una interfaz [**IUserIdentityManager**](iuseridentitymanager.md) , puede llamar a [**IUserIdentityManager:: EnumIdentities**](iuseridentitymanager-enumidentities.md) para recuperar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="16b0b-134">From a [**IUserIdentityManager**](iuseridentitymanager.md) interface, you can call [**IUserIdentityManager::EnumIdentities**](iuseridentitymanager-enumidentities.md) to retrieve this interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="16b0b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16b0b-135">Requirements</span></span>



| <span data-ttu-id="16b0b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b0b-136">Requirement</span></span> | <span data-ttu-id="16b0b-137">Value</span><span class="sxs-lookup"><span data-stu-id="16b0b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16b0b-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16b0b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="16b0b-139">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="16b0b-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="16b0b-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16b0b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="16b0b-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="16b0b-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="16b0b-142">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="16b0b-142">End of client support</span></span><br/>    | <span data-ttu-id="16b0b-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="16b0b-143">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="16b0b-144">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="16b0b-144">End of server support</span></span><br/>    | <span data-ttu-id="16b0b-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16b0b-145">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="16b0b-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16b0b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="16b0b-147"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b0b-147"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="16b0b-148">IDL</span><span class="sxs-lookup"><span data-stu-id="16b0b-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="16b0b-149"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="16b0b-149"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="16b0b-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="16b0b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16b0b-151"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16b0b-151"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16b0b-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="16b0b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b0b-153">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="16b0b-153">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> </dl>

 

 
