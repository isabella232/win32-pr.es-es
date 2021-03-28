---
description: GetCookie no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: 'IUserIdentity:: GetCookie (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 96cafb13f2c90c41e4aa6dcaaa72cf052757d0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984618"
---
# <a name="iuseridentitygetcookie-method"></a><span data-ttu-id="bf995-104">IUserIdentity:: GetCookie (método)</span><span class="sxs-lookup"><span data-stu-id="bf995-104">IUserIdentity::GetCookie method</span></span>

<span data-ttu-id="bf995-105">\[**GetCookie** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="bf995-105">\[**GetCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bf995-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="bf995-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="bf995-107">Obtiene la cookie usada para identificar de forma única esta identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="bf995-107">Gets the cookie used to uniquely identify this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf995-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf995-108">Syntax</span></span>


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a><span data-ttu-id="bf995-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf995-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf995-110">*puidCookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bf995-110">*puidCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf995-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="bf995-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="bf995-112">Un puntero a un valor _ *GUID*\* que recibe la cookie usada para identificar de forma única esta identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="bf995-112">A pointer to a _ *GUID*\* value that receives the cookie used to uniquely identify this user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf995-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf995-113">Return value</span></span>

<span data-ttu-id="bf995-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bf995-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bf995-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bf995-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf995-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf995-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf995-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf995-117">Requirements</span></span>



| <span data-ttu-id="bf995-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf995-118">Requirement</span></span> | <span data-ttu-id="bf995-119">Value</span><span class="sxs-lookup"><span data-stu-id="bf995-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf995-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf995-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf995-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bf995-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bf995-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf995-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf995-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf995-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bf995-124">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bf995-124">End of client support</span></span><br/>    | <span data-ttu-id="bf995-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bf995-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="bf995-126">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bf995-126">End of server support</span></span><br/>    | <span data-ttu-id="bf995-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf995-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="bf995-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf995-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf995-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf995-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf995-130">IDL</span><span class="sxs-lookup"><span data-stu-id="bf995-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bf995-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf995-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="bf995-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf995-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf995-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf995-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf995-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf995-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf995-135">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="bf995-135">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="bf995-136">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="bf995-136">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




