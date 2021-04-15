---
title: Método INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent. h)
description: Se llama a si se ha consultado un SoHRequest desde SHA, pero la respuesta nunca llegó.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Método NotifyOrphanedSoHRequest NAP
- Método NotifyOrphanedSoHRequest NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método NotifyOrphanedSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422579"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a><span data-ttu-id="50326-106">INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest (método)</span><span class="sxs-lookup"><span data-stu-id="50326-106">INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="50326-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="50326-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="50326-108">Se llama al método **INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest** si se ha consultado un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) desde Sha, pero la respuesta nunca llegó.</span><span class="sxs-lookup"><span data-stu-id="50326-108">The **INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest** method is called if an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was queried from the SHA, but the response never came back.</span></span>

## <a name="syntax"></a><span data-ttu-id="50326-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50326-109">Syntax</span></span>


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="50326-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50326-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50326-111">*CorrelationId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50326-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50326-112">Un puntero a la estructura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) única que identifica el [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)huérfano.</span><span class="sxs-lookup"><span data-stu-id="50326-112">A pointer to the unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies the orphaned [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50326-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50326-113">Return value</span></span>

<span data-ttu-id="50326-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="50326-114">This method can return one of these values.</span></span>



| <span data-ttu-id="50326-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="50326-115">Return code</span></span>                                                                          | <span data-ttu-id="50326-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="50326-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="50326-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="50326-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="50326-118">Indica que se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="50326-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50326-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50326-119">Remarks</span></span>

<span data-ttu-id="50326-120">Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.</span><span class="sxs-lookup"><span data-stu-id="50326-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="50326-121">El sistema puede llamar a este método en los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="50326-121">This method can be called by the system in the following cases:</span></span>

-   <span data-ttu-id="50326-122">No se pudo enviar un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) en la conexión.</span><span class="sxs-lookup"><span data-stu-id="50326-122">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) could not be sent on the wire.</span></span>
-   <span data-ttu-id="50326-123">Se envió un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) de seguridad de red en la conexión, pero no se devolvió ningún **SoHResponse** , es decir, el forzado agotó el tiempo de espera o no había ningún SHV correspondiente en el lado servidor.</span><span class="sxs-lookup"><span data-stu-id="50326-123">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was sent on the wire, but no **SoHResponse** came back, i.e. the enforcer timed out or there was no corresponding SHV on the server-side.</span></span>
-   <span data-ttu-id="50326-124">La conexión dejó de funcionar o un forzado se desconectó.</span><span class="sxs-lookup"><span data-stu-id="50326-124">The connection went down or an enforcer went offline.</span></span>

<span data-ttu-id="50326-125">Esta es solo una notificación de mejor esfuerzo, por lo que los Sha no deben confiar en esta información para limpiar el estado.</span><span class="sxs-lookup"><span data-stu-id="50326-125">This is only a best effort notification, so SHAs must not rely on this information to clean up state.</span></span> <span data-ttu-id="50326-126">Hay varias situaciones en las que un SHA no recibirá ninguna notificación:</span><span class="sxs-lookup"><span data-stu-id="50326-126">There are several situations in which an SHA will not be notified:</span></span>

-   <span data-ttu-id="50326-127">Si un forzador no se comporta, es decir, no notifica al SHA cuando el estado de conexión está inactivo.</span><span class="sxs-lookup"><span data-stu-id="50326-127">If an enforcer misbehaves, i.e. it does not notify the SHA when the connection state is down.</span></span>
-   <span data-ttu-id="50326-128">Si se bloquea un forzador.</span><span class="sxs-lookup"><span data-stu-id="50326-128">If an enforcer crashes.</span></span>
-   <span data-ttu-id="50326-129">En condiciones de error, es decir, el NapAgent no tiene memoria suficiente.</span><span class="sxs-lookup"><span data-stu-id="50326-129">In error conditions, i.e. the NapAgent is out of memory.</span></span>

<span data-ttu-id="50326-130">Los Sha pueden obtener algunas notificaciones falsas cuando se enlazan por primera vez a NapAgent, por ejemplo, si un intercambio de SoH está en curso cuando se enlaza SHA y después se agota el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="50326-130">SHAs may get some spurious notifications when they first bind to the NapAgent, for instance, if an SoH exchange is in progress when the SHA bound, and then it times out.</span></span>

## <a name="requirements"></a><span data-ttu-id="50326-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50326-131">Requirements</span></span>



| <span data-ttu-id="50326-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="50326-132">Requirement</span></span> | <span data-ttu-id="50326-133">Value</span><span class="sxs-lookup"><span data-stu-id="50326-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50326-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50326-134">Minimum supported client</span></span><br/> | <span data-ttu-id="50326-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="50326-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="50326-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50326-136">Minimum supported server</span></span><br/> | <span data-ttu-id="50326-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="50326-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="50326-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50326-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="50326-139"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="50326-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="50326-140">IDL</span><span class="sxs-lookup"><span data-stu-id="50326-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50326-141"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50326-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50326-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="50326-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50326-143">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="50326-143">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





