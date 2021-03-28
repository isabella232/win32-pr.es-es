---
description: Establece u obtiene un valor que controla cómo se resuelve el identificador de seguridad (SID) del usuario en los nombres de usuario.
title: Propiedad DiskQuotaControl. UserNameResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: fbe079680191937f022bd45a491fad054e1a9033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984414"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="4deb5-103">Propiedad DiskQuotaControl. UserNameResolution</span><span class="sxs-lookup"><span data-stu-id="4deb5-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="4deb5-104">Establece u obtiene un valor que controla cómo se resuelve el identificador de seguridad (SID) del usuario en los nombres de usuario.</span><span class="sxs-lookup"><span data-stu-id="4deb5-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="4deb5-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4deb5-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4deb5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4deb5-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="4deb5-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4deb5-107">Property value</span></span>

<span data-ttu-id="4deb5-108">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4deb5-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="4deb5-109">Tipo de resolución</span><span class="sxs-lookup"><span data-stu-id="4deb5-109">Resolution Type</span></span> | <span data-ttu-id="4deb5-110">Value</span><span class="sxs-lookup"><span data-stu-id="4deb5-110">Value</span></span> | <span data-ttu-id="4deb5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4deb5-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4deb5-112">dqResolveNone</span><span class="sxs-lookup"><span data-stu-id="4deb5-112">dqResolveNone</span></span>   | <span data-ttu-id="4deb5-113">0</span><span class="sxs-lookup"><span data-stu-id="4deb5-113">0</span></span>     | <span data-ttu-id="4deb5-114">No resuelva la información del nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="4deb5-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="4deb5-115">dqResolveSync</span><span class="sxs-lookup"><span data-stu-id="4deb5-115">dqResolveSync</span></span>   | <span data-ttu-id="4deb5-116">1</span><span class="sxs-lookup"><span data-stu-id="4deb5-116">1</span></span>     | <span data-ttu-id="4deb5-117">Espere mientras se resuelve la información de nombre.</span><span class="sxs-lookup"><span data-stu-id="4deb5-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="4deb5-118">dqResolveAsync</span><span class="sxs-lookup"><span data-stu-id="4deb5-118">dqResolveAsync</span></span>  | <span data-ttu-id="4deb5-119">2</span><span class="sxs-lookup"><span data-stu-id="4deb5-119">2</span></span>     | <span data-ttu-id="4deb5-120">No espere a que se resuelva la información de nombre.</span><span class="sxs-lookup"><span data-stu-id="4deb5-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="4deb5-121">El evento [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) se desencadena cuando se resuelve el nombre.</span><span class="sxs-lookup"><span data-stu-id="4deb5-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4deb5-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4deb5-122">Remarks</span></span>

<span data-ttu-id="4deb5-123">Esta propiedad afecta a la enumeración de los objetos [**DIDiskQuotaUser**](didiskquotauser-object.md) y a los métodos [**adduser**](diskquotacontrol-adduser.md) y [**FindUser**](diskquotacontrol-finduser.md) .</span><span class="sxs-lookup"><span data-stu-id="4deb5-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="4deb5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4deb5-124">Requirements</span></span>



| <span data-ttu-id="4deb5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4deb5-125">Requirement</span></span> | <span data-ttu-id="4deb5-126">Value</span><span class="sxs-lookup"><span data-stu-id="4deb5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4deb5-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4deb5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4deb5-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4deb5-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4deb5-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4deb5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4deb5-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4deb5-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4deb5-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4deb5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4deb5-132"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4deb5-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4deb5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4deb5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4deb5-134">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="4deb5-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




