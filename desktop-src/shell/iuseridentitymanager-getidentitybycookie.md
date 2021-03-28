---
description: GetIdentityByCookie no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'IUserIdentityManager:: GetIdentityByCookie (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539483"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a><span data-ttu-id="22ba0-104">IUserIdentityManager:: GetIdentityByCookie (método)</span><span class="sxs-lookup"><span data-stu-id="22ba0-104">IUserIdentityManager::GetIdentityByCookie method</span></span>

<span data-ttu-id="22ba0-105">\[**GetIdentityByCookie** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="22ba0-105">\[**GetIdentityByCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="22ba0-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="22ba0-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="22ba0-107">Obtiene una identidad de usuario específica por la cookie usada para identificarla de forma única.</span><span class="sxs-lookup"><span data-stu-id="22ba0-107">Gets a specific user identity by the cookie used to uniquely identify it.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ba0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22ba0-108">Syntax</span></span>


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="22ba0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22ba0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ba0-110">*uidCookie* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22ba0-110">*uidCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22ba0-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="22ba0-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="22ba0-112">Dirección de un valor _ *GUID*\* que representa la cookie de la identidad que se desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="22ba0-112">The address of a _ *GUID*\* value that represents the cookie for the identity you want to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="22ba0-113">*ppIdentity* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="22ba0-113">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22ba0-114">Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="22ba0-114">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="22ba0-115">Dirección del puntero que recibirá el objeto de identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="22ba0-115">The address of the pointer that will receive the user identity object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22ba0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22ba0-116">Return value</span></span>

<span data-ttu-id="22ba0-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="22ba0-117">Type: **HRESULT**</span></span>

<span data-ttu-id="22ba0-118">Resultado de la solicitud de recuperación.</span><span class="sxs-lookup"><span data-stu-id="22ba0-118">The result of the retrieval request.</span></span> <span data-ttu-id="22ba0-119">Si se realiza correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="22ba0-119">If successful, it returns S\_OK.</span></span> <span data-ttu-id="22ba0-120">De lo contrario, devolverá uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="22ba0-120">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="22ba0-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="22ba0-121">Return code</span></span>                                                                                            | <span data-ttu-id="22ba0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="22ba0-122">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="22ba0-123"><dt>**identidad de E \_ \_ no \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="22ba0-123"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="22ba0-124">No se encontró la identidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="22ba0-124">The identity requested could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="22ba0-125"><dt>**E \_ identidades \_ deshabilitadas**</dt></span><span class="sxs-lookup"><span data-stu-id="22ba0-125"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="22ba0-126">La administración de identidades está deshabilitada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="22ba0-126">Identity management is disabled on the system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="22ba0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22ba0-127">Requirements</span></span>



| <span data-ttu-id="22ba0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="22ba0-128">Requirement</span></span> | <span data-ttu-id="22ba0-129">Value</span><span class="sxs-lookup"><span data-stu-id="22ba0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22ba0-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22ba0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="22ba0-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="22ba0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="22ba0-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22ba0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="22ba0-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22ba0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="22ba0-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="22ba0-134">End of client support</span></span><br/>    | <span data-ttu-id="22ba0-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="22ba0-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="22ba0-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="22ba0-136">End of server support</span></span><br/>    | <span data-ttu-id="22ba0-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22ba0-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="22ba0-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22ba0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="22ba0-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="22ba0-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="22ba0-140">IDL</span><span class="sxs-lookup"><span data-stu-id="22ba0-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="22ba0-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="22ba0-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="22ba0-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22ba0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22ba0-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22ba0-143"><dt>Msident.dll</dt></span></span> </dl> |



 

 




