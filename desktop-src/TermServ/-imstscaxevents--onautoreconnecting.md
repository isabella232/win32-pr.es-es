---
title: IMsTscAxEvents OnAutoReconnecting, método
description: Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD). | IMsTscAxEvents OnAutoReconnecting, método
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Método OnAutoReconnecting Servicios de Escritorio remoto
- Método OnAutoReconnecting Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnAutoReconnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362296"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a><span data-ttu-id="62933-107">IMsTscAxEvents:: OnAutoReconnecting (método)</span><span class="sxs-lookup"><span data-stu-id="62933-107">IMsTscAxEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="62933-108">Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD).</span><span class="sxs-lookup"><span data-stu-id="62933-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="62933-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62933-109">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a><span data-ttu-id="62933-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62933-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62933-111">*disconnectReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62933-111">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62933-112">Código que describe el motivo de la última desconexión de la sesión.</span><span class="sxs-lookup"><span data-stu-id="62933-112">Code describing the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="62933-113">*attemptCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62933-113">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62933-114">Número de intentos realizados en el proceso de reconexión automática actual.</span><span class="sxs-lookup"><span data-stu-id="62933-114">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="62933-115">Este recuento se incrementa en uno por cada intento realizado.</span><span class="sxs-lookup"><span data-stu-id="62933-115">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="62933-116">*pArcContinueStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="62933-116">*pArcContinueStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62933-117">Puntero a un código devuelto que especifica el estado del proceso de reconexión automática.</span><span class="sxs-lookup"><span data-stu-id="62933-117">Pointer to a returned code specifying the state of the automatic reconnection process.</span></span> <span data-ttu-id="62933-118">Este código se puede restablecer para cambiar el estado del proceso de reconexión automática actual.</span><span class="sxs-lookup"><span data-stu-id="62933-118">This code can be reset to change the state of the current automatic reconnection process.</span></span>

<span data-ttu-id="62933-119">Para obtener más información sobre cómo restablecer este código, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="62933-119">For more information about resetting this code, refer to the Remarks section.</span></span>

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span data-ttu-id="62933-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic \* \* \* (0)</span><span class="sxs-lookup"><span data-stu-id="62933-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>\*\*\*\*autoReconnectContinueAutomatic\*\*\*\* (0)</span></span>


</dt> <dd>

<span data-ttu-id="62933-121">El proceso de reconexión se está produciendo automáticamente.</span><span class="sxs-lookup"><span data-stu-id="62933-121">The reconnection process is occurring automatically.</span></span> <span data-ttu-id="62933-122">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="62933-122">This is the default value.</span></span>

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span data-ttu-id="62933-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop \* \* \* \* (1)</span><span class="sxs-lookup"><span data-stu-id="62933-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>\*\*\*\*autoReconnectContinueStop\*\*\*\* (1)</span></span>


</dt> <dd>

<span data-ttu-id="62933-124">Se ha detenido el proceso de reconexión.</span><span class="sxs-lookup"><span data-stu-id="62933-124">The reconnection process has been stopped.</span></span>

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span data-ttu-id="62933-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual \* \* \* \* (2)</span><span class="sxs-lookup"><span data-stu-id="62933-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>\*\*\*\*autoReconnectContinueManual\*\*\*\* (2)</span></span>


</dt> <dd>

<span data-ttu-id="62933-126">El proceso de reconexión se está produciendo manualmente.</span><span class="sxs-lookup"><span data-stu-id="62933-126">The reconnection process is occurring manually.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62933-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62933-127">Return value</span></span>

<span data-ttu-id="62933-128">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="62933-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62933-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62933-129">Remarks</span></span>

<span data-ttu-id="62933-130">Implemente este método en el receptor de eventos para recibir la notificación de que el control está reestableciendo una conexión con un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="62933-130">Implement this method in your event sink to receive notification that the control is reestablishing a connection with an RD Session Host server.</span></span>

<span data-ttu-id="62933-131">Cuando se cambia el estado del proceso de reconexión automática estableciendo el valor del parámetro *pArcContinueStatus* en **autoReconnectContinueAutomatic**, este método funciona en un modo meramente consultivo.</span><span class="sxs-lookup"><span data-stu-id="62933-131">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueAutomatic**, this method functions in a purely advisory mode.</span></span> <span data-ttu-id="62933-132">Los contenedores pueden escuchar este evento en busca de notificaciones que el proceso de reconexión automática está realizando.</span><span class="sxs-lookup"><span data-stu-id="62933-132">Containers can listen to this event for notifications that the automatic reconnection process is proceeding.</span></span> <span data-ttu-id="62933-133">El control seguirá intentando volver a establecer automáticamente una conexión basándose en sus propios recuentos de tiempo internos e intentos.</span><span class="sxs-lookup"><span data-stu-id="62933-133">The control will automatically keep trying to re-establish a connection based on its own internal timing and attempt counts.</span></span> <span data-ttu-id="62933-134">Se llama a este método durante cada intento de reconexión automática a fin de notificar al contenedor.</span><span class="sxs-lookup"><span data-stu-id="62933-134">This method is called during each automatic reconnection attempt in order to notify the container.</span></span>

<span data-ttu-id="62933-135">Cuando cambie el estado del proceso de reconexión automática estableciendo el valor del parámetro *pArcContinueStatus* en **autoReconnectContinueStop**, se terminará el intento de reconexión automática actual, se enviará una notificación de desconexión al contenedor y no se emitirá ninguna notificación de reconexión automática más.</span><span class="sxs-lookup"><span data-stu-id="62933-135">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueStop**, the current automatic reconnection attempt will be terminated, a disconnect notification will be sent to the container, and no further automatic reconnect notifications will be issued.</span></span>

> [!Note]  
> <span data-ttu-id="62933-136">Use la propiedad [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) para habilitar o deshabilitar la reconexión automática.</span><span class="sxs-lookup"><span data-stu-id="62933-136">Use the [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) property to enable or disable automatic reconnection.</span></span>

 

<span data-ttu-id="62933-137">Cuando se cambia el estado del proceso de reconexión automática estableciendo el valor del parámetro *pArcContinueStatus* en **autoReconnectContinueManual**, el contenedor controlará manualmente el proceso de reconexión automática mediante una llamada a [**Connect**](imstscax-connect.md) para desencadenar un intento de conexión o [**desconectar**](imstscax-disconnect.md) para cancelar el proceso de reconexión automática.</span><span class="sxs-lookup"><span data-stu-id="62933-137">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueManual**, the container will manually control the automatic reconnection process by calling [**Connect**](imstscax-connect.md) to trigger a connection attempt or [**Disconnect**](imstscax-disconnect.md) to cancel the automatic reconnection process.</span></span> <span data-ttu-id="62933-138">Una vez establecido este valor, el control dejará de realizar los intentos de reconexión automática y se convertirá en la Directiva del contenedor para **realizar llamadas de conexión para** desencadenar los intentos de reconexión automática.</span><span class="sxs-lookup"><span data-stu-id="62933-138">Once set to this value, the control will stop making automatic reconnection attempts and it becomes the policy of the container to make **Connect** calls to trigger automatic reconnection attempts.</span></span> <span data-ttu-id="62933-139">Esto se hace cuando el contenedor proporciona el comportamiento de la interfaz de usuario personalizado para la reconexión automática, como reiniciar una conexión VPN o RAS quitada antes del proceso de reconexión automática.</span><span class="sxs-lookup"><span data-stu-id="62933-139">This is done when the container provides customized UI behavior for automatic reconnection, such as restarting a dropped RAS or VPN connection before the automatic reconnection process.</span></span>

<span data-ttu-id="62933-140">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="62933-140">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62933-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62933-141">Requirements</span></span>



| <span data-ttu-id="62933-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="62933-142">Requirement</span></span> | <span data-ttu-id="62933-143">Value</span><span class="sxs-lookup"><span data-stu-id="62933-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62933-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62933-144">Minimum supported client</span></span><br/> | <span data-ttu-id="62933-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62933-145">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="62933-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62933-146">Minimum supported server</span></span><br/> | <span data-ttu-id="62933-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62933-147">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="62933-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="62933-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="62933-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62933-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="62933-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62933-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62933-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62933-151"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62933-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="62933-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62933-153">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="62933-153">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





