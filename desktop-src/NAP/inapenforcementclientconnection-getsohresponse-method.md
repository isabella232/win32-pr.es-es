---
title: Método INapEnforcementClientConnection GetSoHResponse (NapEnforcementClient. h)
description: Obtiene el SoH-Response recibido por el cliente de cumplimiento.
ms.assetid: fc0084a3-a668-435e-8390-f322941c5cd4
keywords:
- Método GetSoHResponse NAP
- Método GetSoHResponse NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método GetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4d65135d6e4ce606a83eb08fdeed036cc62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905122"
---
# <a name="inapenforcementclientconnectiongetsohresponse-method"></a><span data-ttu-id="7742f-106">INapEnforcementClientConnection:: GetSoHResponse (método)</span><span class="sxs-lookup"><span data-stu-id="7742f-106">INapEnforcementClientConnection::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="7742f-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="7742f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7742f-108">El método **INapEnforcementClientConnection:: GetSoHResponse** obtiene el SoH-Response recibido por el cliente de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="7742f-108">The **INapEnforcementClientConnection::GetSoHResponse** method gets the SoH-Response received by the enforcement client.</span></span>

## <a name="syntax"></a><span data-ttu-id="7742f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7742f-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] NetworkSoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="7742f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7742f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7742f-111">*sohResponse* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7742f-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7742f-112">Un puntero a un puntero a una estructura [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) única, que es un BLOB de datos opacos para el aplicador.</span><span class="sxs-lookup"><span data-stu-id="7742f-112">A pointer to a pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7742f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7742f-113">Return value</span></span>

<span data-ttu-id="7742f-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="7742f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7742f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7742f-115">Return code</span></span>                                                                                     | <span data-ttu-id="7742f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7742f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7742f-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="7742f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7742f-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="7742f-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7742f-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7742f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7742f-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="7742f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7742f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7742f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7742f-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="7742f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7742f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7742f-123">Remarks</span></span>

<span data-ttu-id="7742f-124">Un paquete con un tamaño de cero bytes es válido.</span><span class="sxs-lookup"><span data-stu-id="7742f-124">A zero-byte sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="7742f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7742f-125">Requirements</span></span>



| <span data-ttu-id="7742f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7742f-126">Requirement</span></span> | <span data-ttu-id="7742f-127">Value</span><span class="sxs-lookup"><span data-stu-id="7742f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7742f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7742f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7742f-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7742f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7742f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7742f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7742f-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7742f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7742f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7742f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7742f-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7742f-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7742f-134">IDL</span><span class="sxs-lookup"><span data-stu-id="7742f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7742f-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7742f-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="7742f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7742f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7742f-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7742f-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7742f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="7742f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7742f-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="7742f-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





