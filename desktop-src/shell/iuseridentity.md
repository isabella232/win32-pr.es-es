---
description: IUserIdentity no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interfaz IUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985402"
---
# <a name="iuseridentity-interface"></a><span data-ttu-id="4dad8-104">Interfaz IUserIdentity</span><span class="sxs-lookup"><span data-stu-id="4dad8-104">IUserIdentity interface</span></span>

<span data-ttu-id="4dad8-105">\[**IUserIdentity** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="4dad8-105">\[**IUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="4dad8-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="4dad8-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="4dad8-107">Expone métodos que proporcionan datos de identificación, registro y carpeta para una identidad de usuario específica.</span><span class="sxs-lookup"><span data-stu-id="4dad8-107">Exposes methods that provide identification, registry, and folder data for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="4dad8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4dad8-108">Members</span></span>

<span data-ttu-id="4dad8-109">La interfaz **IUserIdentity** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4dad8-109">The **IUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4dad8-110">**IUserIdentity** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4dad8-110">**IUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="4dad8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4dad8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4dad8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4dad8-112">Methods</span></span>

<span data-ttu-id="4dad8-113">La interfaz **IUserIdentity** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4dad8-113">The **IUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="4dad8-114">Método</span><span class="sxs-lookup"><span data-stu-id="4dad8-114">Method</span></span>                                                         | <span data-ttu-id="4dad8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dad8-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4dad8-116">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="4dad8-116">**GetCookie**</span></span>](iuseridentity-getcookie.md)                   | <span data-ttu-id="4dad8-117">En desuso.</span><span class="sxs-lookup"><span data-stu-id="4dad8-117">Deprecated.</span></span> <span data-ttu-id="4dad8-118">Obtiene la cookie usada para identificar de forma única esta identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="4dad8-118">Gets the cookie used to uniquely identify this user identity.</span></span><br/>             |
| [<span data-ttu-id="4dad8-119">**GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="4dad8-119">**GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)   | <span data-ttu-id="4dad8-120">En desuso.</span><span class="sxs-lookup"><span data-stu-id="4dad8-120">Deprecated.</span></span> <span data-ttu-id="4dad8-121">Obtiene la carpeta de archivos asociada a esta identidad.</span><span class="sxs-lookup"><span data-stu-id="4dad8-121">Gets the file folder associated with this identity.</span></span><br/>                       |
| [<span data-ttu-id="4dad8-122">**GetName**</span><span class="sxs-lookup"><span data-stu-id="4dad8-122">**GetName**</span></span>](iuseridentity-getname.md)                       | <span data-ttu-id="4dad8-123">En desuso.</span><span class="sxs-lookup"><span data-stu-id="4dad8-123">Deprecated.</span></span> <span data-ttu-id="4dad8-124">Obtiene el nombre asociado a esta identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="4dad8-124">Gets the name associated with this user identity.</span></span><br/>                         |
| [<span data-ttu-id="4dad8-125">**OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="4dad8-125">**OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md) | <span data-ttu-id="4dad8-126">En desuso.</span><span class="sxs-lookup"><span data-stu-id="4dad8-126">Deprecated.</span></span> <span data-ttu-id="4dad8-127">Recupera la clave del registro que corresponde a esta identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="4dad8-127">Retrieves the key in the registry that corresponds to this user identity.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4dad8-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dad8-128">Remarks</span></span>

<span data-ttu-id="4dad8-129">Esta interfaz proporciona información que corresponde a una identidad de usuario específica presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="4dad8-129">This interface provides information that corresponds to a specific user identity present on the system.</span></span> <span data-ttu-id="4dad8-130">Puede tener acceso a la carpeta de identidad de esta identidad de usuario, su clave del registro y su cookie de identificación, así como recuperar el nombre asociado a la identidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="4dad8-130">You can access this user identity's identity folder, its registry key, and its identification cookie, as well as retrieve the name associated with the user identity.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dad8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dad8-131">Requirements</span></span>



| <span data-ttu-id="4dad8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dad8-132">Requirement</span></span> | <span data-ttu-id="4dad8-133">Value</span><span class="sxs-lookup"><span data-stu-id="4dad8-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4dad8-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dad8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4dad8-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4dad8-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4dad8-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dad8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4dad8-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4dad8-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4dad8-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4dad8-138">End of client support</span></span><br/>    | <span data-ttu-id="4dad8-139">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4dad8-139">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="4dad8-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4dad8-140">End of server support</span></span><br/>    | <span data-ttu-id="4dad8-141">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4dad8-141">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="4dad8-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4dad8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dad8-143"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dad8-143"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="4dad8-144">IDL</span><span class="sxs-lookup"><span data-stu-id="4dad8-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4dad8-145"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4dad8-145"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="4dad8-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4dad8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dad8-147"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dad8-147"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dad8-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dad8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dad8-149">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="4dad8-149">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="4dad8-150">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="4dad8-150">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="4dad8-151">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="4dad8-151">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> </dl>

 

 
