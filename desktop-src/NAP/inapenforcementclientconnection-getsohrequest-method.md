---
title: Método INapEnforcementClientConnection GetSoHRequest (NapEnforcementClient. h)
description: Obtiene la solicitud de SoH actual.
ms.assetid: 21397a0d-ef18-494e-9c5a-43d7f6216a67
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6115e607f810aef67911ec7d7800d35207368e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996180"
---
# <a name="inapenforcementclientconnectiongetsohrequest-method"></a><span data-ttu-id="49760-106">INapEnforcementClientConnection:: GetSoHRequest (método)</span><span class="sxs-lookup"><span data-stu-id="49760-106">INapEnforcementClientConnection::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="49760-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="49760-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="49760-108">El método **INapEnforcementClientConnection:: GetSoHRequest** obtiene la solicitud de SOH actual.</span><span class="sxs-lookup"><span data-stu-id="49760-108">The **INapEnforcementClientConnection::GetSoHRequest** method gets the current SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="49760-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49760-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] NetworkSoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="49760-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49760-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49760-111">*sohRequest* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="49760-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49760-112">Un puntero a un puntero a una estructura [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , que es un BLOB de datos opacos para el aplicador.</span><span class="sxs-lookup"><span data-stu-id="49760-112">A pointer to a pointer to a [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49760-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49760-113">Return value</span></span>

<span data-ttu-id="49760-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="49760-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="49760-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="49760-115">Return code</span></span>                                                                                     | <span data-ttu-id="49760-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="49760-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="49760-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="49760-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="49760-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="49760-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="49760-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="49760-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="49760-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="49760-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="49760-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="49760-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="49760-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="49760-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="49760-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49760-123">Remarks</span></span>

<span data-ttu-id="49760-124">Lo establece el NapAgent y lo consultan los enforcedores para enviarlos en la conexión.</span><span class="sxs-lookup"><span data-stu-id="49760-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="49760-125">Un paquete SoH de longitud cero no es válido.</span><span class="sxs-lookup"><span data-stu-id="49760-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="49760-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49760-126">Requirements</span></span>



| <span data-ttu-id="49760-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="49760-127">Requirement</span></span> | <span data-ttu-id="49760-128">Value</span><span class="sxs-lookup"><span data-stu-id="49760-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49760-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49760-129">Minimum supported client</span></span><br/> | <span data-ttu-id="49760-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="49760-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="49760-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49760-131">Minimum supported server</span></span><br/> | <span data-ttu-id="49760-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="49760-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="49760-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49760-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="49760-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="49760-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="49760-135">IDL</span><span class="sxs-lookup"><span data-stu-id="49760-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49760-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49760-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="49760-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49760-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49760-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49760-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="49760-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="49760-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49760-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="49760-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





