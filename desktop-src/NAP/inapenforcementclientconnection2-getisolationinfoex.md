---
title: Método INapEnforcementClientConnection2 GetIsolationInfoEx (NapEnforcementClient. h)
description: Se usa para obtener información de aislamiento sobre el cliente.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Método GetIsolationInfoEx NAP
- Método GetIsolationInfoEx NAP, interfaz INapEnforcementClientConnection2
- Interfaz INapEnforcementClientConnection2 NAP, método GetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493240"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a><span data-ttu-id="fcd35-106">INapEnforcementClientConnection2:: GetIsolationInfoEx (método)</span><span class="sxs-lookup"><span data-stu-id="fcd35-106">INapEnforcementClientConnection2::GetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="fcd35-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fcd35-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fcd35-108">El método **INapEnforcementClientConnection2:: GetIsolationInfoEx** se usa para obtener información de aislamiento sobre el cliente.</span><span class="sxs-lookup"><span data-stu-id="fcd35-108">The **INapEnforcementClientConnection2::GetIsolationInfoEx** method is used to get isolation information about the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd35-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcd35-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a><span data-ttu-id="fcd35-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcd35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd35-111">*isolationInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fcd35-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcd35-112">Un puntero a un puntero a una estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contiene la información de conectividad y de Estado extendido del cliente.</span><span class="sxs-lookup"><span data-stu-id="fcd35-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity and extended state information of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd35-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcd35-113">Return value</span></span>

<span data-ttu-id="fcd35-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="fcd35-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fcd35-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fcd35-115">Return code</span></span>                                                                                     | <span data-ttu-id="fcd35-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcd35-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fcd35-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="fcd35-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="fcd35-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="fcd35-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fcd35-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fcd35-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="fcd35-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="fcd35-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fcd35-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fcd35-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="fcd35-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="fcd35-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fcd35-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcd35-123">Remarks</span></span>

<span data-ttu-id="fcd35-124">NapAgent establece esta información después de procesar una [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) y el exigidor no debe establecerla.</span><span class="sxs-lookup"><span data-stu-id="fcd35-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

<span data-ttu-id="fcd35-125">SHA debe liberar la estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) llamando a [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="fcd35-125">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd35-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcd35-126">Requirements</span></span>



| <span data-ttu-id="fcd35-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcd35-127">Requirement</span></span> | <span data-ttu-id="fcd35-128">Value</span><span class="sxs-lookup"><span data-stu-id="fcd35-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd35-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcd35-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd35-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fcd35-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fcd35-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fcd35-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd35-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fcd35-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fcd35-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcd35-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcd35-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcd35-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fcd35-135">IDL</span><span class="sxs-lookup"><span data-stu-id="fcd35-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fcd35-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fcd35-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fcd35-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fcd35-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcd35-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcd35-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fcd35-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcd35-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd35-140">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="fcd35-140">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





