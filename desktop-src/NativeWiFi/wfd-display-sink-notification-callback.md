---
description: Define la función de devolución \# de llamada&8212; que se implementa en la aplicación&\# 8212; que se especificó para la función WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK función de devolución de llamada (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667131"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a><span data-ttu-id="7c313-103">Función de devolución de llamada de devolución de llamada de \_ \_ notificación del receptor \_ \_ de WFD</span><span class="sxs-lookup"><span data-stu-id="7c313-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK callback function</span></span>

<span data-ttu-id="7c313-104">La función de **devolución de llamada de notificación del receptor de visualización de WFD \_ \_ \_ \_** define la función de devolución de llamada, que se implementa en la aplicación, que se especificó para la función [**WFDStartDisplaySink**](wfdstartdisplaysink.md) .</span><span class="sxs-lookup"><span data-stu-id="7c313-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK** function defines the callback function—which you implement in your app—that was specified to the [**WFDStartDisplaySink**](wfdstartdisplaysink.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c313-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c313-105">Syntax</span></span>


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a><span data-ttu-id="7c313-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c313-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c313-107">*pvContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7c313-107">*pvContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c313-108">Un puntero de contexto opcional que se pasa a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="7c313-108">An optional context pointer passed to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="7c313-109">*pNotification* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c313-109">*pNotification* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c313-110">Puntero a una estructura que contiene datos sobre la notificación de presentación del receptor.</span><span class="sxs-lookup"><span data-stu-id="7c313-110">A pointer to a struct containing data about the display sink notification.</span></span>

</dd> <dt>

<span data-ttu-id="7c313-111">*pNotificationResult* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7c313-111">*pNotificationResult* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c313-112">Un puntero a un struct que contiene los datos que la aplicación puede establecer opcionalmente para indicar el resultado de procesar la notificación de presentación del receptor.</span><span class="sxs-lookup"><span data-stu-id="7c313-112">A pointer to a struct containing data that your app can optionally set to indicate the result of processing the display sink notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c313-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c313-113">Requirements</span></span>



| <span data-ttu-id="7c313-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c313-114">Requirement</span></span> | <span data-ttu-id="7c313-115">Value</span><span class="sxs-lookup"><span data-stu-id="7c313-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7c313-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c313-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7c313-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="7c313-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7c313-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c313-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7c313-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c313-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7c313-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c313-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c313-121"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c313-121"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




