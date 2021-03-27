---
description: IdentityInformationChanged no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'IIdentityChangeNotify:: IdentityInformationChanged (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909521"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a><span data-ttu-id="6fc9c-104">IIdentityChangeNotify:: IdentityInformationChanged (método)</span><span class="sxs-lookup"><span data-stu-id="6fc9c-104">IIdentityChangeNotify::IdentityInformationChanged method</span></span>

<span data-ttu-id="6fc9c-105">\[**IdentityInformationChanged** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-105">\[**IdentityInformationChanged** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="6fc9c-106">En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="6fc9c-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="6fc9c-107">Se llama cuando ha cambiado la información sobre una identidad de usuario o cuando se ha agregado o eliminado una identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-107">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc9c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6fc9c-108">Syntax</span></span>


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a><span data-ttu-id="6fc9c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fc9c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc9c-110">*dwType*</span><span class="sxs-lookup"><span data-stu-id="6fc9c-110">*dwType*</span></span> 
</dt> <dd>

<span data-ttu-id="6fc9c-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6fc9c-111">Type: **DWORD**</span></span>

<span data-ttu-id="6fc9c-112">Valor que especifica el tipo de información que se ha cambiado o la operación realizada en una identidad.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-112">A value that specifies the type of information changed, or the operation performed on an identity.</span></span> <span data-ttu-id="6fc9c-113">Puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-113">Can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="6fc9c-114">(IIC \_ \_identidad actual \_ modificada)</span><span class="sxs-lookup"><span data-stu-id="6fc9c-114">(IIC\_CURRENT\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="6fc9c-115">La identidad actual se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-115">The current identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="6fc9c-116">(IIC \_ IDENTIDAD \_ cambiada)</span><span class="sxs-lookup"><span data-stu-id="6fc9c-116">(IIC\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="6fc9c-117">Se ha modificado una identidad.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-117">An identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="6fc9c-118">(IIC \_ IDENTIDAD \_ eliminada)</span><span class="sxs-lookup"><span data-stu-id="6fc9c-118">(IIC\_IDENTITY\_DELETED)</span></span>


</dt> <dd>

<span data-ttu-id="6fc9c-119">Se ha eliminado una identidad.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-119">An identity has been deleted.</span></span>

</dd> <dt>



 <span data-ttu-id="6fc9c-120">(IIC \_ IDENTIDAD \_ agregada)</span><span class="sxs-lookup"><span data-stu-id="6fc9c-120">(IIC\_IDENTITY\_ADDED)</span></span>


</dt> <dd>

<span data-ttu-id="6fc9c-121">Se ha agregado una nueva identidad.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-121">A new identity has been added.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc9c-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fc9c-122">Return value</span></span>

<span data-ttu-id="6fc9c-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6fc9c-123">Type: **HRESULT**</span></span>

<span data-ttu-id="6fc9c-124">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fc9c-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fc9c-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fc9c-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fc9c-126">Remarks</span></span>

<span data-ttu-id="6fc9c-127">Puede implementar este método para proporcionar un comportamiento personalizado para la aplicación cuando se ha modificado la lista de identidades de usuario en el sistema.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-127">You may implement this method to provide custom behavior for your application when the list of user identities on the system has been modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc9c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fc9c-128">Requirements</span></span>



| <span data-ttu-id="6fc9c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc9c-129">Requirement</span></span> | <span data-ttu-id="6fc9c-130">Value</span><span class="sxs-lookup"><span data-stu-id="6fc9c-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc9c-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fc9c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc9c-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6fc9c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6fc9c-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fc9c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc9c-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6fc9c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6fc9c-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6fc9c-135">End of client support</span></span><br/>    | <span data-ttu-id="6fc9c-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6fc9c-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="6fc9c-137">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6fc9c-137">End of server support</span></span><br/>    | <span data-ttu-id="6fc9c-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6fc9c-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="6fc9c-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fc9c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc9c-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc9c-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fc9c-141">IDL</span><span class="sxs-lookup"><span data-stu-id="6fc9c-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6fc9c-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6fc9c-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="6fc9c-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6fc9c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fc9c-144"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fc9c-144"><dt>Msoe.dll</dt></span></span> </dl>    |



 

 




