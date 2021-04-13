---
title: Método INapEnforcementClientConnection SetMaxSize (NapEnforcementClient. h)
description: Establece el tamaño máximo del paquete SoH para este cliente.
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- Método SetMaxSize NAP
- Método SetMaxSize NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetMaxSize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b10d7bc1a023371683f17bb3e6e12cd578fa964
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422177"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a><span data-ttu-id="5974c-106">INapEnforcementClientConnection:: SetMaxSize (método)</span><span class="sxs-lookup"><span data-stu-id="5974c-106">INapEnforcementClientConnection::SetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="5974c-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5974c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5974c-108">El método **INapEnforcementClientConnection:: SetMaxSize** establece el tamaño máximo del paquete SOH para este cliente.</span><span class="sxs-lookup"><span data-stu-id="5974c-108">The **INapEnforcementClientConnection::SetMaxSize** method sets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="5974c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5974c-109">Syntax</span></span>


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="5974c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5974c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5974c-111">*MaxSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5974c-111">*maxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5974c-112">Una estructura [**ProtocolMaxSize**](nap-datatypes.md) que indica el tamaño máximo, en bytes, del paquete SOH.</span><span class="sxs-lookup"><span data-stu-id="5974c-112">A [**ProtocolMaxSize**](nap-datatypes.md) structure that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5974c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5974c-113">Return value</span></span>

<span data-ttu-id="5974c-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="5974c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5974c-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5974c-115">Return code</span></span>                                                                                     | <span data-ttu-id="5974c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5974c-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5974c-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="5974c-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5974c-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="5974c-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5974c-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5974c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5974c-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="5974c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5974c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5974c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5974c-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="5974c-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5974c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5974c-123">Remarks</span></span>

<span data-ttu-id="5974c-124">El cliente de cumplimiento establece este valor.</span><span class="sxs-lookup"><span data-stu-id="5974c-124">This value is set by the enforcement client.</span></span>

## <a name="requirements"></a><span data-ttu-id="5974c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5974c-125">Requirements</span></span>



| <span data-ttu-id="5974c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5974c-126">Requirement</span></span> | <span data-ttu-id="5974c-127">Value</span><span class="sxs-lookup"><span data-stu-id="5974c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5974c-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5974c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5974c-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5974c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5974c-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5974c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5974c-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5974c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5974c-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5974c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5974c-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5974c-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5974c-134">IDL</span><span class="sxs-lookup"><span data-stu-id="5974c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5974c-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5974c-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5974c-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5974c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5974c-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5974c-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5974c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5974c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5974c-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="5974c-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





