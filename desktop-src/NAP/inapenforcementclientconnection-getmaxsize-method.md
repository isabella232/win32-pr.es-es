---
title: Método INapEnforcementClientConnection GetMaxSize (NapEnforcementClient. h)
description: Obtiene el tamaño máximo del paquete SoH para este cliente.
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- Método GetMaxSize NAP
- Método GetMaxSize NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método GetMaxSize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d86cc71cd5da906146ab1577d58311d167d484
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801850"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a><span data-ttu-id="1ad65-106">INapEnforcementClientConnection:: GetMaxSize (método)</span><span class="sxs-lookup"><span data-stu-id="1ad65-106">INapEnforcementClientConnection::GetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="1ad65-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1ad65-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1ad65-108">El método **INapEnforcementClientConnection:: GetMaxSize** obtiene el tamaño máximo del paquete SOH para este cliente.</span><span class="sxs-lookup"><span data-stu-id="1ad65-108">The **INapEnforcementClientConnection::GetMaxSize** method gets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad65-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ad65-109">Syntax</span></span>


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="1ad65-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ad65-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad65-111">*MaxSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1ad65-111">*maxSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad65-112">Un puntero a un [**ProtocolMaxSize**](nap-datatypes.md) que indica el tamaño máximo, en bytes, del paquete SOH.</span><span class="sxs-lookup"><span data-stu-id="1ad65-112">A pointer to a [**ProtocolMaxSize**](nap-datatypes.md) that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ad65-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ad65-113">Return value</span></span>

<span data-ttu-id="1ad65-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="1ad65-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1ad65-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1ad65-115">Return code</span></span>                                                                                     | <span data-ttu-id="1ad65-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ad65-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ad65-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad65-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1ad65-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="1ad65-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1ad65-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad65-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1ad65-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="1ad65-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1ad65-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1ad65-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1ad65-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="1ad65-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1ad65-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ad65-123">Requirements</span></span>



| <span data-ttu-id="1ad65-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ad65-124">Requirement</span></span> | <span data-ttu-id="1ad65-125">Value</span><span class="sxs-lookup"><span data-stu-id="1ad65-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad65-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ad65-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad65-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ad65-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1ad65-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ad65-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad65-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ad65-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1ad65-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ad65-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ad65-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ad65-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ad65-132">IDL</span><span class="sxs-lookup"><span data-stu-id="1ad65-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1ad65-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1ad65-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="1ad65-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ad65-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ad65-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ad65-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1ad65-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ad65-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad65-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="1ad65-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





