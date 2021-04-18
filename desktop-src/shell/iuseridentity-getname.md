---
description: 'IUserIdentity:: GetName no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: 'IUserIdentity:: GetName (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88c0a3d08ff917c2cc9fd59f15e4c23fc22fc79d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985403"
---
# <a name="iuseridentitygetname-method"></a><span data-ttu-id="8288d-104">IUserIdentity:: GetName (método)</span><span class="sxs-lookup"><span data-stu-id="8288d-104">IUserIdentity::GetName method</span></span>

<span data-ttu-id="8288d-105">\[**IUserIdentity:: GetName** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="8288d-105">\[**IUserIdentity::GetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="8288d-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="8288d-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="8288d-107">Obtiene el nombre asociado a esta identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="8288d-107">Gets the name associated with this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="8288d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8288d-108">Syntax</span></span>


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="8288d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8288d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8288d-110">*pszName empiezan* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8288d-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8288d-111">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="8288d-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="8288d-112">Puntero a una cadena de caracteres anchos que recibe el nombre de esta identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="8288d-112">A pointer to a wide-character string that receives the name of this user identity.</span></span>

</dd> <dt>

<span data-ttu-id="8288d-113">_ulBuffSize \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8288d-113">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8288d-114">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="8288d-114">Type: **ULONG**</span></span>

<span data-ttu-id="8288d-115">Valor que especifica el tamaño de *pszName empiezan*.</span><span class="sxs-lookup"><span data-stu-id="8288d-115">A value that specifies the size of *pszName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8288d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8288d-116">Return value</span></span>

<span data-ttu-id="8288d-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8288d-117">Type: **HRESULT**</span></span>

<span data-ttu-id="8288d-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8288d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8288d-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8288d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8288d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8288d-120">Requirements</span></span>



| <span data-ttu-id="8288d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8288d-121">Requirement</span></span> | <span data-ttu-id="8288d-122">Value</span><span class="sxs-lookup"><span data-stu-id="8288d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8288d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8288d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8288d-124">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8288d-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8288d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8288d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8288d-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8288d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8288d-127">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8288d-127">End of client support</span></span><br/>    | <span data-ttu-id="8288d-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8288d-128">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="8288d-129">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8288d-129">End of server support</span></span><br/>    | <span data-ttu-id="8288d-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8288d-130">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="8288d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8288d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8288d-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="8288d-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="8288d-133">IDL</span><span class="sxs-lookup"><span data-stu-id="8288d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8288d-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8288d-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="8288d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8288d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8288d-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8288d-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8288d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8288d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8288d-138">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="8288d-138">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="8288d-139">**SetName**</span><span class="sxs-lookup"><span data-stu-id="8288d-139">**SetName**</span></span>](iuseridentity2-setname.md)
</dt> </dl>

 

 




