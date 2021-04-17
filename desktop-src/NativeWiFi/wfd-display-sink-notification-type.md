---
description: Define el tipo de notificación que se pasa a la \_ función de devolución de llamada de notificación de receptor de visualización de WFD \_ \_ \_ .
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: Enumeración WFD_DISPLAY_SINK_NOTIFICATION_TYPE (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667129"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a><span data-ttu-id="851c4-103">\_ \_ \_ Enumeración de tipo de notificación de receptor de visualización de WFD \_</span><span class="sxs-lookup"><span data-stu-id="851c4-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE enumeration</span></span>

<span data-ttu-id="851c4-104">El tipo enumerado tipo de notificación de receptor de visualización de WFD define el tipo de notificación que se pasa a la función de devolución de llamada de [**notificación del receptor de visualización de WFD \_ \_ \_ \_**](wfd-display-sink-notification-callback.md) . **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="851c4-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE** enumerated type defines the type of the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="851c4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="851c4-105">Syntax</span></span>


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="851c4-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="851c4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="851c4-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="851c4-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="851c4-108">La notificación es una solicitud de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="851c4-108">The notification is a provisioning request.</span></span>

</dd> <dt>

<span data-ttu-id="851c4-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="851c4-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="851c4-110">La notificación es una solicitud de reconexión.</span><span class="sxs-lookup"><span data-stu-id="851c4-110">The notification is a reconnect request.</span></span>

</dd> <dt>

<span data-ttu-id="851c4-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="851c4-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="851c4-112">La notificación es una notificación conectada.</span><span class="sxs-lookup"><span data-stu-id="851c4-112">The notification is a connected notification.</span></span>

</dd> <dt>

<span data-ttu-id="851c4-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="851c4-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="851c4-114">La notificación es una notificación desconectada.</span><span class="sxs-lookup"><span data-stu-id="851c4-114">The notification is a disconnected notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="851c4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="851c4-115">Requirements</span></span>



| <span data-ttu-id="851c4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="851c4-116">Requirement</span></span> | <span data-ttu-id="851c4-117">Value</span><span class="sxs-lookup"><span data-stu-id="851c4-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="851c4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="851c4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="851c4-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="851c4-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="851c4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="851c4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="851c4-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="851c4-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="851c4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="851c4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="851c4-123"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="851c4-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




