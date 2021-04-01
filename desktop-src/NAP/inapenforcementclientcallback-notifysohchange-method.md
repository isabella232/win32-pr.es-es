---
title: Método INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient. h)
description: NapAgent lo usa para informar al cliente de cumplimiento de los cambios de SoH.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Método NotifySoHChange NAP
- Método NotifySoHChange NAP, interfaz INapEnforcementClientCallback
- Interfaz INapEnforcementClientCallback NAP, método NotifySoHChange
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151203"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a><span data-ttu-id="0150c-106">INapEnforcementClientCallback:: NotifySoHChange (método)</span><span class="sxs-lookup"><span data-stu-id="0150c-106">INapEnforcementClientCallback::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="0150c-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0150c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0150c-108">El NapAgent usa el método de devolución de llamada **INapEnforcementClientCallback:: NotifySoHChange** para informar al cliente de cumplimiento de los cambios de SOH.</span><span class="sxs-lookup"><span data-stu-id="0150c-108">The **INapEnforcementClientCallback::NotifySoHChange** callback method is used by the NapAgent to inform the enforcement client of SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0150c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0150c-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="0150c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0150c-110">Parameters</span></span>

<span data-ttu-id="0150c-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0150c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0150c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0150c-112">Return value</span></span>

<span data-ttu-id="0150c-113">Este método de devolución de llamada debe devolver uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="0150c-113">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="0150c-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0150c-114">Return code</span></span>                                                                                                | <span data-ttu-id="0150c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0150c-115">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0150c-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0150c-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="0150c-117">Devuelve este valor si la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0150c-117">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="0150c-118"><dt>**el \_ servidor RPC S \_ \_ no está disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="0150c-118"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="0150c-119">Al devolver este valor, el aplicador se quita de la lista Bound-SHA y la entrada de caché de NapAgent correspondiente que se va a vaciar.</span><span class="sxs-lookup"><span data-stu-id="0150c-119">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="0150c-120">Después, el SHA con error puede volver a inicializarse con el NapAgent.</span><span class="sxs-lookup"><span data-stu-id="0150c-120">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0150c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0150c-121">Remarks</span></span>

<span data-ttu-id="0150c-122">La finalización de la corrección del sistema es un evento de cambio de mantenimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="0150c-122">The completion of system fix-up is a system health change event.</span></span> <span data-ttu-id="0150c-123">Esto significa que debe llamar a **NotifySoHChange** cuando una notificación [**INapSystemHealthAgentCallback:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indica que el cliente es fijo.</span><span class="sxs-lookup"><span data-stu-id="0150c-123">That means you must call **NotifySoHChange** when a [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) notification indicates that the client is fixed.</span></span> <span data-ttu-id="0150c-124">Cuando se corrige un cliente, el miembro **State** de la estructura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) devuelto por **GetFixupInfo** tiene un valor de **fixupStateSuccess**.</span><span class="sxs-lookup"><span data-stu-id="0150c-124">When a client is fixed, the **state** member of the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure returned by **GetFixupInfo** has a value of **fixupStateSuccess**.</span></span>

<span data-ttu-id="0150c-125">Después de ser llamado por el NapAgent a través de esta devolución de llamada, el agente de cumplimiento debe llamar a [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) para recuperar la nueva solicitud.</span><span class="sxs-lookup"><span data-stu-id="0150c-125">After being called by the NapAgent via this callback, the enforcement agent must then call [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) to retrieve the new request.</span></span> <span data-ttu-id="0150c-126">Esta llamada se puede realizar en el mismo subproceso que **INapEnforcementClientCallback:: NotifySoHChange**.</span><span class="sxs-lookup"><span data-stu-id="0150c-126">This call can be made on the same thread as **INapEnforcementClientCallback::NotifySoHChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0150c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0150c-127">Requirements</span></span>



| <span data-ttu-id="0150c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0150c-128">Requirement</span></span> | <span data-ttu-id="0150c-129">Value</span><span class="sxs-lookup"><span data-stu-id="0150c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0150c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0150c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0150c-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0150c-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0150c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0150c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0150c-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0150c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0150c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0150c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0150c-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0150c-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0150c-136">IDL</span><span class="sxs-lookup"><span data-stu-id="0150c-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0150c-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0150c-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0150c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0150c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0150c-139">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="0150c-139">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





