---
description: El mensaje PROXYREQUEST de línea de TAPI \_ entrega una solicitud a un controlador de función de proxy registrado.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: Mensaje de LINE_PROXYREQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690385"
---
# <a name="line_proxyrequest-message"></a><span data-ttu-id="f18e6-103">Mensaje de línea \_ PROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="f18e6-103">LINE\_PROXYREQUEST message</span></span>

<span data-ttu-id="f18e6-104">El mensaje **\_ PROXYREQUEST de línea** de TAPI entrega una solicitud a un controlador de función de proxy registrado.</span><span class="sxs-lookup"><span data-stu-id="f18e6-104">The TAPI **LINE\_PROXYREQUEST** message delivers a request to a registered proxy function handler.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f18e6-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f18e6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f18e6-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="f18e6-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f18e6-107">Identificador de la aplicación para el dispositivo de línea en el que ha cambiado el estado del agente.</span><span class="sxs-lookup"><span data-stu-id="f18e6-107">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="f18e6-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f18e6-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f18e6-109">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f18e6-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="f18e6-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f18e6-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f18e6-111">Puntero a una estructura [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) que contiene la solicitud que va a ser procesada por la aplicación de controlador proxy.</span><span class="sxs-lookup"><span data-stu-id="f18e6-111">Pointer to a [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) structure containing the request to be processed by the proxy handler application.</span></span>

</dd> <dt>

<span data-ttu-id="f18e6-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f18e6-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f18e6-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f18e6-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f18e6-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f18e6-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f18e6-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f18e6-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f18e6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f18e6-116">Return value</span></span>

<span data-ttu-id="f18e6-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f18e6-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f18e6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f18e6-118">Remarks</span></span>

<span data-ttu-id="f18e6-119">El mensaje **line \_ PROXYREQUEST** se envía solo a la primera aplicación que se registró para controlar las solicitudes de proxy del tipo que se está entregando.</span><span class="sxs-lookup"><span data-stu-id="f18e6-119">The **LINE\_PROXYREQUEST** message is sent only to the first application that registered to handle proxy requests of the type being delivered.</span></span>

<span data-ttu-id="f18e6-120">La aplicación debe procesar la solicitud incluida en el búfer del proxy y llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para devolver datos o proporcionar resultados.</span><span class="sxs-lookup"><span data-stu-id="f18e6-120">The application should process the request contained in the proxy buffer and call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) to return data or deliver results.</span></span> <span data-ttu-id="f18e6-121">El procesamiento de la solicitud debe realizarse en el contexto de la función de devolución de llamada TAPI de la aplicación solo si se puede realizar inmediatamente, sin esperar la respuesta de ninguna otra entidad.</span><span class="sxs-lookup"><span data-stu-id="f18e6-121">Processing of the request should be done within the context of the application's TAPI callback function only if it can be performed immediately, without waiting for response from any other entity.</span></span> <span data-ttu-id="f18e6-122">Si la aplicación necesita comunicarse con otras entidades (por ejemplo, un proveedor de servicios para controlar ACD basado en PBX o cualquier otro servicio del sistema que pueda provocar un bloqueo), la solicitud se debe poner en cola dentro de la aplicación y salir de la función de devolución de llamada para evitar el retraso de la recepción de mensajes TAPI adicionales por parte de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f18e6-122">If the application needs to communicate with other entities (for example, a service provider to handle PBX-based ACD, or any other system service which might result in blocking), then the request should be queued within the application and the callback function exited to avoid delaying the receipt of further TAPI messages by the application.</span></span>

<span data-ttu-id="f18e6-123">En el momento en que se entrega la **línea \_ PROXYREQUEST** al controlador de proxy, TAPI ya ha devuelto un resultado de función *dwRequestID* positivo a la aplicación original y desbloqueó el subproceso que realiza la llamada para continuar la ejecución.</span><span class="sxs-lookup"><span data-stu-id="f18e6-123">At the time the **LINE\_PROXYREQUEST** is delivered to the proxy handler, TAPI has already returned a positive *dwRequestID* function result to the original application and unblocked the calling thread to continue execution.</span></span> <span data-ttu-id="f18e6-124">La aplicación espera un mensaje de [**\_ respuesta de línea**](line-reply.md) , que se genera automáticamente cuando la aplicación de controlador de proxy llama a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="f18e6-124">The application is awaiting a [**LINE\_REPLY**](line-reply.md) message, which is automatically generated when the proxy handler application calls [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span>

<span data-ttu-id="f18e6-125">La aplicación no debe liberar la memoria a la que apunta *lpProxyRequest*.</span><span class="sxs-lookup"><span data-stu-id="f18e6-125">The application shall not free the memory pointed to by *lpProxyRequest*.</span></span> <span data-ttu-id="f18e6-126">TAPI libera la memoria durante la ejecución de [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="f18e6-126">TAPI frees the memory during the execution of [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span> <span data-ttu-id="f18e6-127">La aplicación puede llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactamente una vez por cada mensaje **\_ PROXYREQUEST de línea** .</span><span class="sxs-lookup"><span data-stu-id="f18e6-127">The application can call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactly once for each **LINE\_PROXYREQUEST** message.</span></span>

<span data-ttu-id="f18e6-128">Si la aplicación recibe un mensaje de [**\_ cierre de línea**](line-close.md) mientras tiene solicitudes de proxy pendientes, debe llamar a [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para cada solicitud pendiente, pasando un valor de *dwResult* adecuado (como LINEERR \_ OPERATIONFAILED).</span><span class="sxs-lookup"><span data-stu-id="f18e6-128">If the application receives a [**LINE\_CLOSE**](line-close.md) message while it has pending proxy requests, it should call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) for each pending request, passing in an appropriate *dwResult* value (such as LINEERR\_OPERATIONFAILED).</span></span>

## <a name="requirements"></a><span data-ttu-id="f18e6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f18e6-129">Requirements</span></span>



| <span data-ttu-id="f18e6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f18e6-130">Requirement</span></span> | <span data-ttu-id="f18e6-131">Value</span><span class="sxs-lookup"><span data-stu-id="f18e6-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f18e6-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f18e6-132">TAPI version</span></span><br/> | <span data-ttu-id="f18e6-133">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f18e6-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f18e6-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f18e6-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f18e6-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f18e6-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f18e6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f18e6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18e6-137">**cierre de línea \_**</span><span class="sxs-lookup"><span data-stu-id="f18e6-137">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="f18e6-138">**respuesta de línea \_**</span><span class="sxs-lookup"><span data-stu-id="f18e6-138">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="f18e6-139">**LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="f18e6-139">**LINEPROXYREQUEST**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[<span data-ttu-id="f18e6-140">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="f18e6-140">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




