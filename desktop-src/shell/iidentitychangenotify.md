---
description: Desusado. Proporciona una notificación de las modificaciones realizadas en las identidades de usuario en el sistema, así como las solicitudes de usuario para cambiar la identidad del usuario actual.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interfaz IIdentityChangeNotify (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276737"
---
# <a name="iidentitychangenotify-interface"></a><span data-ttu-id="21ac7-104">Interfaz IIdentityChangeNotify</span><span class="sxs-lookup"><span data-stu-id="21ac7-104">IIdentityChangeNotify interface</span></span>

<span data-ttu-id="21ac7-105">\[La interfaz **IIdentityChangeNotify** está disponible para su uso en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="21ac7-105">\[The **IIdentityChangeNotify** interface is available for use in Windows 2000.</span></span> <span data-ttu-id="21ac7-106">En Windows XP, esta funcionalidad se ha sustituido por [las cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md), y puede modificarse o no estar disponible en las versiones posteriores.\]</span><span class="sxs-lookup"><span data-stu-id="21ac7-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="21ac7-107">En desuso.</span><span class="sxs-lookup"><span data-stu-id="21ac7-107">Deprecated.</span></span> <span data-ttu-id="21ac7-108">Proporciona una notificación de las modificaciones realizadas en las identidades de usuario en el sistema, así como las solicitudes de usuario para cambiar la identidad del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="21ac7-108">Provides notification of modifications to user identities on the system, as well as user requests to switch the current user identity.</span></span>

## <a name="members"></a><span data-ttu-id="21ac7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="21ac7-109">Members</span></span>

<span data-ttu-id="21ac7-110">La interfaz **IIdentityChangeNotify** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="21ac7-110">The **IIdentityChangeNotify** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="21ac7-111">**IIdentityChangeNotify** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="21ac7-111">**IIdentityChangeNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="21ac7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="21ac7-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="21ac7-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="21ac7-113">Methods</span></span>

<span data-ttu-id="21ac7-114">La interfaz **IIdentityChangeNotify** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="21ac7-114">The **IIdentityChangeNotify** interface has these methods.</span></span>



| <span data-ttu-id="21ac7-115">Método</span><span class="sxs-lookup"><span data-stu-id="21ac7-115">Method</span></span>                                                                                 | <span data-ttu-id="21ac7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="21ac7-116">Description</span></span>                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21ac7-117">**IdentityInformationChanged**</span><span class="sxs-lookup"><span data-stu-id="21ac7-117">**IdentityInformationChanged**</span></span>](iidentitychangenotify-identityinformationchanged.md) | <span data-ttu-id="21ac7-118">En desuso.</span><span class="sxs-lookup"><span data-stu-id="21ac7-118">Deprecated.</span></span> <span data-ttu-id="21ac7-119">Se llama cuando ha cambiado la información sobre una identidad de usuario o cuando se ha agregado o eliminado una identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="21ac7-119">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span><br/>  |
| [<span data-ttu-id="21ac7-120">**QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="21ac7-120">**QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)           | <span data-ttu-id="21ac7-121">En desuso.</span><span class="sxs-lookup"><span data-stu-id="21ac7-121">Deprecated.</span></span> <span data-ttu-id="21ac7-122">Se llama cuando el usuario actual ha solicitado que se cambie su identidad de usuario, pero antes de que se produzca el cambio.</span><span class="sxs-lookup"><span data-stu-id="21ac7-122">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span><br/> |
| [<span data-ttu-id="21ac7-123">**SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="21ac7-123">**SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)                     | <span data-ttu-id="21ac7-124">En desuso.</span><span class="sxs-lookup"><span data-stu-id="21ac7-124">Deprecated.</span></span> <span data-ttu-id="21ac7-125">Se llama cuando se cambian las identidades de usuario.</span><span class="sxs-lookup"><span data-stu-id="21ac7-125">Called when user identities are switched.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="21ac7-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21ac7-126">Remarks</span></span>

<span data-ttu-id="21ac7-127">Para implementar notificaciones, una interfaz derivada debe conectarse al [**IUserIdentityManager**](iuseridentitymanager.md) llamando a [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) y pasando un puntero a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="21ac7-127">To implement notifications, a derived interface must connect to the [**IUserIdentityManager**](iuseridentitymanager.md) by calling [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) and by passing a pointer to the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ac7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21ac7-128">Requirements</span></span>



| <span data-ttu-id="21ac7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="21ac7-129">Requirement</span></span> | <span data-ttu-id="21ac7-130">Value</span><span class="sxs-lookup"><span data-stu-id="21ac7-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21ac7-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21ac7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="21ac7-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="21ac7-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="21ac7-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21ac7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="21ac7-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21ac7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="21ac7-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21ac7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="21ac7-136"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="21ac7-136"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="21ac7-137">IDL</span><span class="sxs-lookup"><span data-stu-id="21ac7-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21ac7-138"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21ac7-138"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="21ac7-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21ac7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21ac7-140"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21ac7-140"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="21ac7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="21ac7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ac7-142">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="21ac7-142">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="21ac7-143">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="21ac7-143">**IConnectionPoint**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
