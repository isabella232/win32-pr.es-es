---
description: Describe el resultado que puede establecer de forma opcional después de procesar un notificación receptor de pantalla en la función de devolución de llamada de notificación de receptor de visualización de WFD \_ \_ \_ \_ .
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: WFD_DISPLAY_SINK_NOTIFICATION_RESULT estructura (Wfdsink. h)
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
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669745"
---
# <a name="wfd_display_sink_notification_result-structure"></a><span data-ttu-id="cfe0f-103">La \_ \_ estructura de \_ resultado de notificación de receptor de visualización de WFD \_</span><span class="sxs-lookup"><span data-stu-id="cfe0f-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT structure</span></span>

<span data-ttu-id="cfe0f-104">La estructura de resultados de notificación del receptor de visualización de WFD describe el resultado que puede establecer opcionalmente después de procesar un notificación receptor de pantalla en la función de devolución de llamada de [**notificación de receptor de visualización de WFD \_ \_ \_ \_**](wfd-display-sink-notification-callback.md) . **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cfe0f-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT** structure describes the result that you can optionally set after processing a display sink notfication in the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe0f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfe0f-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="cfe0f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cfe0f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cfe0f-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="cfe0f-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="cfe0f-108">Un [**\_ encabezado de \_ \_ objeto \_ de receptor de visualización de WFD**](wfd-display-sink-object-header.md) que describe los datos incluidos en el resultado de la notificación.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification result.</span></span>

</dd> <dt>

<span data-ttu-id="cfe0f-109">**type**</span><span class="sxs-lookup"><span data-stu-id="cfe0f-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="cfe0f-110">Un valor de tipo de notificación de receptor de visualización de WFD que indica el tipo de resultado de la notificación. [**\_ \_ \_ \_**](wfd-display-sink-notification-type.md)</span><span class="sxs-lookup"><span data-stu-id="cfe0f-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification result.</span></span> <span data-ttu-id="cfe0f-111">Este parámetro también determina la información que se va a usar en la Unión siguiente.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="cfe0f-112">**ProvisioningData**</span><span class="sxs-lookup"><span data-stu-id="cfe0f-112">**ProvisioningData**</span></span>
</dt> <dd>

<span data-ttu-id="cfe0f-113">Información sobre el resultado de una solicitud de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-113">Info about the result of a provisioning request.</span></span> <span data-ttu-id="cfe0f-114">Use este si *Type* tiene el valor **ProvisioningRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-114">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="cfe0f-115">**ConfigMethod**</span><span class="sxs-lookup"><span data-stu-id="cfe0f-115">**ConfigMethod**</span></span>
</dt> <dd>

<span data-ttu-id="cfe0f-116">Método para mostrar la interfaz de usuario para la aceptación interactiva.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-116">The method for showing UI for interactive acceptance.</span></span>

</dd> <dt>

<span data-ttu-id="cfe0f-117">**uPassKeyLength**</span><span class="sxs-lookup"><span data-stu-id="cfe0f-117">**uPassKeyLength**</span></span>
</dt> <dd>

<span data-ttu-id="cfe0f-118">Número de caracteres anchos de la *clave de paso*, sin contar ningún terminador null.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-118">The number of wide characters in *Passkey*, not counting any NULL-terminator.</span></span>

</dd> <dt>

<span data-ttu-id="cfe0f-119">**Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="cfe0f-119">**Passkey**</span></span>
</dt> <dd>

<span data-ttu-id="cfe0f-120">Contiene la clave Pass como una matriz de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-120">Contains the pass key as an array of wide characters.</span></span> <span data-ttu-id="cfe0f-121">\_ \_ \_ \_ \_ La longitud máxima de la clave de paso de información del receptor de WFD \_ se define como el valor (8).</span><span class="sxs-lookup"><span data-stu-id="cfe0f-121">WFD\_SINK\_WPS\_INFO\_MAX\_PASSKEY\_LENGTH is defined as the value (8).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cfe0f-122">**ReconnectData**</span><span class="sxs-lookup"><span data-stu-id="cfe0f-122">**ReconnectData**</span></span>
</dt> <dd>

<span data-ttu-id="cfe0f-123">Información sobre el resultado de una solicitud de reconexión.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-123">Info about the result of a reconnect request.</span></span> <span data-ttu-id="cfe0f-124">Use este si *Type* tiene el valor **ReconnectRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-124">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="cfe0f-125">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="cfe0f-125">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="cfe0f-126">Puntero a una cadena terminada en NULL que describe el perfil.</span><span class="sxs-lookup"><span data-stu-id="cfe0f-126">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfe0f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfe0f-127">Requirements</span></span>



| <span data-ttu-id="cfe0f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe0f-128">Requirement</span></span> | <span data-ttu-id="cfe0f-129">Value</span><span class="sxs-lookup"><span data-stu-id="cfe0f-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe0f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfe0f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe0f-131">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="cfe0f-131">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cfe0f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfe0f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe0f-133">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfe0f-133">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cfe0f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfe0f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfe0f-135"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe0f-135"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




