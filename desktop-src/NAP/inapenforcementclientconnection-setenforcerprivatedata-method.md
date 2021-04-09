---
title: Método INapEnforcementClientConnection SetEnforcerPrivateData (NapEnforcementClient. h)
description: Lo utiliza el aplicador para establecer datos privados.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Método SetEnforcerPrivateData NAP
- Método SetEnforcerPrivateData NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079166"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a><span data-ttu-id="faaff-106">INapEnforcementClientConnection:: SetEnforcerPrivateData (método)</span><span class="sxs-lookup"><span data-stu-id="faaff-106">INapEnforcementClientConnection::SetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="faaff-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="faaff-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="faaff-108">El forzado usa el método **INapEnforcementClientConnection:: SetEnforcerPrivateData** para establecer datos privados.</span><span class="sxs-lookup"><span data-stu-id="faaff-108">The **INapEnforcementClientConnection::SetEnforcerPrivateData** method is used by the enforcer to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="faaff-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="faaff-109">Syntax</span></span>


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="faaff-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="faaff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faaff-111">*privateData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="faaff-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faaff-112">Un puntero a un BLOB de datos opacos de [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que solo puede interpretar el aplicador.</span><span class="sxs-lookup"><span data-stu-id="faaff-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faaff-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="faaff-113">Return value</span></span>

<span data-ttu-id="faaff-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="faaff-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="faaff-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="faaff-115">Return code</span></span>                                                                                     | <span data-ttu-id="faaff-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="faaff-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="faaff-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="faaff-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="faaff-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="faaff-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="faaff-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="faaff-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="faaff-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="faaff-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="faaff-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="faaff-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="faaff-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="faaff-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="faaff-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faaff-123">Requirements</span></span>



| <span data-ttu-id="faaff-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="faaff-124">Requirement</span></span> | <span data-ttu-id="faaff-125">Value</span><span class="sxs-lookup"><span data-stu-id="faaff-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faaff-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faaff-126">Minimum supported client</span></span><br/> | <span data-ttu-id="faaff-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="faaff-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="faaff-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faaff-128">Minimum supported server</span></span><br/> | <span data-ttu-id="faaff-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="faaff-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="faaff-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="faaff-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="faaff-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="faaff-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="faaff-132">IDL</span><span class="sxs-lookup"><span data-stu-id="faaff-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="faaff-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="faaff-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="faaff-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="faaff-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faaff-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faaff-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="faaff-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="faaff-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faaff-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="faaff-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





