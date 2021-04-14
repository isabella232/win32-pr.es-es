---
description: Limpia el estado de la sesión que se está abriendo o la sesión abierta actualmente.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Función WFDDisplaySinkCloseSession (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544238"
---
# <a name="wfddisplaysinkclosesession-function"></a><span data-ttu-id="cea0b-103">WFDDisplaySinkCloseSession función)</span><span class="sxs-lookup"><span data-stu-id="cea0b-103">WFDDisplaySinkCloseSession function</span></span>

<span data-ttu-id="cea0b-104">Limpia el estado de la sesión que se está abriendo o la sesión abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="cea0b-104">Cleans up the state for the session being opened, or the currently open session.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea0b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cea0b-105">Syntax</span></span>


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a><span data-ttu-id="cea0b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cea0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea0b-107">*hSessionHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cea0b-107">*hSessionHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea0b-108">El identificador recibido a través de la invocación de devolución de llamada de notificación del receptor de visualización de WFD más reciente que incluye uno. [**\_ \_ \_ \_**](wfd-display-sink-notification-callback.md)</span><span class="sxs-lookup"><span data-stu-id="cea0b-108">The handle received via the most recent [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) invocation that included one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea0b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cea0b-109">Return value</span></span>

<span data-ttu-id="cea0b-110">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="cea0b-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea0b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cea0b-111">Remarks</span></span>

<span data-ttu-id="cea0b-112">La aplicación puede llamar a esta función para finalizar la sesión de Miracast por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="cea0b-112">Your app can call this function to terminate the Miracast session for any reason.</span></span> <span data-ttu-id="cea0b-113">No es necesario que la aplicación la llame cuando recibe el tipo **DisconnectedNotification** en su devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="cea0b-113">Your app is not required to call it when it receives the **DisconnectedNotification** type in its callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea0b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cea0b-114">Requirements</span></span>



| <span data-ttu-id="cea0b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea0b-115">Requirement</span></span> | <span data-ttu-id="cea0b-116">Value</span><span class="sxs-lookup"><span data-stu-id="cea0b-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cea0b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cea0b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cea0b-118">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="cea0b-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cea0b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cea0b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cea0b-120">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cea0b-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cea0b-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="cea0b-121">End of client support</span></span><br/>    | <span data-ttu-id="cea0b-122">Windows 10</span><span class="sxs-lookup"><span data-stu-id="cea0b-122">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="cea0b-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="cea0b-123">End of server support</span></span><br/>    | <span data-ttu-id="cea0b-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cea0b-124">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="cea0b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cea0b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cea0b-126"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="cea0b-126"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="cea0b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cea0b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="cea0b-128"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cea0b-128"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="cea0b-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cea0b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cea0b-130"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cea0b-130"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cea0b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="cea0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea0b-132">**\_devolución de \_ llamada de notificación de receptor de pantalla de \_ WFD \_**</span><span class="sxs-lookup"><span data-stu-id="cea0b-132">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




