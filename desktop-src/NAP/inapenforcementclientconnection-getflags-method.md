---
title: Método GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
description: Se usa para diferenciar las respuestas por primera vez de las respuestas debido a SoHRequests almacenados en memoria caché por los imforcedores. | Método GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- Método GetFlags NAP
- Método GetFlags NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método GetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a35e183b5d4f606d21f4afce8cca68135732a35c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105653153"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a><span data-ttu-id="214f6-107">INapEnforcementClientConnection:: GetFlags (método)</span><span class="sxs-lookup"><span data-stu-id="214f6-107">INapEnforcementClientConnection::GetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="214f6-108">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="214f6-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="214f6-109">El método **INapEnforcementClientConnection:: GetFlags** se usa para diferenciar las respuestas por primera vez de las respuestas debidas a SoHRequests almacenados en memoria caché por los imforcedores.</span><span class="sxs-lookup"><span data-stu-id="214f6-109">The **INapEnforcementClientConnection::GetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="214f6-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="214f6-110">Syntax</span></span>


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a><span data-ttu-id="214f6-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="214f6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214f6-112">*marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="214f6-112">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214f6-113">Puntero a una marca que determina si [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) se debe a un **SoHRequest** almacenado en memoria caché.</span><span class="sxs-lookup"><span data-stu-id="214f6-113">A pointer to a flag that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="214f6-114">Si *Flags* tiene un valor de [**freshSoHRequest**](nap-type-constants.md), es una solicitud nueva; en caso contrario, se trata de una solicitud almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="214f6-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="214f6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="214f6-115">Return value</span></span>

<span data-ttu-id="214f6-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="214f6-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="214f6-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="214f6-117">Return code</span></span>                                                                                     | <span data-ttu-id="214f6-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="214f6-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="214f6-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="214f6-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="214f6-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="214f6-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="214f6-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="214f6-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="214f6-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="214f6-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="214f6-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="214f6-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="214f6-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="214f6-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="214f6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="214f6-125">Requirements</span></span>



| <span data-ttu-id="214f6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="214f6-126">Requirement</span></span> | <span data-ttu-id="214f6-127">Value</span><span class="sxs-lookup"><span data-stu-id="214f6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="214f6-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="214f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="214f6-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="214f6-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="214f6-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="214f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="214f6-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="214f6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="214f6-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="214f6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="214f6-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="214f6-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="214f6-134">IDL</span><span class="sxs-lookup"><span data-stu-id="214f6-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="214f6-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="214f6-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="214f6-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="214f6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="214f6-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="214f6-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="214f6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="214f6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214f6-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="214f6-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





