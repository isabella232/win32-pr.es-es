---
title: Método INapEnforcementClientConnection SetSoHRequest (NapEnforcementClient. h)
description: Establece la solicitud de SoH.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- Método SetSoHRequest NAP
- Método SetSoHRequest NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801832"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a><span data-ttu-id="f2119-106">INapEnforcementClientConnection:: SetSoHRequest (método)</span><span class="sxs-lookup"><span data-stu-id="f2119-106">INapEnforcementClientConnection::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="f2119-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="f2119-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f2119-108">El método **INapEnforcementClientConnection:: SetSoHRequest** establece la solicitud de SOH.</span><span class="sxs-lookup"><span data-stu-id="f2119-108">The **INapEnforcementClientConnection::SetSoHRequest** method sets the SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2119-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2119-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="f2119-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2119-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2119-111">*sohRequest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2119-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2119-112">Un puntero a una estructura [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) única, que es un BLOB de datos opacos para el aplicador.</span><span class="sxs-lookup"><span data-stu-id="f2119-112">A pointer to a unique [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2119-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2119-113">Return value</span></span>

<span data-ttu-id="f2119-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="f2119-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f2119-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f2119-115">Return code</span></span>                                                                                     | <span data-ttu-id="f2119-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2119-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2119-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="f2119-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f2119-118">El paquete SoH es válido.</span><span class="sxs-lookup"><span data-stu-id="f2119-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="f2119-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f2119-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f2119-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="f2119-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f2119-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f2119-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f2119-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f2119-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f2119-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2119-123">Remarks</span></span>

<span data-ttu-id="f2119-124">Lo establece el NapAgent y lo consultan los enforcedores para enviarlos en la conexión.</span><span class="sxs-lookup"><span data-stu-id="f2119-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="f2119-125">Un paquete SoH de longitud cero no es válido.</span><span class="sxs-lookup"><span data-stu-id="f2119-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2119-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2119-126">Requirements</span></span>



| <span data-ttu-id="f2119-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2119-127">Requirement</span></span> | <span data-ttu-id="f2119-128">Value</span><span class="sxs-lookup"><span data-stu-id="f2119-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2119-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2119-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f2119-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2119-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f2119-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2119-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f2119-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2119-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f2119-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2119-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2119-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2119-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2119-135">IDL</span><span class="sxs-lookup"><span data-stu-id="f2119-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2119-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2119-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="f2119-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2119-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2119-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2119-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f2119-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2119-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2119-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="f2119-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





