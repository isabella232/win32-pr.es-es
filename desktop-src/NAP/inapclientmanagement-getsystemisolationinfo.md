---
title: Método INapClientManagement GetSystemIsolationInfo (NapManagement. h)
description: Recupera información sobre el estado de aislamiento de NapClient.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Método GetSystemIsolationInfo NAP
- Método GetSystemIsolationInfo NAP, interfaz INapClientManagement
- Interfaz INapClientManagement NAP, método GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422492"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a><span data-ttu-id="104dc-106">INapClientManagement:: GetSystemIsolationInfo (método)</span><span class="sxs-lookup"><span data-stu-id="104dc-106">INapClientManagement::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="104dc-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="104dc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="104dc-108">El método **GetSystemIsolationInfo** recupera información sobre el estado de aislamiento de NapClient.</span><span class="sxs-lookup"><span data-stu-id="104dc-108">The **GetSystemIsolationInfo** method retrieves information about the isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="104dc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="104dc-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="104dc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="104dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="104dc-111">*isolationInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="104dc-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="104dc-112">Un puntero a un puntero a una estructura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contiene información de estado de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="104dc-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="104dc-113">*unknownConnections* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="104dc-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="104dc-114">Un puntero a una marca que indica si alguna de las conexiones está en un estado desconocido.</span><span class="sxs-lookup"><span data-stu-id="104dc-114">A pointer to a flag that indicates whether any of the connections are in an unknown state.</span></span> <span data-ttu-id="104dc-115">Si cualquiera de ellos es, la marca se establece en **true**; en caso contrario, la marca se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="104dc-115">If any of them are, the flag is set to **TRUE**; otherwise the flag is set to **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="104dc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="104dc-116">Return value</span></span>

<span data-ttu-id="104dc-117">El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="104dc-117">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="104dc-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="104dc-118">Return code</span></span>                                                                                         | <span data-ttu-id="104dc-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="104dc-119">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="104dc-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="104dc-120"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="104dc-121">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="104dc-121">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="104dc-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="104dc-122"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="104dc-123">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="104dc-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="104dc-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="104dc-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="104dc-125">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="104dc-125">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="104dc-126"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="104dc-126"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="104dc-127">NapAgent no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="104dc-127">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="104dc-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="104dc-128">Remarks</span></span>

<span data-ttu-id="104dc-129">La información de aislamiento que se recupera no refleja Estados desconocidos.</span><span class="sxs-lookup"><span data-stu-id="104dc-129">The isolation information that is retrieved does not reflect unknown states.</span></span>

## <a name="requirements"></a><span data-ttu-id="104dc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="104dc-130">Requirements</span></span>



| <span data-ttu-id="104dc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="104dc-131">Requirement</span></span> | <span data-ttu-id="104dc-132">Value</span><span class="sxs-lookup"><span data-stu-id="104dc-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="104dc-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="104dc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="104dc-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="104dc-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="104dc-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="104dc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="104dc-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="104dc-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="104dc-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="104dc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="104dc-138"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="104dc-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="104dc-139">IDL</span><span class="sxs-lookup"><span data-stu-id="104dc-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="104dc-140"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="104dc-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="104dc-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="104dc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="104dc-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="104dc-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="104dc-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="104dc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="104dc-144">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="104dc-144">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





