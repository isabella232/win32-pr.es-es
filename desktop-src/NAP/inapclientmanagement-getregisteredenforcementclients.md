---
title: Método INapClientManagement GetRegisteredEnforcementClients (NapManagement. h)
description: Recupera información acerca de los clientes de cumplimiento registrados.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Método GetRegisteredEnforcementClients NAP
- Método GetRegisteredEnforcementClients NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método GetRegisteredEnforcementClients
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491711"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a><span data-ttu-id="fab95-106">INapClientManagement:: GetRegisteredEnforcementClients (método)</span><span class="sxs-lookup"><span data-stu-id="fab95-106">INapClientManagement::GetRegisteredEnforcementClients method</span></span>

> [!Note]  
> <span data-ttu-id="fab95-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fab95-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fab95-108">El método **GetRegisteredEnforcementClients** recupera información sobre los clientes de cumplimiento registrados.</span><span class="sxs-lookup"><span data-stu-id="fab95-108">The **GetRegisteredEnforcementClients** method retrieves information about the registered enforcement clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab95-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fab95-109">Syntax</span></span>


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a><span data-ttu-id="fab95-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fab95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab95-111">*recuento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fab95-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fab95-112">Un puntero a un [**EnforcementEntityCount**](nap-datatypes.md) que contiene el número de clientes de cumplimiento registrados.</span><span class="sxs-lookup"><span data-stu-id="fab95-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of registered enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="fab95-113">*aplicadores* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fab95-113">*enforcers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fab95-114">Puntero a una matriz de estructuras [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que describen los clientes de cumplimiento registrados.</span><span class="sxs-lookup"><span data-stu-id="fab95-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered enforcement clients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fab95-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fab95-115">Return value</span></span>

<span data-ttu-id="fab95-116">El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="fab95-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="fab95-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fab95-117">Return code</span></span>                                                                                         | <span data-ttu-id="fab95-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fab95-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fab95-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="fab95-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="fab95-120">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="fab95-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fab95-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fab95-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="fab95-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="fab95-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fab95-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fab95-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="fab95-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="fab95-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fab95-125"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="fab95-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="fab95-126">NapAgent no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="fab95-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="fab95-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fab95-127">Requirements</span></span>



| <span data-ttu-id="fab95-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab95-128">Requirement</span></span> | <span data-ttu-id="fab95-129">Value</span><span class="sxs-lookup"><span data-stu-id="fab95-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fab95-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fab95-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fab95-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fab95-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fab95-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fab95-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fab95-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fab95-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fab95-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fab95-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fab95-135"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="fab95-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="fab95-136">IDL</span><span class="sxs-lookup"><span data-stu-id="fab95-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fab95-137"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fab95-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="fab95-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fab95-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fab95-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fab95-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="fab95-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="fab95-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab95-141">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="fab95-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





