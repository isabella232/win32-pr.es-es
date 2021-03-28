---
description: No se admite el cierre de sesión y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'IUserIdentityManager:: Logoff (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984155"
---
# <a name="iuseridentitymanagerlogoff-method"></a><span data-ttu-id="4a0be-104">IUserIdentityManager:: Logoff (método)</span><span class="sxs-lookup"><span data-stu-id="4a0be-104">IUserIdentityManager::Logoff method</span></span>

<span data-ttu-id="4a0be-105">\[No se admite el **cierre de sesión** y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="4a0be-105">\[**Logoff** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="4a0be-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="4a0be-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="4a0be-107">En desuso.</span><span class="sxs-lookup"><span data-stu-id="4a0be-107">Deprecated.</span></span> <span data-ttu-id="4a0be-108">Cierre la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="4a0be-108">Log off the current identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a0be-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a0be-109">Syntax</span></span>


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="4a0be-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a0be-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a0be-111">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a0be-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a0be-112">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="4a0be-112">Type: **HWND**</span></span>

<span data-ttu-id="4a0be-113">Un valor **hWnd** que identifica una ventana que se incluirá en primer plano cuando se complete el cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="4a0be-113">An **HWND** value that identifies a window that will be brought into the foreground when the logoff is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a0be-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a0be-114">Return value</span></span>

<span data-ttu-id="4a0be-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a0be-115">Type: **HRESULT**</span></span>

<span data-ttu-id="4a0be-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4a0be-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a0be-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a0be-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a0be-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a0be-118">Requirements</span></span>



| <span data-ttu-id="4a0be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a0be-119">Requirement</span></span> | <span data-ttu-id="4a0be-120">Value</span><span class="sxs-lookup"><span data-stu-id="4a0be-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a0be-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a0be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4a0be-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4a0be-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4a0be-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a0be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4a0be-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a0be-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a0be-125">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4a0be-125">End of client support</span></span><br/>    | <span data-ttu-id="4a0be-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4a0be-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="4a0be-127">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4a0be-127">End of server support</span></span><br/>    | <span data-ttu-id="4a0be-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a0be-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="4a0be-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a0be-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a0be-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a0be-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a0be-131">IDL</span><span class="sxs-lookup"><span data-stu-id="4a0be-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a0be-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a0be-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="4a0be-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a0be-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a0be-134"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a0be-134"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a0be-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a0be-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a0be-136">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="4a0be-136">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="4a0be-137">**IUserIdentityManager:: Logon**</span><span class="sxs-lookup"><span data-stu-id="4a0be-137">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="4a0be-138">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="4a0be-138">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




