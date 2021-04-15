---
title: Función de devolución de llamada PxeProviderRecvRequest
description: Se le llama cuando se recibe una solicitud de un cliente.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Función de devolución de llamada PxeProviderRecvRequest servicios de implementación de Windows
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422316"
---
# <a name="pxeproviderrecvrequest-callback-function"></a><span data-ttu-id="a80ab-104">Función de devolución de llamada PxeProviderRecvRequest</span><span class="sxs-lookup"><span data-stu-id="a80ab-104">PxeProviderRecvRequest callback function</span></span>

<span data-ttu-id="a80ab-105">Se le llama cuando se recibe una solicitud de un cliente.</span><span class="sxs-lookup"><span data-stu-id="a80ab-105">Called when a request is received from a client.</span></span> <span data-ttu-id="a80ab-106">Esta función se registra mediante una llamada a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el parámetro *CallbackType* establecido en **\_ \_ \_ solicitud de devolución de llamada de PXE**.</span><span class="sxs-lookup"><span data-stu-id="a80ab-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_RECV\_REQUEST**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a80ab-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a><span data-ttu-id="a80ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a80ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80ab-109">*hClientRequest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a80ab-109">*hClientRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80ab-110">Identificador de una solicitud recibida de un cliente.</span><span class="sxs-lookup"><span data-stu-id="a80ab-110">Handle to a request received from a client.</span></span>

</dd> <dt>

<span data-ttu-id="a80ab-111">*pPacket* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a80ab-111">*pPacket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80ab-112">Puntero al búfer de memoria que contiene el paquete recibido.</span><span class="sxs-lookup"><span data-stu-id="a80ab-112">Pointer to the memory buffer that contains the received packet.</span></span>

</dd> <dt>

<span data-ttu-id="a80ab-113">*uPacketLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a80ab-113">*uPacketLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80ab-114">Longitud, en bytes, del búfer al que apunta el parámetro *pPacket* .</span><span class="sxs-lookup"><span data-stu-id="a80ab-114">Length, in bytes, of the buffer pointed to by the *pPacket* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a80ab-115">*pLocalAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a80ab-115">*pLocalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80ab-116">Puntero a una estructura de [**\_ direcciones de PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contiene la dirección local en la que se recibió el paquete.</span><span class="sxs-lookup"><span data-stu-id="a80ab-116">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the local address on which the packet was received.</span></span>

</dd> <dt>

<span data-ttu-id="a80ab-117">*pRemoteAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a80ab-117">*pRemoteAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80ab-118">Puntero a una estructura de [**\_ direcciones de PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contiene la dirección de origen del paquete.</span><span class="sxs-lookup"><span data-stu-id="a80ab-118">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the source address of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="a80ab-119">*pAction* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a80ab-119">*pAction* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a80ab-120">Especifica la acción que debe realizar el sistema.</span><span class="sxs-lookup"><span data-stu-id="a80ab-120">Specifies the action that the system should take.</span></span>



| <span data-ttu-id="a80ab-121">Value</span><span class="sxs-lookup"><span data-stu-id="a80ab-121">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="a80ab-122">Significado</span><span class="sxs-lookup"><span data-stu-id="a80ab-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <span data-ttu-id="a80ab-123"><dt>**PXE \_ BA \_ NBP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a80ab-123"><dt>**PXE\_BA\_NBP**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="a80ab-124">El proveedor respondió a un cliente con un paquete de respuesta DHCP estándar que contiene una ruta de acceso al programa de arranque de red.</span><span class="sxs-lookup"><span data-stu-id="a80ab-124">The provider replied to a client with a standard DHCP response packet that contains a path to the Network Boot Program.</span></span> <span data-ttu-id="a80ab-125">Devolver esta acción significa que el proveedor completó correctamente la solicitud de cliente mediante una llamada a la función [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="a80ab-125">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <span data-ttu-id="a80ab-126"><dt>**PXE \_ BA \_ personalizado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a80ab-126"><dt>**PXE\_BA\_CUSTOM**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="a80ab-127">El proveedor respondió a un cliente mediante una respuesta personalizada que no se ajusta a las especificaciones de DHCP.</span><span class="sxs-lookup"><span data-stu-id="a80ab-127">The provider replied to a client by using a custom response that does not conform to DHCP specifications.</span></span> <span data-ttu-id="a80ab-128">Devolver esta acción significa que el proveedor completó correctamente la solicitud de cliente mediante una llamada a la función [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) al menos una vez.</span><span class="sxs-lookup"><span data-stu-id="a80ab-128">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <span data-ttu-id="a80ab-129"><dt>**PXE \_ BA \_ omitir**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a80ab-129"><dt>**PXE\_BA\_IGNORE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="a80ab-130">El proveedor no desea atender la solicitud del cliente y la solicitud no debe pasarse al siguiente proveedor.</span><span class="sxs-lookup"><span data-stu-id="a80ab-130">The provider does not want to service the client request and the request should not be passed to the next provider.</span></span> <span data-ttu-id="a80ab-131">Se liberan todos los recursos asociados a la solicitud del cliente y se omite la solicitud del cliente.</span><span class="sxs-lookup"><span data-stu-id="a80ab-131">All resources associated with the client request are released and the client request is ignored.</span></span> <span data-ttu-id="a80ab-132">Los proveedores también pueden usar este valor si reconocen el cliente pero la solicitud tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="a80ab-132">Providers can also use this value if they recognize the client but the request was malformed.</span></span><br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <span data-ttu-id="a80ab-133"><dt>**PXE \_ BA \_ rechazado**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a80ab-133"><dt>**PXE\_BA\_REJECTED**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="a80ab-134">El proveedor no desea atender la solicitud del cliente.</span><span class="sxs-lookup"><span data-stu-id="a80ab-134">The provider does not want to service the client request.</span></span> <span data-ttu-id="a80ab-135">El sistema pasa la solicitud al siguiente proveedor de la lista de proveedores registrados.</span><span class="sxs-lookup"><span data-stu-id="a80ab-135">The system passes the request to the next provider in the list of registered providers.</span></span> <span data-ttu-id="a80ab-136">Si este era el último proveedor de la lista, se liberarán todos los recursos asociados a la solicitud del cliente y se omitirá la solicitud del cliente.</span><span class="sxs-lookup"><span data-stu-id="a80ab-136">If this was the last provider in the list, then all resources associated with the client request are released and client request is ignored.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="a80ab-137">*pContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a80ab-137">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80ab-138">Valor de contexto que se pasa a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="a80ab-138">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80ab-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a80ab-139">Return value</span></span>

<span data-ttu-id="a80ab-140">Si el proveedor ha procesado correctamente la solicitud de cliente, la devolución de llamada debe devolver el **error \_ Success** y la **\_ \_ acción de arranque de PXE** a la que apunta el parámetro *pAction* contiene la acción de arranque adecuada para esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="a80ab-140">If the provider successfully processed the client request, the callback should return **ERROR\_SUCCESS** and the **PXE\_BOOT\_ACTION** pointed to by the *pAction* parameter contains the appropriate boot action for this request.</span></span> <span data-ttu-id="a80ab-141">Si el proveedor va a procesar la solicitud de cliente de forma asincrónica, la devolución de llamada debe devolver la **\_ e/s de error \_ pendiente** y llamar a la función [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) cuando se haya procesado la solicitud de cliente.</span><span class="sxs-lookup"><span data-stu-id="a80ab-141">If the provider will process the client request asynchronously, the callback should return **ERROR\_IO\_PENDING** and call the [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) function when the client request has been processed.</span></span> <span data-ttu-id="a80ab-142">En caso de error, se debe devolver un código de error adecuado y el sistema continuará como si se hubiera especificado la acción de arranque de la operación **PXE \_ BA \_ rechazada** .</span><span class="sxs-lookup"><span data-stu-id="a80ab-142">In case of failure, an appropriate error code should be returned and the system will proceed as if the **PXE\_BA\_REJECTED** boot action was specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="a80ab-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a80ab-143">Remarks</span></span>

<span data-ttu-id="a80ab-144">El tipo de paquetes que detecta un proveedor se puede cambiar con la función [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) .</span><span class="sxs-lookup"><span data-stu-id="a80ab-144">The type of packets seen by a provider can be changed with the [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a80ab-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a80ab-145">Requirements</span></span>



| <span data-ttu-id="a80ab-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80ab-146">Requirement</span></span> | <span data-ttu-id="a80ab-147">Value</span><span class="sxs-lookup"><span data-stu-id="a80ab-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a80ab-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a80ab-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a80ab-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a80ab-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="a80ab-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a80ab-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a80ab-151">Windows Server 2008, Windows Server 2003 con \[ solo aplicaciones de escritorio de SP2\]</span><span class="sxs-lookup"><span data-stu-id="a80ab-151">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a80ab-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="a80ab-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80ab-153">Funciones de servidor de servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="a80ab-153">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="a80ab-154">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="a80ab-154">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[<span data-ttu-id="a80ab-155">**PxeSendReply**</span><span class="sxs-lookup"><span data-stu-id="a80ab-155">**PxeSendReply**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[<span data-ttu-id="a80ab-156">**PxeProviderSetAttribute**</span><span class="sxs-lookup"><span data-stu-id="a80ab-156">**PxeProviderSetAttribute**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





