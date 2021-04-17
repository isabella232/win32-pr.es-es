---
description: Describe la notificación que se pasa a la función de devolución de llamada de notificación de receptor de visualización de WFD \_ \_ \_ \_ .
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: WFD_DISPLAY_SINK_NOTIFICATION estructura (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667130"
---
# <a name="wfd_display_sink_notification-structure"></a><span data-ttu-id="0ce80-103">\_Mostrar la \_ estructura de notificación del receptor \_ de WFD</span><span class="sxs-lookup"><span data-stu-id="0ce80-103">WFD\_DISPLAY\_SINK\_NOTIFICATION structure</span></span>

<span data-ttu-id="0ce80-104">La estructura de notificación del receptor de visualización de WFD describe la notificación que se pasa a la función de devolución de llamada de [**notificación de receptor de visualización de WFD \_ \_ \_ \_**](wfd-display-sink-notification-callback.md) . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0ce80-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION** structure describes the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce80-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ce80-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="0ce80-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ce80-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ce80-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="0ce80-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-108">Un [**\_ encabezado de \_ \_ objeto \_ de receptor de visualización de WFD**](wfd-display-sink-object-header.md) que describe los datos incluidos en la notificación.</span><span class="sxs-lookup"><span data-stu-id="0ce80-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-109">**type**</span><span class="sxs-lookup"><span data-stu-id="0ce80-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-110">Un valor de tipo de notificación de receptor de visualización de WFD que indica el tipo de notificación. [**\_ \_ \_ \_**](wfd-display-sink-notification-type.md)</span><span class="sxs-lookup"><span data-stu-id="0ce80-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification.</span></span> <span data-ttu-id="0ce80-111">Este parámetro también determina la información que se va a usar en la Unión siguiente.</span><span class="sxs-lookup"><span data-stu-id="0ce80-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-112">**strRemoteDeviceName**</span><span class="sxs-lookup"><span data-stu-id="0ce80-112">**strRemoteDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-113">Contiene una cadena terminada en NULL que contiene el nombre del dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="0ce80-113">Contains a NULL-terminated string containing the name of the remote device.</span></span> <span data-ttu-id="0ce80-114">\_ \_ \_ \_ \_ La longitud máxima del nombre del dispositivo del receptor de WFD se define como el valor (32).</span><span class="sxs-lookup"><span data-stu-id="0ce80-114">WFD\_SINK\_MAX\_DEVICE\_NAME\_LENGTH is defined as the value (32).</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-115">**RemoteDeviceAddress**</span><span class="sxs-lookup"><span data-stu-id="0ce80-115">**RemoteDeviceAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-116">Una [**\_ \_ dirección Mac de DOT11**](dot11-mac-address-type.md) que contiene el BSSID del dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="0ce80-116">A [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) that contains the BSSID of the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-117">**ProvisioningRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="0ce80-117">**ProvisioningRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-118">Información sobre una solicitud de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="0ce80-118">Info about a provisioning request.</span></span> <span data-ttu-id="0ce80-119">Use este si *Type* tiene el valor **ProvisioningRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="0ce80-119">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="0ce80-120">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="0ce80-120">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-121">Identificador de la sesión.</span><span class="sxs-lookup"><span data-stu-id="0ce80-121">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-122">**PossibleConfigMethods**</span><span class="sxs-lookup"><span data-stu-id="0ce80-122">**PossibleConfigMethods**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-123">Métodos posibles para mostrar la interfaz de usuario para la aceptación interactiva.</span><span class="sxs-lookup"><span data-stu-id="0ce80-123">Possible methods for showing UI for interactive acceptance.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0ce80-124">**ReconnectRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="0ce80-124">**ReconnectRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-125">Información sobre una solicitud de reconexión.</span><span class="sxs-lookup"><span data-stu-id="0ce80-125">Info about a reconnect request.</span></span> <span data-ttu-id="0ce80-126">Use este si *Type* tiene el valor **ReconnectRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="0ce80-126">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="0ce80-127">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="0ce80-127">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-128">Identificador del grupo.</span><span class="sxs-lookup"><span data-stu-id="0ce80-128">The group id.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0ce80-129">**ConnectedInfo**</span><span class="sxs-lookup"><span data-stu-id="0ce80-129">**ConnectedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-130">Información acerca de una notificación conectada.</span><span class="sxs-lookup"><span data-stu-id="0ce80-130">Info about a connected notification.</span></span> <span data-ttu-id="0ce80-131">Use este si *Type* tiene el valor **ConnectedNotification**.</span><span class="sxs-lookup"><span data-stu-id="0ce80-131">Use this if *type* has the value **ConnectedNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="0ce80-132">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="0ce80-132">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-133">Identificador de la sesión.</span><span class="sxs-lookup"><span data-stu-id="0ce80-133">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-134">**guidSessionInterface**</span><span class="sxs-lookup"><span data-stu-id="0ce80-134">**guidSessionInterface**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-135">Un GUID que indica la interfaz de sesión.</span><span class="sxs-lookup"><span data-stu-id="0ce80-135">A GUID indicating the session interface.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-136">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="0ce80-136">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-137">Identificador del grupo.</span><span class="sxs-lookup"><span data-stu-id="0ce80-137">The group id.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-138">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="0ce80-138">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-139">Puntero a una cadena terminada en NULL que describe el perfil.</span><span class="sxs-lookup"><span data-stu-id="0ce80-139">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-140">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="0ce80-140">**LocalAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-141">Dirección local.</span><span class="sxs-lookup"><span data-stu-id="0ce80-141">The local address.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-142">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="0ce80-142">**RemoteAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-143">La dirección remota.</span><span class="sxs-lookup"><span data-stu-id="0ce80-143">The remote address.</span></span>

</dd> <dt>

<span data-ttu-id="0ce80-144">**uRTSPPort**</span><span class="sxs-lookup"><span data-stu-id="0ce80-144">**uRTSPPort**</span></span>
</dt> <dd>

<span data-ttu-id="0ce80-145">Puerto RTSP.</span><span class="sxs-lookup"><span data-stu-id="0ce80-145">The RTSP port.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ce80-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ce80-146">Requirements</span></span>



| <span data-ttu-id="0ce80-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ce80-147">Requirement</span></span> | <span data-ttu-id="0ce80-148">Value</span><span class="sxs-lookup"><span data-stu-id="0ce80-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce80-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ce80-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0ce80-150">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="0ce80-150">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0ce80-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ce80-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0ce80-152">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ce80-152">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0ce80-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ce80-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ce80-154"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ce80-154"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




