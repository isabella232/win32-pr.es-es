---
description: El mensaje de cierre del teléfono TAPI \_ se envía cuando un dispositivo telefónico abierto se ha cerrado forzosamente como parte de la recuperación de recursos. El identificador de dispositivo ya no es válido una vez que se ha enviado el mensaje.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: Mensaje de PHONE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680426"
---
# <a name="phone_close-message"></a><span data-ttu-id="65356-104">Mensaje de cierre del teléfono \_</span><span class="sxs-lookup"><span data-stu-id="65356-104">PHONE\_CLOSE message</span></span>

<span data-ttu-id="65356-105">El mensaje **de \_ cierre del teléfono** TAPI se envía cuando un dispositivo telefónico abierto se ha cerrado forzosamente como parte de la recuperación de recursos.</span><span class="sxs-lookup"><span data-stu-id="65356-105">The TAPI **PHONE\_CLOSE** message is sent when an open phone device has been forcibly closed as part of resource reclamation.</span></span> <span data-ttu-id="65356-106">El identificador de dispositivo ya no es válido una vez que se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="65356-106">The device handle is no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="65356-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65356-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65356-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="65356-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="65356-109">Identificador del dispositivo de teléfono abierto que se cerró.</span><span class="sxs-lookup"><span data-stu-id="65356-109">A handle to the open phone device that was closed.</span></span> <span data-ttu-id="65356-110">El identificador ya no es válido después de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="65356-110">The handle is no longer valid after this message has been sent.</span></span>

</dd> <dt>

<span data-ttu-id="65356-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="65356-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="65356-112">Instancia de devolución de llamada de la aplicación que se proporciona al abrir el dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="65356-112">The application's callback instance that provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="65356-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="65356-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="65356-114">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="65356-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="65356-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="65356-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="65356-116">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="65356-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="65356-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="65356-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="65356-118">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="65356-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65356-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65356-119">Return value</span></span>

<span data-ttu-id="65356-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="65356-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65356-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65356-121">Remarks</span></span>

<span data-ttu-id="65356-122">El mensaje de **\_ cierre de teléfono** solo se envía a una aplicación después de que se haya cerrado un teléfono abierto.</span><span class="sxs-lookup"><span data-stu-id="65356-122">The **PHONE\_CLOSE** message is only sent to an application after an open phone has been forcibly closed.</span></span> <span data-ttu-id="65356-123">Esto se puede hacer para evitar que una sola aplicación monopolice un dispositivo telefónico durante demasiado tiempo.</span><span class="sxs-lookup"><span data-stu-id="65356-123">This can be done to prevent a single application from monopolizing a phone device for too long.</span></span> <span data-ttu-id="65356-124">Si el teléfono se puede volver a abrir inmediatamente después de que un cierre forzado sea específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="65356-124">Whether the phone can be reopened immediately after a forced close is device specific.</span></span>

<span data-ttu-id="65356-125">También se puede cerrar un dispositivo telefónico abierto después de que el usuario haya modificado la configuración de ese teléfono o su controlador.</span><span class="sxs-lookup"><span data-stu-id="65356-125">An open phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="65356-126">Si el usuario desea que los cambios de configuración se apliquen de inmediato (en lugar de después del siguiente reinicio del sistema) y estos cambios afectan a la vista actual del dispositivo (por ejemplo, un cambio en las capacidades del dispositivo), un proveedor de servicios puede forzar el cierre del dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="65356-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and these changes affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="65356-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65356-127">Requirements</span></span>



| <span data-ttu-id="65356-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="65356-128">Requirement</span></span> | <span data-ttu-id="65356-129">Value</span><span class="sxs-lookup"><span data-stu-id="65356-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="65356-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="65356-130">TAPI version</span></span><br/> | <span data-ttu-id="65356-131">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="65356-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="65356-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65356-132">Header</span></span><br/>       | <dl> <span data-ttu-id="65356-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="65356-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




