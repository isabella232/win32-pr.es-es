---
title: Método INapSystemHealthAgentCallback NotifySystemIsolationStateChange (NapSystemHealthAgent. h)
description: El NapAgent llama a este método para indicar que ha cambiado el estado de aislamiento del sistema o la hora de finalización del período de prueba.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- Método NotifySystemIsolationStateChange NAP
- Método NotifySystemIsolationStateChange NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método NotifySystemIsolationStateChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802617"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a><span data-ttu-id="be285-106">INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange (método)</span><span class="sxs-lookup"><span data-stu-id="be285-106">INapSystemHealthAgentCallback::NotifySystemIsolationStateChange method</span></span>

> [!Note]  
> <span data-ttu-id="be285-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="be285-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="be285-108">El NapAgent llama al método **INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange** para indicar que ha cambiado el estado de aislamiento del sistema o el tiempo de finalización del período de prueba.</span><span class="sxs-lookup"><span data-stu-id="be285-108">The **INapSystemHealthAgentCallback::NotifySystemIsolationStateChange** method is called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="be285-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be285-109">Syntax</span></span>


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a><span data-ttu-id="be285-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be285-110">Parameters</span></span>

<span data-ttu-id="be285-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="be285-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be285-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be285-112">Return value</span></span>

<span data-ttu-id="be285-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="be285-113">This method can return one of these values.</span></span>



| <span data-ttu-id="be285-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="be285-114">Return code</span></span>                                                                          | <span data-ttu-id="be285-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="be285-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="be285-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="be285-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="be285-117">Indica que se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="be285-117">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="be285-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be285-118">Remarks</span></span>

<span data-ttu-id="be285-119">Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.</span><span class="sxs-lookup"><span data-stu-id="be285-119">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="be285-120">El agente de mantenimiento puede consultar el estado de NAP del sistema mediante [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="be285-120">The health agent can query the system NAP state using the [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be285-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be285-121">Requirements</span></span>



| <span data-ttu-id="be285-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="be285-122">Requirement</span></span> | <span data-ttu-id="be285-123">Value</span><span class="sxs-lookup"><span data-stu-id="be285-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be285-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be285-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be285-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="be285-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="be285-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be285-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be285-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="be285-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be285-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be285-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="be285-129"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="be285-129"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="be285-130">IDL</span><span class="sxs-lookup"><span data-stu-id="be285-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be285-131"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be285-131"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be285-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="be285-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be285-133">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="be285-133">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





