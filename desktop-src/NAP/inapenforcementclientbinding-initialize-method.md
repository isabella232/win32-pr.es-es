---
title: Método Initialize INapEnforcementClientBinding (NapEnforcementClient. h)
description: Inicia automáticamente el servicio NapAgent.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489892"
---
# <a name="inapenforcementclientbindinginitialize-method"></a><span data-ttu-id="fae91-106">INapEnforcementClientBinding:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="fae91-106">INapEnforcementClientBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="fae91-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fae91-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fae91-108">El método **INapEnforcementClientBinding:: Initialize** inicia el servicio NapAgent automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fae91-108">The **INapEnforcementClientBinding::Initialize** method starts up the NapAgent service automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae91-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fae91-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="fae91-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fae91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae91-111">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="fae91-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fae91-112">Un [**EnforcementEntityId**](nap-datatypes.md) que identifica el cliente de cumplimiento y su versión.</span><span class="sxs-lookup"><span data-stu-id="fae91-112">An [**EnforcementEntityId**](nap-datatypes.md) that identifies the enforcement client and its version.</span></span>

</dd> <dt>

<span data-ttu-id="fae91-113">*devolución de llamada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fae91-113">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fae91-114">Puntero COM a una interfaz [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) que usa NapAgent para devolver la llamada a los clientes de cumplimiento con Notify/Process.</span><span class="sxs-lookup"><span data-stu-id="fae91-114">A COM pointer to an [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interface used by the NapAgent to callback the enforcement clients with notify/process.</span></span> <span data-ttu-id="fae91-115">NapAgent contiene una referencia al objeto asociado a esta interfaz hasta que se llama a [**INapEnforcementClientBinding:: UnInitialize**](inapenforcementclientbinding-uninitialize-method.md) .</span><span class="sxs-lookup"><span data-stu-id="fae91-115">The NapAgent holds a reference to the object associated with this interface until [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae91-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fae91-116">Return value</span></span>

<span data-ttu-id="fae91-117">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="fae91-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fae91-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fae91-118">Return code</span></span>                                                                                                         | <span data-ttu-id="fae91-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="fae91-119">Description</span></span>                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fae91-120"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="fae91-120"><dt>**S\_OK** </dt></span></span> </dl>                               | <span data-ttu-id="fae91-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fae91-121">The operation is successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="fae91-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fae91-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>                     | <span data-ttu-id="fae91-123">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="fae91-123">Permissions error, access denied.</span></span><br/>                                             |
| <dl> <span data-ttu-id="fae91-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fae91-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>                      | <span data-ttu-id="fae91-125">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="fae91-125">System resource limit, could not perform the operation.</span></span><br/>                       |
| <dl> <span data-ttu-id="fae91-126"><dt>**HRESULT (ERROR \_ ya \_ inicializado)**</dt></span><span class="sxs-lookup"><span data-stu-id="fae91-126"><dt>**HRESULT(ERROR\_ALREADY\_INITIALIZED)**</dt></span></span> </dl> | <span data-ttu-id="fae91-127">Si el aplicador se ha inicializado previamente, se devuelve este código de error.</span><span class="sxs-lookup"><span data-stu-id="fae91-127">If the enforcer has initialized previously, then this error code is returned.</span></span><br/> |
| <dl> <span data-ttu-id="fae91-128"><dt>**NAP \_ E \_ no \_ registrado**</dt></span><span class="sxs-lookup"><span data-stu-id="fae91-128"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>              | <span data-ttu-id="fae91-129">Si el aplicador no se ha registrado anteriormente, se devuelve este código de error.</span><span class="sxs-lookup"><span data-stu-id="fae91-129">If the enforcer has not registered earlier, this error code is returned.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="fae91-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fae91-130">Remarks</span></span>

<span data-ttu-id="fae91-131">El cliente de cumplimiento debe llamar al método **INapEnforcementClientBinding:: Initialize** antes de llamar a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="fae91-131">The enforcement client must call the **INapEnforcementClientBinding::Initialize** method before calling any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="fae91-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fae91-132">Requirements</span></span>



| <span data-ttu-id="fae91-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae91-133">Requirement</span></span> | <span data-ttu-id="fae91-134">Value</span><span class="sxs-lookup"><span data-stu-id="fae91-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae91-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fae91-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fae91-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fae91-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fae91-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fae91-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fae91-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fae91-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fae91-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fae91-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="fae91-140"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fae91-140"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fae91-141">IDL</span><span class="sxs-lookup"><span data-stu-id="fae91-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fae91-142"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fae91-142"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fae91-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fae91-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fae91-144"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fae91-144"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fae91-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="fae91-145">See also</span></span>

<dl> <span data-ttu-id="fae91-146"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="fae91-146"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="fae91-147">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="fae91-147">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="fae91-148">**INapEnforcementClientBinding:: UnInitialize**</span><span class="sxs-lookup"><span data-stu-id="fae91-148">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





