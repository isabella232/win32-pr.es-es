---
title: Método INapClientManagement2 GetSystemIsolationInfoEx (NapManagement. h)
description: Recupera información sobre el estado de aislamiento y el estado de aislamiento extendido de NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Método GetSystemIsolationInfoEx NAP
- Método GetSystemIsolationInfoEx NAP, interfaz INapClientManagement2
- Interfaz INapClientManagement2 NAP, método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079170"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a><span data-ttu-id="ddc30-106">INapClientManagement2:: GetSystemIsolationInfoEx (método)</span><span class="sxs-lookup"><span data-stu-id="ddc30-106">INapClientManagement2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="ddc30-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="ddc30-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ddc30-108">El método **GetSystemIsolationInfoEx** recupera información sobre el estado de aislamiento y el estado de aislamiento extendido de NapClient.</span><span class="sxs-lookup"><span data-stu-id="ddc30-108">The **GetSystemIsolationInfoEx** method retrieves information about the isolation state and extended isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc30-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddc30-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="ddc30-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddc30-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddc30-111">*isolationInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ddc30-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc30-112">Un puntero a un puntero a una estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contiene información de estado de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="ddc30-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="ddc30-113">*unknownConnections* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ddc30-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc30-114">Un puntero a un valor BOOLEANO que es **true** si alguna de las conexiones tiene un estado desconocido y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ddc30-114">A pointer to a BOOL that is **TRUE** if any of the connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddc30-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddc30-115">Return value</span></span>

<span data-ttu-id="ddc30-116">El método devuelve un código de estado HRESULT, incluido pero no limitado a uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="ddc30-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="ddc30-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ddc30-117">Return code</span></span>                                                                                         | <span data-ttu-id="ddc30-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddc30-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ddc30-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc30-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="ddc30-120">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="ddc30-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ddc30-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc30-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="ddc30-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="ddc30-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ddc30-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc30-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="ddc30-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="ddc30-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ddc30-125"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc30-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ddc30-126">NapAgent no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="ddc30-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="ddc30-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddc30-127">Remarks</span></span>

<span data-ttu-id="ddc30-128">La información de aislamiento que se recupera no refleja Estados desconocidos.</span><span class="sxs-lookup"><span data-stu-id="ddc30-128">The isolation information that is retrieved does not reflect unknown states.</span></span>

<span data-ttu-id="ddc30-129">SHA debe liberar la estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) llamando a [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="ddc30-129">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc30-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddc30-130">Requirements</span></span>



| <span data-ttu-id="ddc30-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddc30-131">Requirement</span></span> | <span data-ttu-id="ddc30-132">Value</span><span class="sxs-lookup"><span data-stu-id="ddc30-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc30-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddc30-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc30-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ddc30-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ddc30-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddc30-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc30-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ddc30-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ddc30-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddc30-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddc30-138"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddc30-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="ddc30-139">IDL</span><span class="sxs-lookup"><span data-stu-id="ddc30-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ddc30-140"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ddc30-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="ddc30-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddc30-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddc30-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddc30-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="ddc30-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddc30-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc30-144">**INapClientManagement2**</span><span class="sxs-lookup"><span data-stu-id="ddc30-144">**INapClientManagement2**</span></span>](inapclientmanagement2.md)
</dt> </dl>

 

 





