---
description: El mensaje de cierre de línea TAPI \_ se envía cuando el dispositivo de línea especificado se ha cerrado forzosamente. Una vez que se ha enviado este mensaje, el identificador del dispositivo de línea o los identificadores de llamada de las llamadas en la línea ya no son válidos.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: Mensaje de LINE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690330"
---
# <a name="line_close-message"></a><span data-ttu-id="cfac8-104">Mensaje de cierre de línea \_</span><span class="sxs-lookup"><span data-stu-id="cfac8-104">LINE\_CLOSE message</span></span>

<span data-ttu-id="cfac8-105">El mensaje **de \_ cierre de línea** TAPI se envía cuando el dispositivo de línea especificado se ha cerrado forzosamente.</span><span class="sxs-lookup"><span data-stu-id="cfac8-105">The TAPI **LINE\_CLOSE** message is sent when the specified line device has been forcibly closed.</span></span> <span data-ttu-id="cfac8-106">Una vez que se ha enviado este mensaje, el identificador del dispositivo de línea o los identificadores de llamada de las llamadas en la línea ya no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cfac8-106">The line device handle or any call handles for calls on the line are no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="cfac8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfac8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfac8-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="cfac8-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="cfac8-109">Identificador del dispositivo de línea que se cerró.</span><span class="sxs-lookup"><span data-stu-id="cfac8-109">A handle to the line device that was closed.</span></span> <span data-ttu-id="cfac8-110">Este identificador ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="cfac8-110">This handle is no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="cfac8-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="cfac8-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="cfac8-112">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="cfac8-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="cfac8-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="cfac8-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="cfac8-114">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="cfac8-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="cfac8-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="cfac8-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="cfac8-116">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="cfac8-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="cfac8-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="cfac8-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="cfac8-118">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="cfac8-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfac8-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfac8-119">Return value</span></span>

<span data-ttu-id="cfac8-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cfac8-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfac8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfac8-121">Remarks</span></span>

<span data-ttu-id="cfac8-122">El mensaje de **\_ cierre de línea** se envía a cualquier aplicación solo después de que el proveedor de servicios TAPI (TSP) haya cerrado de manera forzada una línea abierta.</span><span class="sxs-lookup"><span data-stu-id="cfac8-122">The **LINE\_CLOSE** message is sent to any application only after the TAPI service provider (TSP) has forcibly closed an open line.</span></span> <span data-ttu-id="cfac8-123">Si la línea se puede volver a abrir inmediatamente después de que un cierre forzado sea específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cfac8-123">Whether or not the line can be reopened immediately after a forced close is device-specific.</span></span>

<span data-ttu-id="cfac8-124">La condición que causa puede ser un cambio significativo del estado, un error de hardware, una pérdida de conexión con un servidor o incluso potencialmente para impedir que una sola aplicación monopolice un dispositivo de línea durante demasiado tiempo.</span><span class="sxs-lookup"><span data-stu-id="cfac8-124">The causing condition can be a significant change of state, a hardware error, a loss of connection to a server, or even potentially to prevent a single application from monopolizing a line device for too long.</span></span> <span data-ttu-id="cfac8-125">También se puede cerrar un dispositivo de línea una vez que el usuario haya modificado la configuración de esa línea o su controlador.</span><span class="sxs-lookup"><span data-stu-id="cfac8-125">A line device can also be forcibly closed after the user has modified the configuration of that line or its driver.</span></span> <span data-ttu-id="cfac8-126">Si el usuario desea que los cambios de configuración surtan efecto inmediatamente (en lugar de después del siguiente reinicio del sistema) y afectan a la vista actual del dispositivo (por ejemplo, un cambio en las capacidades del dispositivo), un proveedor de servicios puede forzar el cierre del dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="cfac8-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the line device.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfac8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfac8-127">Requirements</span></span>



| <span data-ttu-id="cfac8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfac8-128">Requirement</span></span> | <span data-ttu-id="cfac8-129">Value</span><span class="sxs-lookup"><span data-stu-id="cfac8-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cfac8-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="cfac8-130">TAPI version</span></span><br/> | <span data-ttu-id="cfac8-131">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="cfac8-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cfac8-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfac8-132">Header</span></span><br/>       | <dl> <span data-ttu-id="cfac8-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfac8-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




