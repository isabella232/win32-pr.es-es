---
description: GetCount no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'IEnumUserIdentity:: GetCount (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360676"
---
# <a name="ienumuseridentitygetcount-method"></a><span data-ttu-id="5fafe-104">IEnumUserIdentity:: GetCount (método)</span><span class="sxs-lookup"><span data-stu-id="5fafe-104">IEnumUserIdentity::GetCount method</span></span>

<span data-ttu-id="5fafe-105">\[**GetCount** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="5fafe-105">\[**GetCount** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="5fafe-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="5fafe-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="5fafe-107">Obtiene el número de identidades de usuario actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="5fafe-107">Gets the count of user identities currently on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fafe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5fafe-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a><span data-ttu-id="5fafe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fafe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fafe-110">*pnCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5fafe-110">*pnCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fafe-111">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="5fafe-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="5fafe-112">Puntero a un _ *ULong*\* que recibe el recuento.</span><span class="sxs-lookup"><span data-stu-id="5fafe-112">Pointer to a _ *ULONG*\* that receives the count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fafe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fafe-113">Return value</span></span>

<span data-ttu-id="5fafe-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5fafe-114">Type: **HRESULT**</span></span>

<span data-ttu-id="5fafe-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5fafe-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5fafe-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5fafe-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fafe-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fafe-117">Remarks</span></span>

<span data-ttu-id="5fafe-118">Si se deshabilita la compatibilidad con varias identidades de usuario, *pnCount* recibirá un valor de 1.</span><span class="sxs-lookup"><span data-stu-id="5fafe-118">If support for multiple user identities is disabled, *pnCount* will receive a value of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fafe-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fafe-119">Requirements</span></span>



| <span data-ttu-id="5fafe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fafe-120">Requirement</span></span> | <span data-ttu-id="5fafe-121">Value</span><span class="sxs-lookup"><span data-stu-id="5fafe-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fafe-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fafe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5fafe-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5fafe-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5fafe-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fafe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5fafe-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5fafe-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5fafe-126">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5fafe-126">End of client support</span></span><br/>    | <span data-ttu-id="5fafe-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5fafe-127">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="5fafe-128">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5fafe-128">End of server support</span></span><br/>    | <span data-ttu-id="5fafe-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5fafe-129">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="5fafe-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fafe-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fafe-131"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fafe-131"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="5fafe-132">IDL</span><span class="sxs-lookup"><span data-stu-id="5fafe-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5fafe-133"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5fafe-133"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="5fafe-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5fafe-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fafe-135"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fafe-135"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fafe-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fafe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fafe-137">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="5fafe-137">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="5fafe-138">**IEnumUserIdentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="5fafe-138">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="5fafe-139">**IEnumUserIdentity:: RESET**</span><span class="sxs-lookup"><span data-stu-id="5fafe-139">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="5fafe-140">**IEnumUserIdentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="5fafe-140">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




