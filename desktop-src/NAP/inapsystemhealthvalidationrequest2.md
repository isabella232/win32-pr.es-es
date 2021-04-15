---
title: Interfaz INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Proporciona métodos que se usan para admitir validadores de mantenimiento del sistema definidos por el desarrollador de la aplicación.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- Interfaz INapSystemHealthValidationRequest2 NAP
- Interfaz INapSystemHealthValidationRequest2 NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677007"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a><span data-ttu-id="72f99-105">Interfaz INapSystemHealthValidationRequest2</span><span class="sxs-lookup"><span data-stu-id="72f99-105">INapSystemHealthValidationRequest2 interface</span></span>

> [!Note]  
> <span data-ttu-id="72f99-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="72f99-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="72f99-107">La interfaz **INapSystemHealthValidationRequest2** proporciona métodos que se usan para admitir los validadores de mantenimiento del sistema definidos por el desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72f99-107">The **INapSystemHealthValidationRequest2** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="72f99-108">Esta interfaz hereda todos los métodos de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) y se debe usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="72f99-108">This interface inherits all the methods of [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="72f99-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="72f99-109">Members</span></span>

<span data-ttu-id="72f99-110">La interfaz **INapSystemHealthValidationRequest2** hereda de [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span><span class="sxs-lookup"><span data-stu-id="72f99-110">The **INapSystemHealthValidationRequest2** interface inherits from [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span></span> <span data-ttu-id="72f99-111">**INapSystemHealthValidationRequest2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="72f99-111">**INapSystemHealthValidationRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="72f99-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="72f99-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72f99-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="72f99-113">Methods</span></span>

<span data-ttu-id="72f99-114">La interfaz **INapSystemHealthValidationRequest2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="72f99-114">The **INapSystemHealthValidationRequest2** interface has these methods.</span></span>



| <span data-ttu-id="72f99-115">Método</span><span class="sxs-lookup"><span data-stu-id="72f99-115">Method</span></span>                                                                                                    | <span data-ttu-id="72f99-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="72f99-116">Description</span></span>                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="72f99-117">**INapSystemHealthValidationRequest2::GetConfigId**</span><span class="sxs-lookup"><span data-stu-id="72f99-117">**INapSystemHealthValidationRequest2::GetConfigId**</span></span>](inapsystemhealthvalidationrequest2-getconfigid.md) | <span data-ttu-id="72f99-118">Recupera el identificador de configuración en una solicitud de validación.</span><span class="sxs-lookup"><span data-stu-id="72f99-118">Retrieves the configuration id in a validation request.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="72f99-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72f99-119">Remarks</span></span>

<span data-ttu-id="72f99-120">Si un SHV no es compatible con [**INapComponentConfig3**](inapcomponentconfig3.md), esta interfaz no se aplica.</span><span class="sxs-lookup"><span data-stu-id="72f99-120">If an SHV doesn t support [**INapComponentConfig3**](inapcomponentconfig3.md), this interface doesn t apply.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f99-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72f99-121">Requirements</span></span>



| <span data-ttu-id="72f99-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72f99-122">Requirement</span></span> | <span data-ttu-id="72f99-123">Value</span><span class="sxs-lookup"><span data-stu-id="72f99-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f99-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72f99-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72f99-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="72f99-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="72f99-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72f99-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72f99-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="72f99-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="72f99-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72f99-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="72f99-129"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f99-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="72f99-130">IDL</span><span class="sxs-lookup"><span data-stu-id="72f99-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72f99-131"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72f99-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="72f99-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72f99-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72f99-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72f99-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="72f99-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="72f99-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f99-135">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="72f99-135">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[<span data-ttu-id="72f99-136">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="72f99-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="72f99-137">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="72f99-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





