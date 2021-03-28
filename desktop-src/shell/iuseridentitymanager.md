---
description: IUserIdentityManager no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Interfaz IUserIdentityManager (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907557"
---
# <a name="iuseridentitymanager-interface"></a><span data-ttu-id="13152-104">Interfaz IUserIdentityManager</span><span class="sxs-lookup"><span data-stu-id="13152-104">IUserIdentityManager interface</span></span>

<span data-ttu-id="13152-105">\[**IUserIdentityManager** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="13152-105">\[**IUserIdentityManager** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="13152-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="13152-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="13152-107">Expone métodos que identifican, enumeran y administran identidades de usuario en el sistema.</span><span class="sxs-lookup"><span data-stu-id="13152-107">Exposes methods that identify, enumerate, and manage user identities on the system.</span></span>

## <a name="members"></a><span data-ttu-id="13152-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="13152-108">Members</span></span>

<span data-ttu-id="13152-109">La interfaz **IUserIdentityManager** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="13152-109">The **IUserIdentityManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="13152-110">**IUserIdentityManager** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="13152-110">**IUserIdentityManager** also has these types of members:</span></span>

-   [<span data-ttu-id="13152-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="13152-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="13152-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="13152-112">Methods</span></span>

<span data-ttu-id="13152-113">La interfaz **IUserIdentityManager** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="13152-113">The **IUserIdentityManager** interface has these methods.</span></span>



| <span data-ttu-id="13152-114">Método</span><span class="sxs-lookup"><span data-stu-id="13152-114">Method</span></span>                                                                  | <span data-ttu-id="13152-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="13152-115">Description</span></span>                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13152-116">**EnumIdentities**</span><span class="sxs-lookup"><span data-stu-id="13152-116">**EnumIdentities**</span></span>](iuseridentitymanager-enumidentities.md)           | <span data-ttu-id="13152-117">En desuso.</span><span class="sxs-lookup"><span data-stu-id="13152-117">Deprecated.</span></span> <span data-ttu-id="13152-118">Obtiene un objeto [**IEnumUserIdentity**](ienumuseridentity.md) , que se puede utilizar para enumerar las identidades de usuario presentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="13152-118">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span><br/> |
| [<span data-ttu-id="13152-119">**GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="13152-119">**GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md) | <span data-ttu-id="13152-120">En desuso.</span><span class="sxs-lookup"><span data-stu-id="13152-120">Deprecated.</span></span> <span data-ttu-id="13152-121">Obtiene una identidad de usuario específica por la cookie usada para identificarla de forma única.</span><span class="sxs-lookup"><span data-stu-id="13152-121">Gets a specific user identity by the cookie used to uniquely identify it.</span></span><br/>                                                                        |
| [<span data-ttu-id="13152-122">**Forzado**</span><span class="sxs-lookup"><span data-stu-id="13152-122">**Logoff**</span></span>](iuseridentitymanager-logoff.md)                           | <span data-ttu-id="13152-123">En desuso.</span><span class="sxs-lookup"><span data-stu-id="13152-123">Deprecated.</span></span> <span data-ttu-id="13152-124">Cierre la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="13152-124">Log off the current identity.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="13152-125">**Expire**</span><span class="sxs-lookup"><span data-stu-id="13152-125">**Logon**</span></span>](iuseridentitymanager-logon.md)                             | <span data-ttu-id="13152-126">En desuso.</span><span class="sxs-lookup"><span data-stu-id="13152-126">Deprecated.</span></span> <span data-ttu-id="13152-127">Muestra una interfaz de usuario para el usuario, lo que permite al usuario elegir una identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="13152-127">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="13152-128">Si se realiza correctamente, la identidad del usuario se iniciará y se recuperará.</span><span class="sxs-lookup"><span data-stu-id="13152-128">If successful, the user identity will be logged on and retrieved.</span></span><br/>        |
| [<span data-ttu-id="13152-129">**ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="13152-129">**ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)       | <span data-ttu-id="13152-130">En desuso.</span><span class="sxs-lookup"><span data-stu-id="13152-130">Deprecated.</span></span> <span data-ttu-id="13152-131">Muestra una interfaz de usuario para el usuario, lo que permite al usuario administrar las identidades de usuario.</span><span class="sxs-lookup"><span data-stu-id="13152-131">Displays a UI to the user, allowing the user to manage user identities.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="13152-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13152-132">Requirements</span></span>



| <span data-ttu-id="13152-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="13152-133">Requirement</span></span> | <span data-ttu-id="13152-134">Value</span><span class="sxs-lookup"><span data-stu-id="13152-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13152-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13152-135">Minimum supported client</span></span><br/> | <span data-ttu-id="13152-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="13152-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13152-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13152-137">Minimum supported server</span></span><br/> | <span data-ttu-id="13152-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13152-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13152-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="13152-139">End of client support</span></span><br/>    | <span data-ttu-id="13152-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="13152-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="13152-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="13152-141">End of server support</span></span><br/>    | <span data-ttu-id="13152-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="13152-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="13152-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13152-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="13152-144"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="13152-144"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="13152-145">IDL</span><span class="sxs-lookup"><span data-stu-id="13152-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13152-146"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13152-146"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="13152-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13152-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13152-148"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13152-148"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13152-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="13152-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13152-150">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="13152-150">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="13152-151">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="13152-151">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="13152-152">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="13152-152">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="13152-153">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="13152-153">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> </dl>

 

 
