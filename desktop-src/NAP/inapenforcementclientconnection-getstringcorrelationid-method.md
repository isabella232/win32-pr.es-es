---
title: Método INapEnforcementClientConnection GetStringCorrelationId (NapEnforcementClient. h)
description: Obtiene la versión de cadena del identificador utilizado para poner en correlación las solicitudes y las respuestas.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Método GetStringCorrelationId NAP
- Método GetStringCorrelationId NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533964"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a><span data-ttu-id="a3a8a-106">INapEnforcementClientConnection:: GetStringCorrelationId (método)</span><span class="sxs-lookup"><span data-stu-id="a3a8a-106">INapEnforcementClientConnection::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="a3a8a-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a3a8a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a3a8a-108">El método **INapEnforcementClientConnection:: GetStringCorrelationId** obtiene la versión de cadena del identificador utilizado para poner en correlación las solicitudes y las respuestas.</span><span class="sxs-lookup"><span data-stu-id="a3a8a-108">The **INapEnforcementClientConnection::GetStringCorrelationId** method gets the string version of the ID used to correlate requests and responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a8a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3a8a-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="a3a8a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3a8a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3a8a-111">*CorrelationId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a3a8a-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3a8a-112">Puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión de cadena del [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)de la conexión.</span><span class="sxs-lookup"><span data-stu-id="a3a8a-112">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the string version of the connection's [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3a8a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3a8a-113">Return value</span></span>

<span data-ttu-id="a3a8a-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="a3a8a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a3a8a-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a3a8a-115">Return code</span></span>                                                                                     | <span data-ttu-id="a3a8a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3a8a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3a8a-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a3a8a-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a3a8a-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a3a8a-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a3a8a-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="a3a8a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a3a8a-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a3a8a-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a3a8a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a3a8a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3a8a-123">Requirements</span></span>



| <span data-ttu-id="a3a8a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3a8a-124">Requirement</span></span> | <span data-ttu-id="a3a8a-125">Value</span><span class="sxs-lookup"><span data-stu-id="a3a8a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a8a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3a8a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a8a-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a3a8a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a3a8a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3a8a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a8a-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3a8a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a3a8a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3a8a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3a8a-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8a-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3a8a-132">IDL</span><span class="sxs-lookup"><span data-stu-id="a3a8a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3a8a-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8a-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a3a8a-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3a8a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3a8a-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8a-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a3a8a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3a8a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3a8a-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a3a8a-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





