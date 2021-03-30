---
title: Método INapSystemHealthAgentRequest GetCacheSoHFlag (NapSystemHealthAgent. h)
description: Solo se usa en NapAgent.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- Método GetCacheSoHFlag NAP
- Método GetCacheSoHFlag NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método GetCacheSoHFlag
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d8b458e4a49b690fe1f0f53482a72dd253c7c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534804"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a><span data-ttu-id="0a778-106">INapSystemHealthAgentRequest:: GetCacheSoHFlag (método)</span><span class="sxs-lookup"><span data-stu-id="0a778-106">INapSystemHealthAgentRequest::GetCacheSoHFlag method</span></span>

> [!Note]  
> <span data-ttu-id="0a778-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0a778-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0a778-108">El método **INapSystemHealthAgentRequest:: GetCacheSoHFlag** solo lo usa el NapAgent.</span><span class="sxs-lookup"><span data-stu-id="0a778-108">The **INapSystemHealthAgentRequest::GetCacheSoHFlag** method is used only by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a778-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a778-109">Syntax</span></span>


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="0a778-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a778-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a778-111">*cacheSohForLaterUse*</span><span class="sxs-lookup"><span data-stu-id="0a778-111">*cacheSohForLaterUse*</span></span> 
</dt> <dd>

<span data-ttu-id="0a778-112">Valor **booleano** que es **true** si NapAgent debe almacenar en caché el [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0a778-112">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a778-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a778-113">Return value</span></span>

<span data-ttu-id="0a778-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="0a778-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0a778-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0a778-115">Return code</span></span>                                                                                     | <span data-ttu-id="0a778-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a778-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a778-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="0a778-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0a778-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="0a778-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0a778-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0a778-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0a778-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="0a778-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0a778-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0a778-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0a778-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="0a778-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0a778-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a778-123">Requirements</span></span>



| <span data-ttu-id="0a778-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a778-124">Requirement</span></span> | <span data-ttu-id="0a778-125">Value</span><span class="sxs-lookup"><span data-stu-id="0a778-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a778-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a778-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0a778-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0a778-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0a778-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a778-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0a778-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a778-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0a778-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a778-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a778-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a778-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a778-132">IDL</span><span class="sxs-lookup"><span data-stu-id="0a778-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0a778-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a778-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="0a778-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a778-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a778-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a778-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="0a778-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a778-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a778-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="0a778-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





