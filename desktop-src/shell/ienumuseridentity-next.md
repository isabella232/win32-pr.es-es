---
description: 'IEnumUserIdentity:: Next no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'IEnumUserIdentity:: Next (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997672"
---
# <a name="ienumuseridentitynext-method"></a><span data-ttu-id="d0d50-104">IEnumUserIdentity:: Next (método)</span><span class="sxs-lookup"><span data-stu-id="d0d50-104">IEnumUserIdentity::Next method</span></span>

<span data-ttu-id="d0d50-105">\[**IEnumUserIdentity:: Next** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="d0d50-105">\[**IEnumUserIdentity::Next** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d0d50-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="d0d50-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="d0d50-107">En desuso.</span><span class="sxs-lookup"><span data-stu-id="d0d50-107">Deprecated.</span></span> <span data-ttu-id="d0d50-108">Recupera una matriz de interfaces de identidad de usuario de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="d0d50-108">Retrieves an array of user identity interfaces from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d50-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0d50-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="d0d50-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0d50-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0d50-111">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0d50-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d50-112">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="d0d50-112">Type: **ULONG**</span></span>

<span data-ttu-id="d0d50-113">Valor **ULong** que representa el número de interfaces que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d0d50-113">A **ULONG** value that represents the number of interfaces to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d0d50-114">*rgelt* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d0d50-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d50-115">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="d0d50-115">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="d0d50-116">Dirección de un puntero que recibe las interfaces.</span><span class="sxs-lookup"><span data-stu-id="d0d50-116">The address of a pointer that receives the interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="d0d50-117">*pceltFetched* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d0d50-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d50-118">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="d0d50-118">Type: \**ULONG\** _</span></span>

<span data-ttu-id="d0d50-119">Dirección de un puntero que recibe el número de interfaces recuperadas correctamente.</span><span class="sxs-lookup"><span data-stu-id="d0d50-119">The address of a pointer that receives the number of interfaces successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0d50-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0d50-120">Return value</span></span>

<span data-ttu-id="d0d50-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d0d50-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d0d50-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d0d50-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d0d50-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0d50-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0d50-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0d50-124">Remarks</span></span>

<span data-ttu-id="d0d50-125">[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un recuento interno que especifica la interfaz que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d0d50-125">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="d0d50-126">Si hay varias llamadas a este método, no se restablecerá este recuento.</span><span class="sxs-lookup"><span data-stu-id="d0d50-126">Multiple calls to this method will not reset this count.</span></span> <span data-ttu-id="d0d50-127">Para restablecer el recuento, llame a [**IEnumUserIdentity:: RESET**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="d0d50-127">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span> <span data-ttu-id="d0d50-128">Para incrementar el recuento sin recuperar interfaces, llame a [**IEnumUserIdentity:: Skip**](ienumuseridentity-skip.md).</span><span class="sxs-lookup"><span data-stu-id="d0d50-128">To increment the count without retrieving interfaces, call [**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md).</span></span>

<span data-ttu-id="d0d50-129">El valor de *Celt* no debe superar el valor devuelto por [**IEnumUserIdentity:: GetCount**](ienumuseridentity-getcount.md).</span><span class="sxs-lookup"><span data-stu-id="d0d50-129">The value of *celt* should not exceed the value returned by [**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0d50-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0d50-130">Requirements</span></span>



| <span data-ttu-id="d0d50-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0d50-131">Requirement</span></span> | <span data-ttu-id="d0d50-132">Value</span><span class="sxs-lookup"><span data-stu-id="d0d50-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0d50-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0d50-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d0d50-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d0d50-134">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d0d50-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0d50-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d0d50-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0d50-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d0d50-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d0d50-137">End of client support</span></span><br/>    | <span data-ttu-id="d0d50-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0d50-138">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="d0d50-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d0d50-139">End of server support</span></span><br/>    | <span data-ttu-id="d0d50-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0d50-140">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="d0d50-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0d50-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0d50-142"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0d50-142"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0d50-143">IDL</span><span class="sxs-lookup"><span data-stu-id="d0d50-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d0d50-144"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d0d50-144"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="d0d50-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0d50-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0d50-146"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0d50-146"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0d50-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0d50-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0d50-148">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="d0d50-148">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="d0d50-149">**IEnumUserIdentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="d0d50-149">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="d0d50-150">**IEnumUserIdentity:: RESET**</span><span class="sxs-lookup"><span data-stu-id="d0d50-150">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="d0d50-151">**IEnumUserIdentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="d0d50-151">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
