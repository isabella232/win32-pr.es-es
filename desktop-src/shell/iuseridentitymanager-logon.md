---
description: 'IUserIdentityManager:: Logon no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'IUserIdentityManager:: Logon (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153602"
---
# <a name="iuseridentitymanagerlogon-method"></a><span data-ttu-id="7c17e-104">IUserIdentityManager:: Logon (método)</span><span class="sxs-lookup"><span data-stu-id="7c17e-104">IUserIdentityManager::Logon method</span></span>

<span data-ttu-id="7c17e-105">\[**IUserIdentityManager:: Logon** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="7c17e-105">\[**IUserIdentityManager::Logon** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7c17e-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="7c17e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="7c17e-107">Muestra una interfaz de usuario para el usuario, lo que permite al usuario elegir una identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="7c17e-107">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="7c17e-108">Si se realiza correctamente, la identidad del usuario se iniciará y se recuperará.</span><span class="sxs-lookup"><span data-stu-id="7c17e-108">If successful, the user identity will be logged on and retrieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c17e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c17e-109">Syntax</span></span>


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="7c17e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c17e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c17e-111">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c17e-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c17e-112">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="7c17e-112">Type: **HWND**</span></span>

<span data-ttu-id="7c17e-113">Un valor **hWnd** que identifica una ventana que se enviará al primer plano después de que se descarte la interfaz de usuario de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7c17e-113">An **HWND** value that identifies a window that will be brought to the foreground after the logon UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="7c17e-114">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c17e-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c17e-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7c17e-115">Type: **DWORD**</span></span>

<span data-ttu-id="7c17e-116">Marcas opcionales para definir cómo se comportará la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7c17e-116">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="7c17e-117">Establezca en UIL \_ Force \_ UI para forzar que se muestre la interfaz de usuario, incluso si ya se ha elegido una identidad.</span><span class="sxs-lookup"><span data-stu-id="7c17e-117">Set to UIL\_FORCE\_UI to force the UI to display, even if an identity has already been chosen.</span></span>

</dd> <dt>

<span data-ttu-id="7c17e-118">*ppIdentity* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7c17e-118">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c17e-119">Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7c17e-119">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="7c17e-120">Dirección del puntero que recibe la identidad del usuario elegida.</span><span class="sxs-lookup"><span data-stu-id="7c17e-120">The address of the pointer that receives the chosen user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c17e-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c17e-121">Return value</span></span>

<span data-ttu-id="7c17e-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7c17e-122">Type: **HRESULT**</span></span>

<span data-ttu-id="7c17e-123">Resultado de la operación de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7c17e-123">Result of the logon operation.</span></span> <span data-ttu-id="7c17e-124">Si se realiza correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="7c17e-124">If successful, it returns S\_OK.</span></span> <span data-ttu-id="7c17e-125">De lo contrario, devolverá uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="7c17e-125">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="7c17e-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7c17e-126">Return code</span></span>                                                                                            | <span data-ttu-id="7c17e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c17e-127">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c17e-128"><dt>**E \_ cancelado por el usuario \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-128"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="7c17e-129">El usuario canceló la operación de inicio de sesión desde la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7c17e-129">The user canceled the logon operation from the UI.</span></span><br/>                               |
| <dl> <span data-ttu-id="7c17e-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="7c17e-131">No se pudo crear la identidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c17e-131">The user identity could not be created.</span></span><br/>                                          |
| <dl> <span data-ttu-id="7c17e-132"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="7c17e-133">Error inesperado en la operación.</span><span class="sxs-lookup"><span data-stu-id="7c17e-133">The operation failed unexpectedly.</span></span><br/>                                               |
| <dl> <span data-ttu-id="7c17e-134"><dt>**E \_ identidades \_ deshabilitadas**</dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-134"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="7c17e-135">La administración de identidades está deshabilitada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="7c17e-135">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7c17e-136"><dt>**\_identidades \_ deshabilitadas**</dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-136"><dt>**S\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="7c17e-137">La administración de identidades está deshabilitada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="7c17e-137">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7c17e-138"><dt>**E \_ identidad \_ cambiando**</dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-138"><dt>**E\_IDENTITY\_CHANGING**</dt></span></span> </dl>   | <span data-ttu-id="7c17e-139">El sistema está cambiando actualmente las identidades y no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="7c17e-139">The system is currently switching identities, and cannot complete the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c17e-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c17e-140">Requirements</span></span>



| <span data-ttu-id="7c17e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c17e-141">Requirement</span></span> | <span data-ttu-id="7c17e-142">Value</span><span class="sxs-lookup"><span data-stu-id="7c17e-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c17e-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c17e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7c17e-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7c17e-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7c17e-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c17e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7c17e-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c17e-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7c17e-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7c17e-147">End of client support</span></span><br/>    | <span data-ttu-id="7c17e-148">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7c17e-148">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="7c17e-149">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7c17e-149">End of server support</span></span><br/>    | <span data-ttu-id="7c17e-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c17e-150">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="7c17e-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c17e-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c17e-152"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-152"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c17e-153">IDL</span><span class="sxs-lookup"><span data-stu-id="7c17e-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c17e-154"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-154"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="7c17e-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c17e-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c17e-156"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c17e-156"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c17e-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c17e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c17e-158">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="7c17e-158">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="7c17e-159">**IUserIdentityManager:: Logoff**</span><span class="sxs-lookup"><span data-stu-id="7c17e-159">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> <dt>

[<span data-ttu-id="7c17e-160">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="7c17e-160">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




