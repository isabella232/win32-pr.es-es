---
description: Establece u obtiene un valor que controla cómo se resuelve el identificador de seguridad de usuario (SID) en nombres de usuario.
title: Propiedad DiskQuotaControl.UserNameResolution
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
ms.openlocfilehash: 169f4db6e135392e9548767520f6d2b0bd2d527c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841466"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="5faaa-103">Propiedad DiskQuotaControl.UserNameResolution</span><span class="sxs-lookup"><span data-stu-id="5faaa-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="5faaa-104">Establece u obtiene un valor que controla cómo se resuelve el identificador de seguridad de usuario (SID) en nombres de usuario.</span><span class="sxs-lookup"><span data-stu-id="5faaa-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="5faaa-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5faaa-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5faaa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5faaa-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="5faaa-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5faaa-107">Property value</span></span>

<span data-ttu-id="5faaa-108">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5faaa-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="5faaa-109">Tipo de resolución</span><span class="sxs-lookup"><span data-stu-id="5faaa-109">Resolution Type</span></span> | <span data-ttu-id="5faaa-110">Value</span><span class="sxs-lookup"><span data-stu-id="5faaa-110">Value</span></span> | <span data-ttu-id="5faaa-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5faaa-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5faaa-112">dqResolveNone</span><span class="sxs-lookup"><span data-stu-id="5faaa-112">dqResolveNone</span></span>   | <span data-ttu-id="5faaa-113">0</span><span class="sxs-lookup"><span data-stu-id="5faaa-113">0</span></span>     | <span data-ttu-id="5faaa-114">No resuelva la información de nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="5faaa-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="5faaa-115">dqResolveSync</span><span class="sxs-lookup"><span data-stu-id="5faaa-115">dqResolveSync</span></span>   | <span data-ttu-id="5faaa-116">1</span><span class="sxs-lookup"><span data-stu-id="5faaa-116">1</span></span>     | <span data-ttu-id="5faaa-117">Espere mientras resuelve la información de nombre.</span><span class="sxs-lookup"><span data-stu-id="5faaa-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="5faaa-118">dqResolveAsync</span><span class="sxs-lookup"><span data-stu-id="5faaa-118">dqResolveAsync</span></span>  | <span data-ttu-id="5faaa-119">2</span><span class="sxs-lookup"><span data-stu-id="5faaa-119">2</span></span>     | <span data-ttu-id="5faaa-120">No espere mientras resuelve la información de nombre.</span><span class="sxs-lookup"><span data-stu-id="5faaa-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="5faaa-121">El [**evento OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) se produce cuando se resuelve el nombre.</span><span class="sxs-lookup"><span data-stu-id="5faaa-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5faaa-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5faaa-122">Remarks</span></span>

<span data-ttu-id="5faaa-123">Esta propiedad afecta a la enumeración de [**objetos DIDiskQuotaUser**](didiskquotauser-object.md) y a los [**métodos AddUser**](diskquotacontrol-adduser.md) [**y FindUser.**](diskquotacontrol-finduser.md)</span><span class="sxs-lookup"><span data-stu-id="5faaa-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="5faaa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5faaa-124">Requirements</span></span>



| <span data-ttu-id="5faaa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5faaa-125">Requirement</span></span> | <span data-ttu-id="5faaa-126">Value</span><span class="sxs-lookup"><span data-stu-id="5faaa-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5faaa-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5faaa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5faaa-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5faaa-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5faaa-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5faaa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5faaa-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5faaa-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5faaa-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5faaa-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5faaa-132"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5faaa-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5faaa-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5faaa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5faaa-134">**DiskQuotaControl (objeto)**</span><span class="sxs-lookup"><span data-stu-id="5faaa-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




