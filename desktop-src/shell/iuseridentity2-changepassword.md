---
description: ChangePassword no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'IUserIdentity2:: ChangePassword (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984606"
---
# <a name="iuseridentity2changepassword-method"></a><span data-ttu-id="72324-104">IUserIdentity2:: ChangePassword (método)</span><span class="sxs-lookup"><span data-stu-id="72324-104">IUserIdentity2::ChangePassword method</span></span>

<span data-ttu-id="72324-105">\[**ChangePassword** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="72324-105">\[**ChangePassword** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="72324-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="72324-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="72324-107">Establece una nueva contraseña para la identidad.</span><span class="sxs-lookup"><span data-stu-id="72324-107">Sets a new password for the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="72324-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72324-108">Syntax</span></span>


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a><span data-ttu-id="72324-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72324-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72324-110">*szOldPass* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72324-110">*szOldPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72324-111">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="72324-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="72324-112">Cadena de caracteres anchos que contiene la contraseña asociada actualmente a la identidad.</span><span class="sxs-lookup"><span data-stu-id="72324-112">The wide-character string that contains the password currently associated with the identity.</span></span>

</dd> <dt>

<span data-ttu-id="72324-113">_szNewPass \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="72324-113">_szNewPass\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72324-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="72324-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="72324-115">Cadena de caracteres anchos que contiene la nueva contraseña que se va a asociar a la identidad.</span><span class="sxs-lookup"><span data-stu-id="72324-115">The wide-character string that contains the new password to be associated with the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72324-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72324-116">Return value</span></span>

<span data-ttu-id="72324-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="72324-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="72324-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="72324-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72324-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72324-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72324-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72324-120">Remarks</span></span>

<span data-ttu-id="72324-121">El valor de *szOldPass* debe coincidir con la contraseña actual de la identidad de *szNewPass* que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="72324-121">The value of *szOldPass* must match the current password of the identity for *szNewPass* to be applied.</span></span> <span data-ttu-id="72324-122">Un valor incorrecto de *szOldPass* producirá un error en un valor devuelto de E \_ .</span><span class="sxs-lookup"><span data-stu-id="72324-122">An incorrect value of *szOldPass* will result in a return value of E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="72324-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72324-123">Requirements</span></span>



| <span data-ttu-id="72324-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="72324-124">Requirement</span></span> | <span data-ttu-id="72324-125">Value</span><span class="sxs-lookup"><span data-stu-id="72324-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72324-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72324-126">Minimum supported client</span></span><br/> | <span data-ttu-id="72324-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="72324-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="72324-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72324-128">Minimum supported server</span></span><br/> | <span data-ttu-id="72324-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72324-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="72324-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="72324-130">End of client support</span></span><br/>    | <span data-ttu-id="72324-131">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="72324-131">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="72324-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="72324-132">End of server support</span></span><br/>    | <span data-ttu-id="72324-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72324-133">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="72324-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72324-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="72324-135"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="72324-135"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="72324-136">IDL</span><span class="sxs-lookup"><span data-stu-id="72324-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72324-137"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72324-137"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="72324-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72324-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72324-139"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72324-139"><dt>Msident.dll</dt></span></span> </dl> |



 

 




