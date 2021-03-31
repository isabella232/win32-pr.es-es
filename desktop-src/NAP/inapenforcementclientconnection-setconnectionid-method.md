---
title: Método INapEnforcementClientConnection SetConnectionId (NapEnforcementClient. h)
description: Se utiliza para establecer el identificador único de la conexión y el cliente de cumplimiento debe establecerla en cuanto se cree la conexión.
ms.assetid: 69d1a891-bc86-4c8a-b614-ebcdaa4a9057
keywords:
- Método SetConnectionId NAP
- Método SetConnectionId NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetConnectionId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9749be304170ec7706b637429f577e77411ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996179"
---
# <a name="inapenforcementclientconnectionsetconnectionid-method"></a><span data-ttu-id="c7de6-106">INapEnforcementClientConnection:: SetConnectionId (método)</span><span class="sxs-lookup"><span data-stu-id="c7de6-106">INapEnforcementClientConnection::SetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="c7de6-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c7de6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c7de6-108">El método **INapEnforcementClientConnection:: SetConnectionId** se usa para establecer el identificador único de la conexión y el cliente de cumplimiento debe establecerlo en cuanto se cree la conexión.</span><span class="sxs-lookup"><span data-stu-id="c7de6-108">The **INapEnforcementClientConnection::SetConnectionId** method is used to set the unique ID of the connection and must be set by the enforcement client as soon as the connection is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7de6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7de6-109">Syntax</span></span>


```C++
HRESULT SetConnectionId(
  [in] const ConnectionId *connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="c7de6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7de6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7de6-111">*connectionId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7de6-111">*connectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7de6-112">Un puntero a un [**ConnectionId**](nap-datatypes.md) que identifica de forma única una conexión.</span><span class="sxs-lookup"><span data-stu-id="c7de6-112">A pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7de6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7de6-113">Return value</span></span>

<span data-ttu-id="c7de6-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="c7de6-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c7de6-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c7de6-115">Return code</span></span>                                                                                     | <span data-ttu-id="c7de6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7de6-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7de6-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="c7de6-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c7de6-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="c7de6-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c7de6-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c7de6-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c7de6-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c7de6-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c7de6-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c7de6-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c7de6-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c7de6-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7de6-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7de6-123">Remarks</span></span>

<span data-ttu-id="c7de6-124">Este ConnectionID se usa principalmente con fines de registro.</span><span class="sxs-lookup"><span data-stu-id="c7de6-124">This ConnectionID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7de6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7de6-125">Requirements</span></span>



| <span data-ttu-id="c7de6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7de6-126">Requirement</span></span> | <span data-ttu-id="c7de6-127">Value</span><span class="sxs-lookup"><span data-stu-id="c7de6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7de6-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7de6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c7de6-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c7de6-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c7de6-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7de6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c7de6-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7de6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c7de6-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7de6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7de6-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7de6-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7de6-134">IDL</span><span class="sxs-lookup"><span data-stu-id="c7de6-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7de6-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7de6-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7de6-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7de6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7de6-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7de6-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c7de6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7de6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7de6-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="c7de6-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





