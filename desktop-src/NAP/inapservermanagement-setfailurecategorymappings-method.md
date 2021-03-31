---
title: Método INapServerManagement SetFailureCategoryMappings (NapServerManagement. h)
description: Se usa para establecer las asignaciones de categorías de error de SHV.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Método SetFailureCategoryMappings NAP
- Método SetFailureCategoryMappings NAP, interfaz INapServerManagement
- Interfaz INapServerManagement NAP, método SetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996692"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a><span data-ttu-id="8a8e0-106">INapServerManagement:: SetFailureCategoryMappings (método)</span><span class="sxs-lookup"><span data-stu-id="8a8e0-106">INapServerManagement::SetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="8a8e0-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="8a8e0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8a8e0-108">El método **INapServerManagement:: SetFailureCategoryMappings** se usa para establecer las asignaciones de categorías de error de SHV.</span><span class="sxs-lookup"><span data-stu-id="8a8e0-108">The **INapServerManagement::SetFailureCategoryMappings** method is used to set the SHV's failure category mappings.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8e0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a8e0-109">Syntax</span></span>


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a><span data-ttu-id="8a8e0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a8e0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8e0-111">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8a8e0-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8e0-112">[**SystemHealthEntityId**](nap-type-constants.md) que contiene el identificador único del SHV.</span><span class="sxs-lookup"><span data-stu-id="8a8e0-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="8a8e0-113">*asignación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8a8e0-113">*mapping* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8e0-114">Una estructura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) que contiene los datos de asignación de la categoría de error.</span><span class="sxs-lookup"><span data-stu-id="8a8e0-114">A [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure that contains the failure category mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8e0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a8e0-115">Return value</span></span>

<span data-ttu-id="8a8e0-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="8a8e0-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8a8e0-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8a8e0-117">Return code</span></span>                                                                                     | <span data-ttu-id="8a8e0-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a8e0-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a8e0-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="8a8e0-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="8a8e0-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a8e0-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8a8e0-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8a8e0-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="8a8e0-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="8a8e0-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8a8e0-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8a8e0-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="8a8e0-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8a8e0-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8a8e0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a8e0-125">Requirements</span></span>



| <span data-ttu-id="8a8e0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a8e0-126">Requirement</span></span> | <span data-ttu-id="8a8e0-127">Value</span><span class="sxs-lookup"><span data-stu-id="8a8e0-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8e0-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a8e0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8e0-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8a8e0-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="8a8e0-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a8e0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8e0-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a8e0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8a8e0-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a8e0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a8e0-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a8e0-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a8e0-134">IDL</span><span class="sxs-lookup"><span data-stu-id="8a8e0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8a8e0-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a8e0-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="8a8e0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a8e0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a8e0-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8e0-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="8a8e0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a8e0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8e0-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="8a8e0-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





