---
description: El \_ mensaje line AGENTSTATUSEX se envía cuando cambia el estado de un agente ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: Mensaje de LINE_AGENTSTATUSEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680774"
---
# <a name="line_agentstatusex-message"></a><span data-ttu-id="6f938-104">Mensaje de línea \_ AGENTSTATUSEX</span><span class="sxs-lookup"><span data-stu-id="6f938-104">LINE\_AGENTSTATUSEX message</span></span>

<span data-ttu-id="6f938-105">El mensaje **line \_ AGENTSTATUSEX** se envía cuando cambia el estado de un agente ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta.</span><span class="sxs-lookup"><span data-stu-id="6f938-105">The **LINE\_AGENTSTATUSEX** message is sent when the status of an ACD agent changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="6f938-106">Este mensaje se genera mediante la función [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="6f938-106">This message is generated using [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="6f938-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f938-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f938-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="6f938-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6f938-109">Identificador de la aplicación para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="6f938-109">The application's handle to the line device.</span></span> <span data-ttu-id="6f938-110">Esto se relaciona con el controlador del agente.</span><span class="sxs-lookup"><span data-stu-id="6f938-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="6f938-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6f938-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6f938-112">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="6f938-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="6f938-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6f938-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6f938-114">Identificador del agente cuyo estado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="6f938-114">The handle of the agent whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="6f938-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6f938-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6f938-116">Especifica el estado de la cola que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="6f938-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="6f938-117">Puede ser una o varias de las [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="6f938-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f938-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6f938-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6f938-119">Si *dwParam2* incluye el \_ bit de estado LINEAGENTSTATUSEX, *dwParam3* indica el nuevo valor del estado del agente, que es una de [**las \_ constantes de LINEAGENTSTATEEX**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="6f938-119">If *dwParam2* includes the LINEAGENTSTATUSEX \_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="6f938-120">De lo contrario, *dwParam3* se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="6f938-120">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f938-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f938-121">Requirements</span></span>



| <span data-ttu-id="6f938-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f938-122">Requirement</span></span> | <span data-ttu-id="6f938-123">Value</span><span class="sxs-lookup"><span data-stu-id="6f938-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6f938-124">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="6f938-124">TAPI version</span></span><br/> | <span data-ttu-id="6f938-125">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="6f938-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="6f938-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f938-126">Header</span></span><br/>       | <dl> <span data-ttu-id="6f938-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f938-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f938-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f938-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f938-129">**lineGetAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="6f938-129">**lineGetAgentInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[<span data-ttu-id="6f938-130">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="6f938-130">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




