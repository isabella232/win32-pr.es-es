---
description: El \_ mensaje AGENTSTATUS de línea de TAPI se envía cuando cambia el estado de un agente ACD en una línea que la aplicación tiene abierta actualmente. La aplicación puede invocar lineGetAgentStatus para determinar el estado actual del agente.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: Mensaje de LINE_AGENTSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690739"
---
# <a name="line_agentstatus-message"></a><span data-ttu-id="7d25d-104">Mensaje de línea \_ AGENTSTATUS</span><span class="sxs-lookup"><span data-stu-id="7d25d-104">LINE\_AGENTSTATUS message</span></span>

<span data-ttu-id="7d25d-105">El mensaje **\_ AGENTSTATUS de línea** de TAPI se envía cuando cambia el estado de un agente ACD en una línea que la aplicación tiene abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="7d25d-105">The TAPI **LINE\_AGENTSTATUS** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="7d25d-106">La aplicación puede invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar el estado actual del agente.</span><span class="sxs-lookup"><span data-stu-id="7d25d-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7d25d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d25d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d25d-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="7d25d-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7d25d-109">Identificador de la aplicación para el dispositivo de línea en el que ha cambiado el estado del agente.</span><span class="sxs-lookup"><span data-stu-id="7d25d-109">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="7d25d-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="7d25d-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7d25d-111">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="7d25d-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="7d25d-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7d25d-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7d25d-113">Identificador de la dirección en la línea en la que cambió el estado del agente.</span><span class="sxs-lookup"><span data-stu-id="7d25d-113">Identifier of the address on the line on which the agent status changed.</span></span> <span data-ttu-id="7d25d-114">Un identificador de dirección está asociado de forma permanente a una dirección; el identificador permanece constante en las actualizaciones del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7d25d-114">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="7d25d-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7d25d-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7d25d-116">Especifica el estado del agente que ha cambiado; puede ser una combinación de [**\_ constantes LINEAGENTSTATUS**](lineagentstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="7d25d-116">Specifies the agent status that has changed; can be a combination of [**LINEAGENTSTATUS\_ constants**](lineagentstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d25d-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7d25d-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7d25d-118">Si *dwParam2* incluye el \_ bit de estado LINEAGENTSTATUS, *dwParam3* indica el nuevo valor del miembro **dwState** en [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span><span class="sxs-lookup"><span data-stu-id="7d25d-118">If *dwParam2* includes the LINEAGENTSTATUS\_STATE bit, then *dwParam3* indicates the new value of the **dwState** member in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span></span> <span data-ttu-id="7d25d-119">De lo contrario, este parámetro se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="7d25d-119">Otherwise, this parameter is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d25d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d25d-120">Return value</span></span>

<span data-ttu-id="7d25d-121">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7d25d-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d25d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d25d-122">Remarks</span></span>

<span data-ttu-id="7d25d-123">El mensaje **line \_ AGENTSTATUS** no se envía a las aplicaciones que admiten versiones anteriores de TAPI.</span><span class="sxs-lookup"><span data-stu-id="7d25d-123">The **LINE\_AGENTSTATUS** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d25d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d25d-124">Requirements</span></span>



| <span data-ttu-id="7d25d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d25d-125">Requirement</span></span> | <span data-ttu-id="7d25d-126">Value</span><span class="sxs-lookup"><span data-stu-id="7d25d-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7d25d-127">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="7d25d-127">TAPI version</span></span><br/> | <span data-ttu-id="7d25d-128">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7d25d-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7d25d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d25d-129">Header</span></span><br/>       | <dl> <span data-ttu-id="7d25d-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d25d-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d25d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d25d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d25d-132">**LINEAGENTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="7d25d-132">**LINEAGENTSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[<span data-ttu-id="7d25d-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="7d25d-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




