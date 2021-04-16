---
title: Método INapEnforcementClientConnection2 SetIsolationInfoEx (NapEnforcementClient. h)
description: Lo usa NapAgent para establecer la información de aislamiento para el cliente.
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- Método SetIsolationInfoEx NAP
- Método SetIsolationInfoEx NAP, interfaz INapEnforcementClientConnection2
- Interfaz INapEnforcementClientConnection2 NAP, método SetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711b4bfd27c3bd92d48a78f4767f5ed452b2d4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677019"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a><span data-ttu-id="1870e-106">INapEnforcementClientConnection2:: SetIsolationInfoEx (método)</span><span class="sxs-lookup"><span data-stu-id="1870e-106">INapEnforcementClientConnection2::SetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="1870e-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1870e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1870e-108">NapAgent usa el método **INapEnforcementClientConnection2:: SetIsolationInfoEx** para establecer la información de aislamiento para el cliente.</span><span class="sxs-lookup"><span data-stu-id="1870e-108">The **INapEnforcementClientConnection2::SetIsolationInfoEx** method is used by the NapAgent to set the isolation information for the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="1870e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1870e-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfoEx(
  [in] const IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1870e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1870e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1870e-111">*isolationInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1870e-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1870e-112">Puntero a una estructura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contiene el estado de Conectividad del cliente.</span><span class="sxs-lookup"><span data-stu-id="1870e-112">A pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1870e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1870e-113">Return value</span></span>

<span data-ttu-id="1870e-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="1870e-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1870e-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1870e-115">Return code</span></span>                                                                                     | <span data-ttu-id="1870e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1870e-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1870e-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="1870e-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1870e-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="1870e-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1870e-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1870e-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1870e-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="1870e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1870e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1870e-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1870e-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="1870e-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1870e-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1870e-123">Remarks</span></span>

<span data-ttu-id="1870e-124">NapAgent establece esta información después de procesar una [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) y el exigidor no debe establecerla.</span><span class="sxs-lookup"><span data-stu-id="1870e-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1870e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1870e-125">Requirements</span></span>



| <span data-ttu-id="1870e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1870e-126">Requirement</span></span> | <span data-ttu-id="1870e-127">Value</span><span class="sxs-lookup"><span data-stu-id="1870e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1870e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1870e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1870e-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1870e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1870e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1870e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1870e-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1870e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1870e-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1870e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1870e-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1870e-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1870e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="1870e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1870e-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1870e-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="1870e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1870e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1870e-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1870e-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1870e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1870e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1870e-139">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="1870e-139">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





