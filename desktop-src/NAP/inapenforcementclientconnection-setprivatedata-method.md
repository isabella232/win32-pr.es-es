---
title: Método INapEnforcementClientConnection SetPrivateData (NapEnforcementClient. h)
description: Lo usa NapAgent para establecer datos privados.
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- Método SetPrivateData NAP
- Método SetPrivateData NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079164"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a><span data-ttu-id="48a72-106">INapEnforcementClientConnection:: SetPrivateData (método)</span><span class="sxs-lookup"><span data-stu-id="48a72-106">INapEnforcementClientConnection::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="48a72-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="48a72-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="48a72-108">NapAgent usa el método **INapEnforcementClientConnection:: SetPrivateData** para establecer datos privados.</span><span class="sxs-lookup"><span data-stu-id="48a72-108">The **INapEnforcementClientConnection::SetPrivateData** method is used by the NapAgent to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a72-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48a72-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="48a72-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48a72-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a72-111">*privateData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48a72-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48a72-112">Un puntero a un BLOB de datos [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que solo el NapAgent puede interpretar.</span><span class="sxs-lookup"><span data-stu-id="48a72-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a72-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48a72-113">Return value</span></span>

<span data-ttu-id="48a72-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="48a72-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="48a72-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="48a72-115">Return code</span></span>                                                                                     | <span data-ttu-id="48a72-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="48a72-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="48a72-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="48a72-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="48a72-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="48a72-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="48a72-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="48a72-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="48a72-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="48a72-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="48a72-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="48a72-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="48a72-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="48a72-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="48a72-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48a72-123">Requirements</span></span>



| <span data-ttu-id="48a72-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a72-124">Requirement</span></span> | <span data-ttu-id="48a72-125">Value</span><span class="sxs-lookup"><span data-stu-id="48a72-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a72-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48a72-126">Minimum supported client</span></span><br/> | <span data-ttu-id="48a72-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="48a72-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="48a72-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48a72-128">Minimum supported server</span></span><br/> | <span data-ttu-id="48a72-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="48a72-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="48a72-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48a72-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a72-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="48a72-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="48a72-132">IDL</span><span class="sxs-lookup"><span data-stu-id="48a72-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48a72-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48a72-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="48a72-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48a72-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48a72-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a72-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="48a72-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="48a72-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a72-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="48a72-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





