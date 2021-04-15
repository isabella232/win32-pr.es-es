---
title: Método INapClientManagement UnregisterSystemHealthAgent (NapManagement. h)
description: Anula el registro de un SHA con el sistema NAP.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Método UnregisterSystemHealthAgent NAP
- Método UnregisterSystemHealthAgent NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método UnregisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676859"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a><span data-ttu-id="e3bbf-106">INapClientManagement:: UnregisterSystemHealthAgent (método)</span><span class="sxs-lookup"><span data-stu-id="e3bbf-106">INapClientManagement::UnregisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="e3bbf-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e3bbf-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e3bbf-108">El método **UnregisterSystemHealthAgent** anula el registro de un Sha con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="e3bbf-108">The **UnregisterSystemHealthAgent** method unregisters an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3bbf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3bbf-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="e3bbf-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3bbf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3bbf-111">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e3bbf-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bbf-112">[**SystemHealthEntityId**](nap-datatypes.md) que identifica el agente de mantenimiento del sistema cuyo registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="e3bbf-112">A [**SystemHealthEntityId**](nap-datatypes.md) that identifies the System Health Agent to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3bbf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3bbf-113">Return value</span></span>

<span data-ttu-id="e3bbf-114">El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e3bbf-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="e3bbf-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e3bbf-115">Return code</span></span>                                                                                         | <span data-ttu-id="e3bbf-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3bbf-116">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3bbf-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e3bbf-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="e3bbf-118">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="e3bbf-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e3bbf-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e3bbf-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="e3bbf-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="e3bbf-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e3bbf-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e3bbf-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="e3bbf-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="e3bbf-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e3bbf-123"><dt>**NAP \_ E \_ todavía \_ enlazado**</dt></span><span class="sxs-lookup"><span data-stu-id="e3bbf-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="e3bbf-124">SHA permanece enlazado y no se pudo anular el registro.</span><span class="sxs-lookup"><span data-stu-id="e3bbf-124">The SHA remains bound and could not be unregistered.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="e3bbf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3bbf-125">Requirements</span></span>



| <span data-ttu-id="e3bbf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3bbf-126">Requirement</span></span> | <span data-ttu-id="e3bbf-127">Value</span><span class="sxs-lookup"><span data-stu-id="e3bbf-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3bbf-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3bbf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e3bbf-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e3bbf-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e3bbf-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3bbf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e3bbf-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3bbf-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e3bbf-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3bbf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3bbf-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3bbf-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3bbf-134">IDL</span><span class="sxs-lookup"><span data-stu-id="e3bbf-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3bbf-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3bbf-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="e3bbf-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e3bbf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3bbf-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3bbf-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="e3bbf-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3bbf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3bbf-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="e3bbf-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





