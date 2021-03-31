---
title: Método INapEnforcementClientConnection GetPrivateData (NapEnforcementClient. h)
description: Lo usa NapAgent para obtener datos privados.
ms.assetid: d38ef523-b645-401f-b3a9-1315ef39931a
keywords:
- Método GetPrivateData NAP
- Método GetPrivateData NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método GetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6618ff7b25ad57cbb943107e80f299d9b6a68bea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905123"
---
# <a name="inapenforcementclientconnectiongetprivatedata-method"></a><span data-ttu-id="1ab00-106">INapEnforcementClientConnection:: GetPrivateData (método)</span><span class="sxs-lookup"><span data-stu-id="1ab00-106">INapEnforcementClientConnection::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="1ab00-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1ab00-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1ab00-108">NapAgent usa el método **INapEnforcementClientConnection:: GetPrivateData** para obtener datos privados.</span><span class="sxs-lookup"><span data-stu-id="1ab00-108">The **INapEnforcementClientConnection::GetPrivateData** method is used by the NapAgent to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab00-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ab00-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="1ab00-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ab00-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ab00-111">*privateData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1ab00-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ab00-112">Un puntero a un puntero a un BLOB de datos opacos [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que solo el NapAgent puede interpretar.</span><span class="sxs-lookup"><span data-stu-id="1ab00-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ab00-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ab00-113">Return value</span></span>

<span data-ttu-id="1ab00-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="1ab00-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1ab00-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1ab00-115">Return code</span></span>                                                                                     | <span data-ttu-id="1ab00-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ab00-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ab00-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="1ab00-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1ab00-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="1ab00-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1ab00-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1ab00-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1ab00-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="1ab00-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1ab00-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1ab00-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1ab00-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="1ab00-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1ab00-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ab00-123">Requirements</span></span>



| <span data-ttu-id="1ab00-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ab00-124">Requirement</span></span> | <span data-ttu-id="1ab00-125">Value</span><span class="sxs-lookup"><span data-stu-id="1ab00-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab00-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ab00-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab00-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ab00-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1ab00-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ab00-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab00-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ab00-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1ab00-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ab00-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ab00-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ab00-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ab00-132">IDL</span><span class="sxs-lookup"><span data-stu-id="1ab00-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1ab00-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1ab00-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="1ab00-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ab00-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ab00-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ab00-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1ab00-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ab00-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab00-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="1ab00-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





