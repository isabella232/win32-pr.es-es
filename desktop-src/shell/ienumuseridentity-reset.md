---
description: Restablece el recuento interno de interfaces recuperadas en la enumeración.
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'IEnumUserIdentity:: RESET (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 05b3c5d38575fa1b2957c28070d642ad15f846ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276740"
---
# <a name="ienumuseridentityreset-method"></a><span data-ttu-id="21866-103">IEnumUserIdentity:: RESET (método)</span><span class="sxs-lookup"><span data-stu-id="21866-103">IEnumUserIdentity::Reset method</span></span>

<span data-ttu-id="21866-104">\[**IEnumUserIdentity:: RESET** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="21866-104">\[**IEnumUserIdentity::Reset** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="21866-105">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="21866-105">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="21866-106">Restablece el recuento interno de interfaces recuperadas en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="21866-106">Resets the internal count of retrieved interfaces in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="21866-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21866-107">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="21866-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21866-108">Parameters</span></span>

<span data-ttu-id="21866-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="21866-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21866-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21866-110">Return value</span></span>

<span data-ttu-id="21866-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="21866-111">Type: **HRESULT**</span></span>

<span data-ttu-id="21866-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="21866-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21866-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21866-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21866-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21866-114">Remarks</span></span>

<span data-ttu-id="21866-115">[**IEnumUserIdentity**](ienumuseridentity.md) mantiene un recuento interno que especifica la interfaz que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="21866-115">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="21866-116">Al llamar a este método, se restablecerá el valor de este recuento.</span><span class="sxs-lookup"><span data-stu-id="21866-116">Calling this method will reset the value of this count.</span></span>

## <a name="requirements"></a><span data-ttu-id="21866-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21866-117">Requirements</span></span>



| <span data-ttu-id="21866-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="21866-118">Requirement</span></span> | <span data-ttu-id="21866-119">Value</span><span class="sxs-lookup"><span data-stu-id="21866-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21866-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21866-120">Minimum supported client</span></span><br/> | <span data-ttu-id="21866-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="21866-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="21866-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21866-122">Minimum supported server</span></span><br/> | <span data-ttu-id="21866-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="21866-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="21866-124">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="21866-124">End of client support</span></span><br/>    | <span data-ttu-id="21866-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="21866-125">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="21866-126">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="21866-126">End of server support</span></span><br/>    | <span data-ttu-id="21866-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21866-127">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="21866-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21866-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="21866-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="21866-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="21866-130">IDL</span><span class="sxs-lookup"><span data-stu-id="21866-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21866-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21866-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="21866-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21866-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21866-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21866-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21866-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="21866-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21866-135">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="21866-135">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="21866-136">**IEnumUserIdentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="21866-136">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="21866-137">**IEnumUserIdentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="21866-137">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> <dt>

[<span data-ttu-id="21866-138">**IEnumUserIdentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="21866-138">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




