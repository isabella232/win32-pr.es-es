---
description: 'IEnumUserIdentity:: Clone no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'IEnumUserIdentity:: Clone (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997673"
---
# <a name="ienumuseridentityclone-method"></a><span data-ttu-id="7173d-104">IEnumUserIdentity:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="7173d-104">IEnumUserIdentity::Clone method</span></span>

<span data-ttu-id="7173d-105">\[**IEnumUserIdentity:: Clone** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="7173d-105">\[**IEnumUserIdentity::Clone** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7173d-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="7173d-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="7173d-107">Obtiene una copia de la enumeración actual.</span><span class="sxs-lookup"><span data-stu-id="7173d-107">Gets a copy of the current enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="7173d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7173d-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="7173d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7173d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7173d-110">*ppenum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7173d-110">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7173d-111">Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7173d-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="7173d-112">Dirección de un puntero que recibe una copia de esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="7173d-112">The address of a pointer that receives a copy of this enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7173d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7173d-113">Return value</span></span>

<span data-ttu-id="7173d-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7173d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7173d-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7173d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7173d-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7173d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7173d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7173d-117">Remarks</span></span>

<span data-ttu-id="7173d-118">[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un recuento interno que especifica la interfaz que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="7173d-118">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="7173d-119">El valor de este recuento se aplicará a la interfaz recibida por *ppenum*.</span><span class="sxs-lookup"><span data-stu-id="7173d-119">The value of this count will be applied to the interface received by *ppenum*.</span></span> <span data-ttu-id="7173d-120">Para restablecer el recuento, llame a [**IEnumUserIdentity:: RESET**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="7173d-120">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7173d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7173d-121">Requirements</span></span>



| <span data-ttu-id="7173d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7173d-122">Requirement</span></span> | <span data-ttu-id="7173d-123">Value</span><span class="sxs-lookup"><span data-stu-id="7173d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7173d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7173d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7173d-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7173d-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7173d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7173d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7173d-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7173d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7173d-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7173d-128">End of client support</span></span><br/>    | <span data-ttu-id="7173d-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7173d-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="7173d-130">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7173d-130">End of server support</span></span><br/>    | <span data-ttu-id="7173d-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7173d-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="7173d-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7173d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7173d-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="7173d-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="7173d-134">IDL</span><span class="sxs-lookup"><span data-stu-id="7173d-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7173d-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7173d-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="7173d-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7173d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7173d-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7173d-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7173d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="7173d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7173d-139">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="7173d-139">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="7173d-140">**IEnumUserIdentity:: RESET**</span><span class="sxs-lookup"><span data-stu-id="7173d-140">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> </dl>

 

 




