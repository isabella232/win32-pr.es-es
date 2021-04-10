---
title: Método INapEnforcementClientConnection Getconnectionid ((NapEnforcementClient. h)
description: Se usa para obtener el identificador de conexión único del cliente.
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- Método Getconnectionid (NAP
- Método Getconnectionid (NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método Getconnectionid (
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151201"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a><span data-ttu-id="5c32c-106">INapEnforcementClientConnection:: Getconnectionid ((método)</span><span class="sxs-lookup"><span data-stu-id="5c32c-106">INapEnforcementClientConnection::GetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="5c32c-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5c32c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5c32c-108">El método **INapEnforcementClientConnection:: getconnectionid (** se usa para obtener el identificador de conexión único del cliente.</span><span class="sxs-lookup"><span data-stu-id="5c32c-108">The **INapEnforcementClientConnection::GetConnectionId** method is used to get the unique connection ID of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c32c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c32c-109">Syntax</span></span>


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="5c32c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c32c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c32c-111">*connectionId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5c32c-111">*connectionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c32c-112">Un puntero a un puntero a un [**ConnectionId**](nap-datatypes.md) que identifica de forma única esta conexión.</span><span class="sxs-lookup"><span data-stu-id="5c32c-112">A pointer to a pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies this connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c32c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c32c-113">Return value</span></span>

<span data-ttu-id="5c32c-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="5c32c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5c32c-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5c32c-115">Return code</span></span>                                                                                     | <span data-ttu-id="5c32c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c32c-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c32c-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="5c32c-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5c32c-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="5c32c-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5c32c-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5c32c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5c32c-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="5c32c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5c32c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5c32c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5c32c-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="5c32c-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c32c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c32c-123">Remarks</span></span>

<span data-ttu-id="5c32c-124">El identificador de conexión se usa principalmente con fines de registro.</span><span class="sxs-lookup"><span data-stu-id="5c32c-124">The connection ID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c32c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c32c-125">Requirements</span></span>



| <span data-ttu-id="5c32c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c32c-126">Requirement</span></span> | <span data-ttu-id="5c32c-127">Value</span><span class="sxs-lookup"><span data-stu-id="5c32c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c32c-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c32c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c32c-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5c32c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5c32c-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c32c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c32c-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c32c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c32c-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c32c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c32c-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c32c-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c32c-134">IDL</span><span class="sxs-lookup"><span data-stu-id="5c32c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c32c-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c32c-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5c32c-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c32c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c32c-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c32c-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5c32c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c32c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c32c-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="5c32c-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





