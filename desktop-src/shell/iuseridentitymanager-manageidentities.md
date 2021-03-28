---
description: 'IUserIdentityManager:: ManageIdentities no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'IUserIdentityManager:: ManageIdentities (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360086"
---
# <a name="iuseridentitymanagermanageidentities-method"></a><span data-ttu-id="3e2c7-104">IUserIdentityManager:: ManageIdentities (método)</span><span class="sxs-lookup"><span data-stu-id="3e2c7-104">IUserIdentityManager::ManageIdentities method</span></span>

<span data-ttu-id="3e2c7-105">\[**IUserIdentityManager:: ManageIdentities** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-105">\[**IUserIdentityManager::ManageIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="3e2c7-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="3e2c7-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="3e2c7-107">Muestra una interfaz de usuario para el usuario, lo que permite al usuario administrar las identidades de usuario.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-107">Displays a UI to the user, allowing the user to manage user identities.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2c7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e2c7-108">Syntax</span></span>


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3e2c7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e2c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e2c7-110">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e2c7-110">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2c7-111">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="3e2c7-111">Type: **HWND**</span></span>

<span data-ttu-id="3e2c7-112">Un valor **hWnd** que identifica una ventana que se va a devolver al primer plano después de que se descarte la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-112">An **HWND** value that identifies a window that will be brought to the foreground after the UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="3e2c7-113">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e2c7-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2c7-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e2c7-114">Type: **DWORD**</span></span>

<span data-ttu-id="3e2c7-115">Marcas opcionales para definir cómo se comportará la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-115">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="3e2c7-116">Establezca en UIMI \_ crear \_ nueva \_ identidad para solicitar al usuario que cree una nueva identidad.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-116">Set to UIMI\_CREATE\_NEW\_IDENTITY to prompt the user to create a new identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e2c7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e2c7-117">Return value</span></span>

<span data-ttu-id="3e2c7-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3e2c7-118">Type: **HRESULT**</span></span>

<span data-ttu-id="3e2c7-119">Resultado de la operación de administración.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-119">The result of the management operation.</span></span> <span data-ttu-id="3e2c7-120">Si se realiza correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-120">If successful, it returns S\_OK.</span></span> <span data-ttu-id="3e2c7-121">De lo contrario, devolverá uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="3e2c7-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3e2c7-122">Return code</span></span>                                                                                            | <span data-ttu-id="3e2c7-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e2c7-123">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="3e2c7-124"><dt>**E \_ identidades \_ deshabilitadas**</dt></span><span class="sxs-lookup"><span data-stu-id="3e2c7-124"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="3e2c7-125">La administración de identidades está deshabilitada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-125">Identity management is disabled on the system.</span></span><br/> |
| <dl> <span data-ttu-id="3e2c7-126"><dt>**E \_ cancelado por el usuario \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e2c7-126"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="3e2c7-127">El usuario canceló el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3e2c7-127">The user canceled the dialog.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="3e2c7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e2c7-128">Requirements</span></span>



| <span data-ttu-id="3e2c7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e2c7-129">Requirement</span></span> | <span data-ttu-id="3e2c7-130">Value</span><span class="sxs-lookup"><span data-stu-id="3e2c7-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2c7-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e2c7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3e2c7-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3e2c7-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3e2c7-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e2c7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3e2c7-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e2c7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3e2c7-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3e2c7-135">End of client support</span></span><br/>    | <span data-ttu-id="3e2c7-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3e2c7-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="3e2c7-137">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3e2c7-137">End of server support</span></span><br/>    | <span data-ttu-id="3e2c7-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e2c7-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="3e2c7-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e2c7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e2c7-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e2c7-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e2c7-141">IDL</span><span class="sxs-lookup"><span data-stu-id="3e2c7-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e2c7-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e2c7-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="3e2c7-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e2c7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e2c7-144"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e2c7-144"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e2c7-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e2c7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2c7-146">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="3e2c7-146">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="3e2c7-147">**IUserIdentityManager:: Logon**</span><span class="sxs-lookup"><span data-stu-id="3e2c7-147">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="3e2c7-148">**IUserIdentityManager:: Logoff**</span><span class="sxs-lookup"><span data-stu-id="3e2c7-148">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




