---
title: Método INapEnforcementClientConnection SetIsolationInfo (NapEnforcementClient. h)
description: Lo usa NapAgent para establecer la información de aislamiento del cliente.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- Método SetIsolationInfo NAP
- Método SetIsolationInfo NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1cfd7ad227fec6942e0660769f52b3d4f12201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801844"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a><span data-ttu-id="a8546-106">INapEnforcementClientConnection:: SetIsolationInfo (método)</span><span class="sxs-lookup"><span data-stu-id="a8546-106">INapEnforcementClientConnection::SetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="a8546-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a8546-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a8546-108">NapAgent usa el método **INapEnforcementClientConnection:: SetIsolationInfo** para establecer la información de aislamiento del cliente.</span><span class="sxs-lookup"><span data-stu-id="a8546-108">The **INapEnforcementClientConnection::SetIsolationInfo** method is used by the NapAgent to set the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8546-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8546-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a8546-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8546-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8546-111">*isolationInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a8546-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8546-112">Puntero a una estructura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contiene el estado de Conectividad del cliente.</span><span class="sxs-lookup"><span data-stu-id="a8546-112">A pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8546-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8546-113">Return value</span></span>

<span data-ttu-id="a8546-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="a8546-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a8546-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a8546-115">Return code</span></span>                                                                                     | <span data-ttu-id="a8546-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8546-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a8546-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="a8546-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a8546-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8546-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a8546-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a8546-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a8546-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="a8546-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a8546-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a8546-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a8546-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a8546-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8546-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8546-123">Remarks</span></span>

<span data-ttu-id="a8546-124">NapAgent establece esta información después de procesar una SoHResponse y el exigidor no debe establecerla.</span><span class="sxs-lookup"><span data-stu-id="a8546-124">This information is set by NapAgent after processing an SoHResponse and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8546-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8546-125">Requirements</span></span>



| <span data-ttu-id="a8546-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8546-126">Requirement</span></span> | <span data-ttu-id="a8546-127">Value</span><span class="sxs-lookup"><span data-stu-id="a8546-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8546-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8546-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a8546-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8546-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a8546-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8546-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a8546-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8546-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a8546-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8546-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8546-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8546-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8546-134">IDL</span><span class="sxs-lookup"><span data-stu-id="a8546-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8546-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8546-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8546-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8546-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8546-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8546-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a8546-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8546-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8546-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a8546-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





