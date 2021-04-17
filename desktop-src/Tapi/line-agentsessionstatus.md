---
description: El \_ mensaje line AGENTSESSIONSTATUS se envía cuando cambia el estado de una sesión del agente ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: Mensaje de LINE_AGENTSESSIONSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690741"
---
# <a name="line_agentsessionstatus-message"></a><span data-ttu-id="e6192-104">Mensaje de línea \_ AGENTSESSIONSTATUS</span><span class="sxs-lookup"><span data-stu-id="e6192-104">LINE\_AGENTSESSIONSTATUS message</span></span>

<span data-ttu-id="e6192-105">El mensaje **line \_ AGENTSESSIONSTATUS** se envía cuando cambia el estado de una sesión del agente ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta.</span><span class="sxs-lookup"><span data-stu-id="e6192-105">The **LINE\_AGENTSESSIONSTATUS** message is sent when the status of an ACD agent session changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="e6192-106">Este mensaje se genera mediante la función [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="e6192-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="e6192-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6192-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6192-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="e6192-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e6192-109">Identificador de la aplicación para el dispositivo de línea en el que ha cambiado el estado de la sesión del agente.</span><span class="sxs-lookup"><span data-stu-id="e6192-109">The application's handle to the line device on which the agent session status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e6192-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="e6192-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e6192-111">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="e6192-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="e6192-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e6192-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e6192-113">Identificador de la sesión del agente cuyo estado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e6192-113">A handle of the agent session whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e6192-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e6192-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e6192-115">Especifica el estado de la sesión del agente que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e6192-115">Specifies the agent session status that has changed.</span></span> <span data-ttu-id="e6192-116">Puede ser uno o varios de los **\_ AGENTSESSIONSTATUS de línea**.</span><span class="sxs-lookup"><span data-stu-id="e6192-116">Can be one or more of the **LINE\_AGENTSESSIONSTATUS**.</span></span>

</dd> <dt>

<span data-ttu-id="e6192-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e6192-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e6192-118">Si *dwParam2* incluye el \_ bit de estado LINEAGENTSTATUSEX, *dwParam3* indica el nuevo valor del estado del agente, que es una de [**las \_ constantes de LINEAGENTSTATEEX**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="e6192-118">If *dwParam2* includes the LINEAGENTSTATUSEX\_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="e6192-119">De lo contrario, *dwParam3* se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="e6192-119">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6192-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6192-120">Requirements</span></span>



| <span data-ttu-id="e6192-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6192-121">Requirement</span></span> | <span data-ttu-id="e6192-122">Value</span><span class="sxs-lookup"><span data-stu-id="e6192-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e6192-123">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e6192-123">TAPI version</span></span><br/> | <span data-ttu-id="e6192-124">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="e6192-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="e6192-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6192-125">Header</span></span><br/>       | <dl> <span data-ttu-id="e6192-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6192-126"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6192-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6192-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6192-128">**lineGetAgentSessionInfo**</span><span class="sxs-lookup"><span data-stu-id="e6192-128">**lineGetAgentSessionInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[<span data-ttu-id="e6192-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="e6192-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




