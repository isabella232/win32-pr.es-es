---
title: Método INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent. h)
description: Se llama a cuando el NapAgent recibe un SoHResponse destinado a este agente de mantenimiento.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Método ProcessSoHResponse NAP
- Método ProcessSoHResponse NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996532"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a><span data-ttu-id="c5ee7-106">INapSystemHealthAgentCallback::P método rocessSoHResponse</span><span class="sxs-lookup"><span data-stu-id="c5ee7-106">INapSystemHealthAgentCallback::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="c5ee7-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c5ee7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c5ee7-108">Se llama al método **INapSystemHealthAgentCallback::P rocesssohresponse** cuando NapAgent recibe un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a este agente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-108">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method is called when the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ee7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5ee7-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="c5ee7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5ee7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ee7-111">*solicitud* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c5ee7-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ee7-112">Puntero COM a un objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica el objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-112">A COM pointer to a [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ee7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5ee7-113">Return value</span></span>

<span data-ttu-id="c5ee7-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c5ee7-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c5ee7-115">Return code</span></span>                                                                                            | <span data-ttu-id="c5ee7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5ee7-116">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5ee7-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ee7-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="c5ee7-118">Indica que se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-118">Indicates success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="c5ee7-119"><dt>**\_paquete NAP E \_ no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ee7-119"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="c5ee7-120">Lo devuelve esta implementación si la respuesta no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-120">Returned by this implementation if the response is not in the correct format.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c5ee7-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5ee7-121">Remarks</span></span>

<span data-ttu-id="c5ee7-122">Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-122">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="c5ee7-123">Cuando el NapAgent recibe un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a este agente de mantenimiento, invoca este método.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-123">When the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent, it invokes this method.</span></span> <span data-ttu-id="c5ee7-124">El agente de mantenimiento debe consultar el SoHResponse desde el objeto de solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-124">The health agent must query the SoHResponse from the request object.</span></span> <span data-ttu-id="c5ee7-125">No debe contener referencias al objeto de solicitud una vez completada esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-125">It must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="c5ee7-126">El método **INapSystemHealthAgentCallback::P rocesssohresponse** no debe bloquearse.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-126">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method must not block.</span></span> <span data-ttu-id="c5ee7-127">Si se requiere un procesamiento de correcciones, cualquier implementación de **ProcessSoHResponse** debe iniciar un nuevo subproceso para realizar el procesamiento de la corrección.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-127">If any fix-up processing is required, any implementation of **ProcessSoHResponse** must start a new thread to perform fix-up processing.</span></span> <span data-ttu-id="c5ee7-128">NapAgent debe llamar a [**INapSystemHealthAgentCallBack:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) para determinar el estado de corrección del Sha.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-128">The NapAgent must call [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) to determine the fix-up status of the SHA.</span></span>

<span data-ttu-id="c5ee7-129">Este método debe devolver **el \_ paquete NAP E \_ no válido \_** si la respuesta no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="c5ee7-129">This method must return **NAP\_E\_INVALID\_PACKET** if the response is not in the correct format.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ee7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5ee7-130">Requirements</span></span>



| <span data-ttu-id="c5ee7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ee7-131">Requirement</span></span> | <span data-ttu-id="c5ee7-132">Value</span><span class="sxs-lookup"><span data-stu-id="c5ee7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ee7-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5ee7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ee7-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c5ee7-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c5ee7-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5ee7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ee7-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5ee7-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c5ee7-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5ee7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ee7-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ee7-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5ee7-139">IDL</span><span class="sxs-lookup"><span data-stu-id="c5ee7-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5ee7-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5ee7-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ee7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5ee7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ee7-142">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="c5ee7-142">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





