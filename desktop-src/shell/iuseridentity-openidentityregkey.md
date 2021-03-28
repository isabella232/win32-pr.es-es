---
description: Desusado. Recupera la clave del registro que corresponde a esta identidad de usuario.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'IUserIdentity:: OpenIdentityRegKey (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984607"
---
# <a name="iuseridentityopenidentityregkey-method"></a><span data-ttu-id="659da-104">IUserIdentity:: OpenIdentityRegKey (método)</span><span class="sxs-lookup"><span data-stu-id="659da-104">IUserIdentity::OpenIdentityRegKey method</span></span>

<span data-ttu-id="659da-105">\[El método **IUserIdentity:: OpenIdentityRegKey** está disponible para su uso en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="659da-105">\[The **IUserIdentity::OpenIdentityRegKey** method is available for use in Windows 2000.</span></span> <span data-ttu-id="659da-106">En Windows XP, esta funcionalidad se ha sustituido por [las cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md), y puede modificarse o no estar disponible en las versiones posteriores.\]</span><span class="sxs-lookup"><span data-stu-id="659da-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="659da-107">En desuso.</span><span class="sxs-lookup"><span data-stu-id="659da-107">Deprecated.</span></span> <span data-ttu-id="659da-108">Recupera la clave del registro que corresponde a esta identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="659da-108">Retrieves the key in the registry that corresponds to this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="659da-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="659da-109">Syntax</span></span>


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a><span data-ttu-id="659da-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="659da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="659da-111">*dwDesiredAccess* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="659da-111">*dwDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="659da-112">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="659da-112">Type: **DWORD**</span></span>

<span data-ttu-id="659da-113">Valor que describe el nivel de acceso solicitado de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="659da-113">A value that describes the access level requested of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="659da-114">*phKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="659da-114">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="659da-115">Tipo: \**HKEY \** _</span><span class="sxs-lookup"><span data-stu-id="659da-115">Type: \**HKEY\** _</span></span>

<span data-ttu-id="659da-116">Puntero que recibe la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="659da-116">A pointer that receives the registry key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="659da-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="659da-117">Return value</span></span>

<span data-ttu-id="659da-118">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="659da-118">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="659da-119">Resultado de la solicitud del registro.</span><span class="sxs-lookup"><span data-stu-id="659da-119">The result of the registry request.</span></span> <span data-ttu-id="659da-120">Si se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="659da-120">If successful, it returns **S\_OK**.</span></span> <span data-ttu-id="659da-121">De lo contrario, devolverá uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="659da-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="659da-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="659da-122">Return code</span></span>                                                                                            | <span data-ttu-id="659da-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="659da-123">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="659da-124"><dt>**identidad de E \_ \_ no \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="659da-124"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="659da-125">Esta identidad no tiene una clave del registro asociada.</span><span class="sxs-lookup"><span data-stu-id="659da-125">This identity does not have an associated registry key.</span></span><br/> |
| <dl> <span data-ttu-id="659da-126"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="659da-126"><dt>**E\_FAIL**</dt></span></span> </dl>                 | <span data-ttu-id="659da-127">No se pudo obtener acceso a la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="659da-127">The registry key was unable to be accessed.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="659da-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="659da-128">Remarks</span></span>

<span data-ttu-id="659da-129">El parámetro *dwDesiredAccess* es un descriptor de seguridad de acceso al registro estándar que describe el acceso que se desea obtener a la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="659da-129">The *dwDesiredAccess* parameter is a standard registry access security descriptor that describes the access you want to gain to the registry key.</span></span> <span data-ttu-id="659da-130">Para obtener más información sobre la seguridad del registro, incluida una lista de valores aceptables para este parámetro, consulte [derechos de acceso y seguridad de la clave del registro](../sysinfo/registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="659da-130">For more information on registry security, including a list of acceptable values for this parameter, see [Registry Key Security and Access Rights](../sysinfo/registry-key-security-and-access-rights.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="659da-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="659da-131">Requirements</span></span>



| <span data-ttu-id="659da-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="659da-132">Requirement</span></span> | <span data-ttu-id="659da-133">Value</span><span class="sxs-lookup"><span data-stu-id="659da-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="659da-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="659da-134">Minimum supported client</span></span><br/> | <span data-ttu-id="659da-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="659da-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="659da-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="659da-136">Minimum supported server</span></span><br/> | <span data-ttu-id="659da-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="659da-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="659da-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="659da-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="659da-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="659da-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="659da-140">IDL</span><span class="sxs-lookup"><span data-stu-id="659da-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="659da-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="659da-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="659da-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="659da-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="659da-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="659da-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="659da-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="659da-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="659da-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="659da-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="659da-146">**IUserIdentity::GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="659da-146">**IUserIdentity::GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
