---
title: Método INapServerInfo GetFailureCategoryMappings (NapServerManagement. h)
description: Recupera las asignaciones de categorías de error para un SHA o SHV especificado.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- Método GetFailureCategoryMappings NAP
- Método GetFailureCategoryMappings NAP, interfaz INapServerInfo
- Interfaz INapServerInfo NAP, método GetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493234"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a><span data-ttu-id="f52fc-106">INapServerInfo:: GetFailureCategoryMappings (método)</span><span class="sxs-lookup"><span data-stu-id="f52fc-106">INapServerInfo::GetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="f52fc-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="f52fc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f52fc-108">El método **INapServerInfo:: GetFailureCategoryMappings** recupera las asignaciones de categorías de error para un Sha o SHV especificado.</span><span class="sxs-lookup"><span data-stu-id="f52fc-108">The **INapServerInfo::GetFailureCategoryMappings** method retrieves the failure category mappings for a specified SHA or SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="f52fc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f52fc-109">Syntax</span></span>


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a><span data-ttu-id="f52fc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f52fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52fc-111">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f52fc-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52fc-112">[**SystemHealthEntityId**](nap-type-constants.md) que contiene el identificador único de la Sha o el SHV.</span><span class="sxs-lookup"><span data-stu-id="f52fc-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHA or the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="f52fc-113">*asignación* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f52fc-113">*mapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f52fc-114">Un puntero a un [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) que contiene los datos de asignación.</span><span class="sxs-lookup"><span data-stu-id="f52fc-114">A pointer to a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) that contains the mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52fc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f52fc-115">Return value</span></span>

<span data-ttu-id="f52fc-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="f52fc-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f52fc-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f52fc-117">Return code</span></span>                                                                                     | <span data-ttu-id="f52fc-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f52fc-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f52fc-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="f52fc-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f52fc-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="f52fc-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f52fc-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f52fc-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f52fc-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="f52fc-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f52fc-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f52fc-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f52fc-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f52fc-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f52fc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f52fc-125">Requirements</span></span>



| <span data-ttu-id="f52fc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f52fc-126">Requirement</span></span> | <span data-ttu-id="f52fc-127">Value</span><span class="sxs-lookup"><span data-stu-id="f52fc-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f52fc-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52fc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f52fc-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f52fc-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="f52fc-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52fc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f52fc-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f52fc-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f52fc-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f52fc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f52fc-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="f52fc-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="f52fc-134">IDL</span><span class="sxs-lookup"><span data-stu-id="f52fc-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f52fc-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f52fc-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="f52fc-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f52fc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f52fc-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f52fc-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="f52fc-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f52fc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52fc-139">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="f52fc-139">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





