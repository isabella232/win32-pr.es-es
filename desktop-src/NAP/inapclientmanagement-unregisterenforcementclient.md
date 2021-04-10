---
title: Método INapClientManagement UnregisterEnforcementClient (NapManagement. h)
description: Anula el registro de un cliente de cumplimiento con el sistema NAP.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- Método UnregisterEnforcementClient NAP
- Método UnregisterEnforcementClient NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método UnregisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150623"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a><span data-ttu-id="e9735-106">INapClientManagement:: UnregisterEnforcementClient (método)</span><span class="sxs-lookup"><span data-stu-id="e9735-106">INapClientManagement::UnregisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="e9735-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e9735-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e9735-108">El método **UnregisterEnforcementClient** anula el registro de un cliente de cumplimiento con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="e9735-108">The **UnregisterEnforcementClient** method unregisters an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9735-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9735-109">Syntax</span></span>


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="e9735-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9735-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9735-111">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e9735-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9735-112">Valor [**EnforcementEntityId**](nap-datatypes.md) que identifica el cliente de cumplimiento cuyo registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="e9735-112">An [**EnforcementEntityId**](nap-datatypes.md) value that identifies the enforcement client to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9735-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9735-113">Return value</span></span>

<span data-ttu-id="e9735-114">El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e9735-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="e9735-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e9735-115">Return code</span></span>                                                                                         | <span data-ttu-id="e9735-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9735-116">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9735-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e9735-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="e9735-118">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="e9735-118">Operation successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="e9735-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e9735-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="e9735-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="e9735-120">Permissions error, access denied.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e9735-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e9735-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="e9735-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="e9735-122">System resource limit, could not perform the operation.</span></span><br/>             |
| <dl> <span data-ttu-id="e9735-123"><dt>**NAP \_ E \_ todavía \_ enlazado**</dt></span><span class="sxs-lookup"><span data-stu-id="e9735-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="e9735-124">No se pudo anular el registro del cliente de cumplimiento y permanece enlazado.</span><span class="sxs-lookup"><span data-stu-id="e9735-124">The enforcement client could not be unregistered and remains bound.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e9735-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9735-125">Requirements</span></span>



| <span data-ttu-id="e9735-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9735-126">Requirement</span></span> | <span data-ttu-id="e9735-127">Value</span><span class="sxs-lookup"><span data-stu-id="e9735-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9735-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9735-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e9735-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e9735-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e9735-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9735-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e9735-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9735-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e9735-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9735-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9735-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9735-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9735-134">IDL</span><span class="sxs-lookup"><span data-stu-id="e9735-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9735-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9735-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="e9735-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9735-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9735-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9735-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="e9735-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9735-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9735-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="e9735-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





