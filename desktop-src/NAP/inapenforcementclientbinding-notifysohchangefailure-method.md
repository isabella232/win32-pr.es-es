---
title: Método INapEnforcementClientBinding NotifySoHChangeFailure (NapEnforcementClient. h)
description: Lo usa el cliente de cumplimiento para informar a NapAgent de que no pudo procesar una NotifySoHChange INapEnforcementClientCallback anterior.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Método NotifySoHChangeFailure NAP
- Método NotifySoHChangeFailure NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método NotifySoHChangeFailure
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493156"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a><span data-ttu-id="edbbc-106">INapEnforcementClientBinding:: NotifySoHChangeFailure (método)</span><span class="sxs-lookup"><span data-stu-id="edbbc-106">INapEnforcementClientBinding::NotifySoHChangeFailure method</span></span>

> [!Note]  
> <span data-ttu-id="edbbc-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="edbbc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="edbbc-108">El cliente de cumplimiento usa el método **INapEnforcementClientBinding:: NotifySoHChangeFailure** para informar a NapAgent de que no pudo procesar una [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)anterior.</span><span class="sxs-lookup"><span data-stu-id="edbbc-108">The **INapEnforcementClientBinding::NotifySoHChangeFailure** method is used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="edbbc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edbbc-109">Syntax</span></span>


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a><span data-ttu-id="edbbc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edbbc-110">Parameters</span></span>

<span data-ttu-id="edbbc-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="edbbc-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="edbbc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edbbc-112">Return value</span></span>

<span data-ttu-id="edbbc-113">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="edbbc-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="edbbc-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="edbbc-114">Return code</span></span>                                                                                             | <span data-ttu-id="edbbc-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="edbbc-115">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="edbbc-116"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="edbbc-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="edbbc-117">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="edbbc-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="edbbc-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="edbbc-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="edbbc-119">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="edbbc-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="edbbc-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="edbbc-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="edbbc-121">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="edbbc-121">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="edbbc-122"><dt>**NAP \_ E \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="edbbc-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="edbbc-123">El exigidor no se ha inicializado previamente.</span><span class="sxs-lookup"><span data-stu-id="edbbc-123">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="edbbc-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edbbc-124">Remarks</span></span>

<span data-ttu-id="edbbc-125">Como resultado de esta llamada al método, NapAgent reintenta aplicar el cambio de SoH más adelante llamando a [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) de nuevo.</span><span class="sxs-lookup"><span data-stu-id="edbbc-125">As a result of this method call the NapAgent retries applying the SoH change at a later time by calling [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) again.</span></span> <span data-ttu-id="edbbc-126">Una vez que el cliente de cumplimiento ha llamado a [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), debe aplicar el cambio, es decir, el NapAgent no controla ningún error después de este punto.</span><span class="sxs-lookup"><span data-stu-id="edbbc-126">Once the enforcement client has called [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), it then must apply the change, i.e. no failures are handled by the NapAgent after this point.</span></span>

<span data-ttu-id="edbbc-127">El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="edbbc-127">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="edbbc-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edbbc-128">Requirements</span></span>



| <span data-ttu-id="edbbc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="edbbc-129">Requirement</span></span> | <span data-ttu-id="edbbc-130">Value</span><span class="sxs-lookup"><span data-stu-id="edbbc-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbbc-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edbbc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="edbbc-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="edbbc-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="edbbc-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edbbc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="edbbc-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="edbbc-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="edbbc-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edbbc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="edbbc-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="edbbc-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="edbbc-137">IDL</span><span class="sxs-lookup"><span data-stu-id="edbbc-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="edbbc-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="edbbc-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="edbbc-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edbbc-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edbbc-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edbbc-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="edbbc-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="edbbc-141">See also</span></span>

<dl> <span data-ttu-id="edbbc-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="edbbc-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="edbbc-143">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="edbbc-143">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="edbbc-144">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="edbbc-144">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[<span data-ttu-id="edbbc-145">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="edbbc-145">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





