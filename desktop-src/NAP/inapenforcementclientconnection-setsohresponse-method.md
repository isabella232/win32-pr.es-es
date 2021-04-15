---
title: Método INapEnforcementClientConnection SetSoHResponse (NapEnforcementClient. h)
description: Establece el SoH-Response y lo usa el cliente de cumplimiento al recibir un paquete.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- Método SetSoHResponse NAP
- Método SetSoHResponse NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdc403a1ff68e28f7d262e64ebe558226741b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491926"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a><span data-ttu-id="a33b0-106">INapEnforcementClientConnection:: SetSoHResponse (método)</span><span class="sxs-lookup"><span data-stu-id="a33b0-106">INapEnforcementClientConnection::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="a33b0-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a33b0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a33b0-108">El método **INapEnforcementClientConnection:: SetSoHResponse** establece el SoH-Response y lo usa el cliente de cumplimiento al recibir un paquete.</span><span class="sxs-lookup"><span data-stu-id="a33b0-108">The **INapEnforcementClientConnection::SetSoHResponse** method sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33b0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a33b0-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="a33b0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a33b0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a33b0-111">*sohResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a33b0-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33b0-112">Un puntero a una estructura [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) única, que es un BLOB de datos opacos para el aplicador.</span><span class="sxs-lookup"><span data-stu-id="a33b0-112">A pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a33b0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a33b0-113">Return value</span></span>

<span data-ttu-id="a33b0-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="a33b0-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a33b0-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a33b0-115">Return code</span></span>                                                                                     | <span data-ttu-id="a33b0-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a33b0-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a33b0-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="a33b0-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a33b0-118">El paquete SoH es válido.</span><span class="sxs-lookup"><span data-stu-id="a33b0-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="a33b0-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a33b0-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a33b0-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="a33b0-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a33b0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a33b0-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a33b0-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a33b0-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a33b0-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a33b0-123">Remarks</span></span>

<span data-ttu-id="a33b0-124">Un paquete de tamaño cero es válido.</span><span class="sxs-lookup"><span data-stu-id="a33b0-124">A zero-sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33b0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33b0-125">Requirements</span></span>



| <span data-ttu-id="a33b0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33b0-126">Requirement</span></span> | <span data-ttu-id="a33b0-127">Value</span><span class="sxs-lookup"><span data-stu-id="a33b0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a33b0-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a33b0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a33b0-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a33b0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a33b0-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a33b0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a33b0-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a33b0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a33b0-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a33b0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a33b0-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a33b0-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a33b0-134">IDL</span><span class="sxs-lookup"><span data-stu-id="a33b0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a33b0-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a33b0-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a33b0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a33b0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a33b0-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a33b0-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a33b0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a33b0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33b0-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a33b0-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





