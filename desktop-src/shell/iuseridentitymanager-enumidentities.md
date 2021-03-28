---
description: 'IUserIdentityManager:: EnumIdentities no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'IUserIdentityManager:: EnumIdentities (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153604"
---
# <a name="iuseridentitymanagerenumidentities-method"></a><span data-ttu-id="d3785-104">IUserIdentityManager:: EnumIdentities (método)</span><span class="sxs-lookup"><span data-stu-id="d3785-104">IUserIdentityManager::EnumIdentities method</span></span>

<span data-ttu-id="d3785-105">\[**IUserIdentityManager:: EnumIdentities** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="d3785-105">\[**IUserIdentityManager::EnumIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d3785-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="d3785-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="d3785-107">Obtiene un objeto [**IEnumUserIdentity**](ienumuseridentity.md) , que se puede utilizar para enumerar las identidades de usuario presentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d3785-107">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3785-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3785-108">Syntax</span></span>


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a><span data-ttu-id="d3785-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3785-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3785-110">*ppEnumUser* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d3785-110">*ppEnumUser* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3785-111">Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d3785-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="d3785-112">Dirección del puntero al nuevo objeto de enumeración de identidades.</span><span class="sxs-lookup"><span data-stu-id="d3785-112">The address of the pointer to the new identity enumeration object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3785-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3785-113">Return value</span></span>

<span data-ttu-id="d3785-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d3785-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d3785-115">Resultado de la operación de recuperación.</span><span class="sxs-lookup"><span data-stu-id="d3785-115">The result of the retrieval operation.</span></span> <span data-ttu-id="d3785-116">Si se realiza correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="d3785-116">If successful, it returns S\_OK.</span></span> <span data-ttu-id="d3785-117">Si no se pudo crear el objeto de enumeración, devuelve E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d3785-117">If the enumeration object could not be created, it returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3785-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3785-118">Remarks</span></span>

<span data-ttu-id="d3785-119">Este método es útil para la iteración en la lista de identidades del sistema.</span><span class="sxs-lookup"><span data-stu-id="d3785-119">This method is useful for iteration over the list of identities on the system.</span></span> <span data-ttu-id="d3785-120">Para recuperar una única identidad por su cookie sin tener acceso a la lista, llame a [**IUserIdentityManager:: GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span><span class="sxs-lookup"><span data-stu-id="d3785-120">To retrieve a single identity by its cookie without accessing the list, call [**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3785-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3785-121">Requirements</span></span>



| <span data-ttu-id="d3785-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3785-122">Requirement</span></span> | <span data-ttu-id="d3785-123">Value</span><span class="sxs-lookup"><span data-stu-id="d3785-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3785-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3785-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d3785-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d3785-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d3785-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3785-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d3785-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3785-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d3785-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d3785-128">End of client support</span></span><br/>    | <span data-ttu-id="d3785-129">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d3785-129">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="d3785-130">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d3785-130">End of server support</span></span><br/>    | <span data-ttu-id="d3785-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3785-131">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="d3785-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3785-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3785-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3785-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3785-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d3785-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3785-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3785-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="d3785-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d3785-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3785-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3785-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3785-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3785-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3785-139">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="d3785-139">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="d3785-140">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="d3785-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="d3785-141">**IUserIdentityManager::GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="d3785-141">**IUserIdentityManager::GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




