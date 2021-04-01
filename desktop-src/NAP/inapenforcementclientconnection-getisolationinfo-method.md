---
title: Método INapEnforcementClientConnection GetIsolationInfo (NapEnforcementClient. h)
description: Se usa para obtener la información de aislamiento del cliente.
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- Método GetIsolationInfo NAP
- Método GetIsolationInfo NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método GetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890f7268801fda77a9794ed21c4d36e78a52dd5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997134"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a><span data-ttu-id="c3c19-106">INapEnforcementClientConnection:: GetIsolationInfo (método)</span><span class="sxs-lookup"><span data-stu-id="c3c19-106">INapEnforcementClientConnection::GetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="c3c19-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c3c19-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c3c19-108">El método **INapEnforcementClientConnection:: GetIsolationInfo** se usa para obtener la información de aislamiento del cliente.</span><span class="sxs-lookup"><span data-stu-id="c3c19-108">The **INapEnforcementClientConnection::GetIsolationInfo** method is used get the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c19-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3c19-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c3c19-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3c19-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3c19-111">*isolationInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c3c19-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3c19-112">Un puntero a un puntero a una estructura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contiene el estado de Conectividad del cliente.</span><span class="sxs-lookup"><span data-stu-id="c3c19-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3c19-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3c19-113">Return value</span></span>

<span data-ttu-id="c3c19-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="c3c19-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c3c19-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c3c19-115">Return code</span></span>                                                                                     | <span data-ttu-id="c3c19-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3c19-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3c19-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="c3c19-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c3c19-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="c3c19-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c3c19-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c3c19-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c3c19-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c3c19-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c3c19-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c3c19-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c3c19-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c3c19-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3c19-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3c19-123">Remarks</span></span>

<span data-ttu-id="c3c19-124">La NapAgent establece esta información después de procesar una [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) y el exigidor no debe establecerla.</span><span class="sxs-lookup"><span data-stu-id="c3c19-124">This information is set by the NapAgent after processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c19-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3c19-125">Requirements</span></span>



| <span data-ttu-id="c3c19-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3c19-126">Requirement</span></span> | <span data-ttu-id="c3c19-127">Value</span><span class="sxs-lookup"><span data-stu-id="c3c19-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c19-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3c19-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c19-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c3c19-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c3c19-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3c19-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c19-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3c19-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c3c19-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3c19-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3c19-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3c19-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3c19-134">IDL</span><span class="sxs-lookup"><span data-stu-id="c3c19-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c3c19-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3c19-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="c3c19-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3c19-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3c19-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3c19-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c3c19-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3c19-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3c19-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="c3c19-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





