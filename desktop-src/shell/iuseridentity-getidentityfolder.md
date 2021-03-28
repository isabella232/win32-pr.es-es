---
description: GetIdentityFolder no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'IUserIdentity:: GetIdentityFolder (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984611"
---
# <a name="iuseridentitygetidentityfolder-method"></a><span data-ttu-id="06467-104">IUserIdentity:: GetIdentityFolder (método)</span><span class="sxs-lookup"><span data-stu-id="06467-104">IUserIdentity::GetIdentityFolder method</span></span>

<span data-ttu-id="06467-105">\[**GetIdentityFolder** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="06467-105">\[**GetIdentityFolder** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="06467-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="06467-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="06467-107">Obtiene la carpeta de archivos asociada a esta identidad.</span><span class="sxs-lookup"><span data-stu-id="06467-107">Gets the file folder associated with this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="06467-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06467-108">Syntax</span></span>


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="06467-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06467-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06467-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06467-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06467-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="06467-111">Type: **DWORD**</span></span>

<span data-ttu-id="06467-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="06467-112">Required.</span></span> <span data-ttu-id="06467-113">Valor que especifica si la carpeta asociada a esta identidad es roaming.</span><span class="sxs-lookup"><span data-stu-id="06467-113">A value that specifies whether the folder associated with this identity is roaming.</span></span> <span data-ttu-id="06467-114">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06467-114">Must be one of the following values.</span></span>

<dt>



 <span data-ttu-id="06467-115">(GIF \_ ) carpeta móvil \_ )</span><span class="sxs-lookup"><span data-stu-id="06467-115">(GIF\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="06467-116">La carpeta está en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="06467-116">The folder is roaming.</span></span>

</dd> <dt>



 <span data-ttu-id="06467-117">(GIF \_ ) \_carpeta no móvil \_ )</span><span class="sxs-lookup"><span data-stu-id="06467-117">(GIF\_NON\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="06467-118">La carpeta es local.</span><span class="sxs-lookup"><span data-stu-id="06467-118">The folder is local.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="06467-119">*pszPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06467-119">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06467-120">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="06467-120">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="06467-121">Puntero a una cadena de caracteres anchos que recibe la ruta de acceso de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="06467-121">A pointer to a wide-character string that receives the folder path.</span></span>

</dd> <dt>

<span data-ttu-id="06467-122">_ulBuffSize \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="06467-122">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06467-123">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="06467-123">Type: **ULONG**</span></span>

<span data-ttu-id="06467-124">Valor que especifica el tamaño de *pszPath*.</span><span class="sxs-lookup"><span data-stu-id="06467-124">A value that specifies the size of *pszPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06467-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06467-125">Return value</span></span>

<span data-ttu-id="06467-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06467-126">Type: **HRESULT**</span></span>

<span data-ttu-id="06467-127">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="06467-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06467-128">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06467-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="06467-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06467-129">Requirements</span></span>



| <span data-ttu-id="06467-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="06467-130">Requirement</span></span> | <span data-ttu-id="06467-131">Value</span><span class="sxs-lookup"><span data-stu-id="06467-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06467-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06467-132">Minimum supported client</span></span><br/> | <span data-ttu-id="06467-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="06467-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="06467-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06467-134">Minimum supported server</span></span><br/> | <span data-ttu-id="06467-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="06467-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="06467-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="06467-136">End of client support</span></span><br/>    | <span data-ttu-id="06467-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="06467-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="06467-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="06467-138">End of server support</span></span><br/>    | <span data-ttu-id="06467-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="06467-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="06467-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06467-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="06467-141"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="06467-141"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="06467-142">IDL</span><span class="sxs-lookup"><span data-stu-id="06467-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06467-143"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06467-143"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="06467-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06467-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06467-145"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06467-145"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06467-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="06467-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06467-147">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="06467-147">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="06467-148">**IUserIdentity::OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="06467-148">**IUserIdentity::OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




