---
description: GetOrdinal no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'IUserIdentity2:: GetOrdinal (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985683"
---
# <a name="iuseridentity2getordinal-method"></a><span data-ttu-id="00d04-104">IUserIdentity2:: GetOrdinal (método)</span><span class="sxs-lookup"><span data-stu-id="00d04-104">IUserIdentity2::GetOrdinal method</span></span>

<span data-ttu-id="00d04-105">\[**GetOrdinal** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="00d04-105">\[**GetOrdinal** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="00d04-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="00d04-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="00d04-107">Obtiene el número ordinal de esta identidad.</span><span class="sxs-lookup"><span data-stu-id="00d04-107">Gets the ordinal number for this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d04-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00d04-108">Syntax</span></span>


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a><span data-ttu-id="00d04-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00d04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d04-110">*dwOrdinal* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="00d04-110">*dwOrdinal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00d04-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="00d04-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="00d04-112">Un puntero a un valor _ *DWORD*\* que recibe el número ordinal de esta identidad.</span><span class="sxs-lookup"><span data-stu-id="00d04-112">A pointer to a _ *DWORD*\* value that receives the ordinal number for this identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d04-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00d04-113">Return value</span></span>

<span data-ttu-id="00d04-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00d04-114">Type: **HRESULT**</span></span>

<span data-ttu-id="00d04-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="00d04-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00d04-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="00d04-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00d04-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00d04-117">Remarks</span></span>

<span data-ttu-id="00d04-118">El ordinal determina el orden de las identidades en la lista de identidades, pero puede que no se conserven en las distintas operaciones de las identidades.</span><span class="sxs-lookup"><span data-stu-id="00d04-118">The ordinal determines the order of the identities in the identity list, but may not persist throughout operations on the identities.</span></span> <span data-ttu-id="00d04-119">Para obtener un valor único para una identidad, llame a [**GetCookie**](iuseridentity-getcookie.md).</span><span class="sxs-lookup"><span data-stu-id="00d04-119">To get a unique value for an identity, call [**GetCookie**](iuseridentity-getcookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00d04-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00d04-120">Requirements</span></span>



| <span data-ttu-id="00d04-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d04-121">Requirement</span></span> | <span data-ttu-id="00d04-122">Value</span><span class="sxs-lookup"><span data-stu-id="00d04-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00d04-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00d04-123">Minimum supported client</span></span><br/> | <span data-ttu-id="00d04-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="00d04-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="00d04-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00d04-125">Minimum supported server</span></span><br/> | <span data-ttu-id="00d04-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00d04-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="00d04-127">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="00d04-127">End of client support</span></span><br/>    | <span data-ttu-id="00d04-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="00d04-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="00d04-129">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="00d04-129">End of server support</span></span><br/>    | <span data-ttu-id="00d04-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00d04-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="00d04-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00d04-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d04-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="00d04-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="00d04-133">IDL</span><span class="sxs-lookup"><span data-stu-id="00d04-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="00d04-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="00d04-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="00d04-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00d04-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00d04-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d04-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d04-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="00d04-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d04-138">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="00d04-138">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="00d04-139">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="00d04-139">**GetCookie**</span></span>](iuseridentity-getcookie.md)
</dt> </dl>

 

 




