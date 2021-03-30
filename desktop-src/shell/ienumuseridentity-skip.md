---
description: 'IEnumUserIdentity:: Skip no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'IEnumUserIdentity:: Skip (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997668"
---
# <a name="ienumuseridentityskip-method"></a><span data-ttu-id="bc05c-104">IEnumUserIdentity:: Skip (método)</span><span class="sxs-lookup"><span data-stu-id="bc05c-104">IEnumUserIdentity::Skip method</span></span>

<span data-ttu-id="bc05c-105">\[**IEnumUserIdentity:: Skip** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="bc05c-105">\[**IEnumUserIdentity::Skip** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bc05c-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="bc05c-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="bc05c-107">Omite un número determinado de interfaces de identidad de usuario en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="bc05c-107">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="bc05c-108">Se utiliza al recuperar interfaces.</span><span class="sxs-lookup"><span data-stu-id="bc05c-108">Used when retrieving interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc05c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc05c-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="bc05c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc05c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc05c-111">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc05c-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc05c-112">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="bc05c-112">Type: **ULONG**</span></span>

<span data-ttu-id="bc05c-113">Número de interfaces que se van a omitir.</span><span class="sxs-lookup"><span data-stu-id="bc05c-113">The number of interfaces to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc05c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc05c-114">Return value</span></span>

<span data-ttu-id="bc05c-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc05c-115">Type: **HRESULT**</span></span>

<span data-ttu-id="bc05c-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bc05c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc05c-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc05c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc05c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc05c-118">Remarks</span></span>

<span data-ttu-id="bc05c-119">[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un recuento interno que especifica la interfaz que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="bc05c-119">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="bc05c-120">Para incrementar este recuento sin recuperar interfaces, llame a este método.</span><span class="sxs-lookup"><span data-stu-id="bc05c-120">To increment this count without retrieving interfaces, call this method.</span></span> <span data-ttu-id="bc05c-121">Para restablecer el recuento, llame a [**IEnumUserIdentity:: RESET**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="bc05c-121">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc05c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc05c-122">Requirements</span></span>



| <span data-ttu-id="bc05c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc05c-123">Requirement</span></span> | <span data-ttu-id="bc05c-124">Value</span><span class="sxs-lookup"><span data-stu-id="bc05c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc05c-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc05c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bc05c-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bc05c-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bc05c-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc05c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bc05c-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc05c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bc05c-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bc05c-129">End of client support</span></span><br/>    | <span data-ttu-id="bc05c-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc05c-130">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="bc05c-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bc05c-131">End of server support</span></span><br/>    | <span data-ttu-id="bc05c-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc05c-132">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="bc05c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc05c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc05c-134"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc05c-134"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc05c-135">IDL</span><span class="sxs-lookup"><span data-stu-id="bc05c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc05c-136"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc05c-136"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="bc05c-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc05c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc05c-138"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc05c-138"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc05c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc05c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc05c-140">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="bc05c-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="bc05c-141">**IEnumUserIdentity:: RESET**</span><span class="sxs-lookup"><span data-stu-id="bc05c-141">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="bc05c-142">**IEnumUserIdentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="bc05c-142">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> <dt>

[<span data-ttu-id="bc05c-143">**IEnumUserIdentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="bc05c-143">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




