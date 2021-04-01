---
title: Método INapClientManagement GetRegisteredSystemHealthAgents (NapManagement. h)
description: Recupera información acerca de los Sha registrados.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Método GetRegisteredSystemHealthAgents NAP
- Método GetRegisteredSystemHealthAgents NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método GetRegisteredSystemHealthAgents
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996694"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a><span data-ttu-id="a47c7-106">INapClientManagement:: GetRegisteredSystemHealthAgents (método)</span><span class="sxs-lookup"><span data-stu-id="a47c7-106">INapClientManagement::GetRegisteredSystemHealthAgents method</span></span>

> [!Note]  
> <span data-ttu-id="a47c7-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a47c7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a47c7-108">El método **GetRegisteredSystemHealthAgents** recupera información acerca de los Sha registrados.</span><span class="sxs-lookup"><span data-stu-id="a47c7-108">The **GetRegisteredSystemHealthAgents** method retrieves information about the registered SHAs.</span></span>

## <a name="syntax"></a><span data-ttu-id="a47c7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a47c7-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a><span data-ttu-id="a47c7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a47c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a47c7-111">*recuento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a47c7-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a47c7-112">Un puntero a un [**SystemHealthEntityCount**](nap-datatypes.md) que describe el número de Sha registrados.</span><span class="sxs-lookup"><span data-stu-id="a47c7-112">A pointer to a [**SystemHealthEntityCount**](nap-datatypes.md) that describes the number of registered SHAs.</span></span>

</dd> <dt>

<span data-ttu-id="a47c7-113">*agentes* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a47c7-113">*agents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a47c7-114">Puntero a una matriz de estructuras [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que describen los Sha registrados.</span><span class="sxs-lookup"><span data-stu-id="a47c7-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered SHAs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a47c7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a47c7-115">Return value</span></span>

<span data-ttu-id="a47c7-116">El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="a47c7-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="a47c7-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a47c7-117">Return code</span></span>                                                                                         | <span data-ttu-id="a47c7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a47c7-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a47c7-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a47c7-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="a47c7-120">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="a47c7-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a47c7-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a47c7-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="a47c7-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="a47c7-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a47c7-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a47c7-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="a47c7-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a47c7-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a47c7-125"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="a47c7-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a47c7-126">NapAgent no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a47c7-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="a47c7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a47c7-127">Requirements</span></span>



| <span data-ttu-id="a47c7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a47c7-128">Requirement</span></span> | <span data-ttu-id="a47c7-129">Value</span><span class="sxs-lookup"><span data-stu-id="a47c7-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a47c7-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a47c7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a47c7-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a47c7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a47c7-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a47c7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a47c7-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a47c7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a47c7-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a47c7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a47c7-135"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="a47c7-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="a47c7-136">IDL</span><span class="sxs-lookup"><span data-stu-id="a47c7-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a47c7-137"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a47c7-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="a47c7-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a47c7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a47c7-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a47c7-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="a47c7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a47c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a47c7-141">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="a47c7-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





