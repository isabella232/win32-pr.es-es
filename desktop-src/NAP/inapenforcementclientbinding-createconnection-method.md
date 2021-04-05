---
title: Método INapEnforcementClientBinding CreateConnection (NapEnforcementClient. h)
description: Lo utilizan los exigentes para crear objetos de conexión.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- Método CreateConnection NAP
- Método CreateConnection NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método CreateConnection
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079168"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a><span data-ttu-id="78320-106">INapEnforcementClientBinding:: CreateConnection (método)</span><span class="sxs-lookup"><span data-stu-id="78320-106">INapEnforcementClientBinding::CreateConnection method</span></span>

> [!Note]  
> <span data-ttu-id="78320-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="78320-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="78320-108">El Factory Method **INapEnforcementClientBinding:: CreateConnection** lo usan los enforceers para crear objetos de conexión.</span><span class="sxs-lookup"><span data-stu-id="78320-108">The **INapEnforcementClientBinding::CreateConnection** factory method is used by enforcers to create connection objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="78320-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78320-109">Syntax</span></span>


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a><span data-ttu-id="78320-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78320-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78320-111">*conexión* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="78320-111">*connection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78320-112">Puntero COM a una nueva interfaz [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) devuelta por el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="78320-112">A COM pointer to a new [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface returned by the NAP system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78320-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78320-113">Return value</span></span>

<span data-ttu-id="78320-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="78320-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="78320-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="78320-115">Return code</span></span>                                                                                     | <span data-ttu-id="78320-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="78320-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="78320-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="78320-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="78320-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="78320-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="78320-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="78320-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="78320-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="78320-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="78320-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="78320-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="78320-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="78320-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78320-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78320-123">Remarks</span></span>

<span data-ttu-id="78320-124">El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="78320-124">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="78320-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78320-125">Requirements</span></span>



| <span data-ttu-id="78320-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="78320-126">Requirement</span></span> | <span data-ttu-id="78320-127">Value</span><span class="sxs-lookup"><span data-stu-id="78320-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78320-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78320-128">Minimum supported client</span></span><br/> | <span data-ttu-id="78320-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="78320-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="78320-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78320-130">Minimum supported server</span></span><br/> | <span data-ttu-id="78320-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="78320-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="78320-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78320-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="78320-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="78320-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="78320-134">IDL</span><span class="sxs-lookup"><span data-stu-id="78320-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78320-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78320-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="78320-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78320-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78320-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78320-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="78320-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="78320-138">See also</span></span>

<dl> <span data-ttu-id="78320-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="78320-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="78320-140">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="78320-140">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="78320-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="78320-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





