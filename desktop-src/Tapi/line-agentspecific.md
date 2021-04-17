---
description: El \_ mensaje AGENTSPECIFIC de línea de TAPI se envía cuando cambia el estado de un agente ACD en una línea que la aplicación tiene abierta actualmente. La aplicación puede invocar lineGetAgentStatus para determinar el estado actual del agente.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Mensaje de LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680779"
---
# <a name="line_agentspecific-message"></a><span data-ttu-id="7fbd4-104">Mensaje de línea \_ AGENTSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="7fbd4-104">LINE\_AGENTSPECIFIC message</span></span>

<span data-ttu-id="7fbd4-105">El mensaje **\_ AGENTSPECIFIC de línea** de TAPI se envía cuando cambia el estado de un agente ACD en una línea que la aplicación tiene abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-105">The TAPI **LINE\_AGENTSPECIFIC** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="7fbd4-106">La aplicación puede invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar el estado actual del agente.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7fbd4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fbd4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbd4-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="7fbd4-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbd4-109">Identificador de la aplicación para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-109">The application's handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="7fbd4-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="7fbd4-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbd4-111">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="7fbd4-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7fbd4-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbd4-113">Índice en la matriz de identificadores de extensión de controlador en la estructura [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) de la extensión de controlador a la que está asociado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-113">The index into the array of handler extension identifiers in the [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) structure of the handler extension with which the message is associated.</span></span>

</dd> <dt>

<span data-ttu-id="7fbd4-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7fbd4-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbd4-115">Específico de la extensión de controlador.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-115">Specific to the handler extension.</span></span> <span data-ttu-id="7fbd4-116">Normalmente, este valor se usa para hacer que la aplicación invoque una función [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) para capturar más detalles sobre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-116">Generally, this value is used to cause the application to invoke a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) function to fetch further details about the message.</span></span>

</dd> <dt>

<span data-ttu-id="7fbd4-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7fbd4-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbd4-118">Específico de la extensión de controlador.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-118">Specific to the handler extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fbd4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fbd4-119">Return value</span></span>

<span data-ttu-id="7fbd4-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fbd4-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fbd4-121">Remarks</span></span>

<span data-ttu-id="7fbd4-122">El mensaje **line \_ AGENTSPECIFIC** no se envía a las aplicaciones que admiten versiones anteriores de TAPI.</span><span class="sxs-lookup"><span data-stu-id="7fbd4-122">The **LINE\_AGENTSPECIFIC** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbd4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbd4-123">Requirements</span></span>



| <span data-ttu-id="7fbd4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbd4-124">Requirement</span></span> | <span data-ttu-id="7fbd4-125">Value</span><span class="sxs-lookup"><span data-stu-id="7fbd4-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbd4-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="7fbd4-126">TAPI version</span></span><br/> | <span data-ttu-id="7fbd4-127">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7fbd4-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7fbd4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fbd4-128">Header</span></span><br/>       | <dl> <span data-ttu-id="7fbd4-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fbd4-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbd4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fbd4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbd4-131">**LINEAGENTCAPS**</span><span class="sxs-lookup"><span data-stu-id="7fbd4-131">**LINEAGENTCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[<span data-ttu-id="7fbd4-132">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="7fbd4-132">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[<span data-ttu-id="7fbd4-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="7fbd4-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




