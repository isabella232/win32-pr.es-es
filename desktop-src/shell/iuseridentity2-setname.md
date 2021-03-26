---
description: 'IUserIdentity2:: SetName no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: 'IUserIdentity2:: SetName (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 0b0fd06ef4b582987e41c2343f2d4596db6b8528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985679"
---
# <a name="iuseridentity2setname-method"></a><span data-ttu-id="1d4f0-104">IUserIdentity2:: SetName (método)</span><span class="sxs-lookup"><span data-stu-id="1d4f0-104">IUserIdentity2::SetName method</span></span>

<span data-ttu-id="1d4f0-105">\[**IUserIdentity2:: setName** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="1d4f0-105">\[**IUserIdentity2::SetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="1d4f0-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="1d4f0-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="1d4f0-107">Establece el nombre para mostrar de la identidad.</span><span class="sxs-lookup"><span data-stu-id="1d4f0-107">Sets the display name of the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4f0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d4f0-108">Syntax</span></span>


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a><span data-ttu-id="1d4f0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d4f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d4f0-110">*pszName empiezan* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d4f0-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4f0-111">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="1d4f0-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="1d4f0-112">Cadena de caracteres anchos que contiene el nuevo nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="1d4f0-112">The wide-character string that contains the new name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d4f0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d4f0-113">Return value</span></span>

<span data-ttu-id="1d4f0-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1d4f0-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1d4f0-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1d4f0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d4f0-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d4f0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4f0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d4f0-117">Requirements</span></span>



| <span data-ttu-id="1d4f0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d4f0-118">Requirement</span></span> | <span data-ttu-id="1d4f0-119">Value</span><span class="sxs-lookup"><span data-stu-id="1d4f0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4f0-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d4f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4f0-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1d4f0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1d4f0-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d4f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4f0-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d4f0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1d4f0-124">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1d4f0-124">End of client support</span></span><br/>    | <span data-ttu-id="1d4f0-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1d4f0-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="1d4f0-126">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="1d4f0-126">End of server support</span></span><br/>    | <span data-ttu-id="1d4f0-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d4f0-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="1d4f0-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d4f0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d4f0-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4f0-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d4f0-130">IDL</span><span class="sxs-lookup"><span data-stu-id="1d4f0-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d4f0-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d4f0-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="1d4f0-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d4f0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d4f0-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d4f0-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4f0-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d4f0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4f0-135">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="1d4f0-135">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="1d4f0-136">**GetName**</span><span class="sxs-lookup"><span data-stu-id="1d4f0-136">**GetName**</span></span>](iuseridentity-getname.md)
</dt> </dl>

 

 




