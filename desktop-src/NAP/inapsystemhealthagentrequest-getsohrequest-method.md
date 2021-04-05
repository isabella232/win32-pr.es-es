---
title: Método INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent. h)
description: Lo pueden usar Sha Get SOH previamente almacenados en caché por NapAgent.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079698"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a><span data-ttu-id="a30f2-106">INapSystemHealthAgentRequest:: GetSoHRequest (método)</span><span class="sxs-lookup"><span data-stu-id="a30f2-106">INapSystemHealthAgentRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="a30f2-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a30f2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a30f2-108">El método **INapSystemHealthAgentRequest:: GetSoHRequest** puede usarse por los Shas Get SOH previamente almacenados en caché por NapAgent.</span><span class="sxs-lookup"><span data-stu-id="a30f2-108">The **INapSystemHealthAgentRequest::GetSoHRequest** method can be used by SHAs get SoHs previously cached by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30f2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a30f2-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="a30f2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a30f2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a30f2-111">*sohRequest* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a30f2-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a30f2-112">Un puntero a un puntero a un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="a30f2-112">A pointer to a pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a30f2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a30f2-113">Return value</span></span>

<span data-ttu-id="a30f2-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="a30f2-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a30f2-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a30f2-115">Return code</span></span>                                                                                            | <span data-ttu-id="a30f2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a30f2-116">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a30f2-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="a30f2-117"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="a30f2-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a30f2-118">Operation succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="a30f2-119"><dt>**\_no se \_ ha \_ almacenado en caché el \_ SOH de NAP E**</dt></span><span class="sxs-lookup"><span data-stu-id="a30f2-119"><dt>**NAP\_E\_NO\_CACHED\_SOH**</dt></span></span> </dl> | <span data-ttu-id="a30f2-120">No se encuentra el SoH; NapAgent no tiene una copia almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="a30f2-120">The SoH is not found; NapAgent does not have a cached copy.</span></span><br/> |
| <dl> <span data-ttu-id="a30f2-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a30f2-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="a30f2-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="a30f2-122">Permissions error, access denied.</span></span><br/>                           |
| <dl> <span data-ttu-id="a30f2-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a30f2-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="a30f2-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a30f2-124">System resource limit, could not perform the operation.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="a30f2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a30f2-125">Requirements</span></span>



| <span data-ttu-id="a30f2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a30f2-126">Requirement</span></span> | <span data-ttu-id="a30f2-127">Value</span><span class="sxs-lookup"><span data-stu-id="a30f2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a30f2-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a30f2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a30f2-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a30f2-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a30f2-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a30f2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a30f2-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a30f2-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a30f2-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a30f2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a30f2-133"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="a30f2-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="a30f2-134">IDL</span><span class="sxs-lookup"><span data-stu-id="a30f2-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a30f2-135"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a30f2-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="a30f2-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a30f2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a30f2-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a30f2-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="a30f2-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a30f2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30f2-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="a30f2-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





