---
description: Realiza la inicialización necesaria para permitir que la aplicación que realiza la llamada se convierta en un receptor de pantalla Miracast.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Función WFDDisplaySinkStart (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544235"
---
# <a name="wfddisplaysinkstart-function"></a><span data-ttu-id="d0ba0-103">WFDDisplaySinkStart función)</span><span class="sxs-lookup"><span data-stu-id="d0ba0-103">WFDDisplaySinkStart function</span></span>

<span data-ttu-id="d0ba0-104">Realiza la inicialización necesaria para permitir que la aplicación que realiza la llamada se convierta en un receptor de pantalla Miracast.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-104">Performs the necessary initialization to allow the calling app to become a Miracast display sink.</span></span> <span data-ttu-id="d0ba0-105">La aplicación debe llamarla una vez al inicio.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-105">Your app should call this once on startup.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ba0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0ba0-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a><span data-ttu-id="d0ba0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0ba0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ba0-108">*uDeviceCategory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0ba0-108">*uDeviceCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ba0-109">La categoría de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-109">The device category.</span></span>

</dd> <dt>

<span data-ttu-id="d0ba0-110">*uSubCategory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0ba0-110">*uSubCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ba0-111">Subcategoría del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-111">The device subcategory.</span></span>

</dd> <dt>

<span data-ttu-id="d0ba0-112">*pCallbackContext* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d0ba0-112">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ba0-113">Un puntero de contexto opcional que se pasa a la función de devolución de llamada especificada en el parámetro *pfnCallback* .</span><span class="sxs-lookup"><span data-stu-id="d0ba0-113">An optional context pointer which is passed to the callback function specified in the *pfnCallback* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d0ba0-114">*pfnCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0ba0-114">*pfnCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ba0-115">Un puntero a la función de devolución de llamada a la que se llamará siempre que haya una notificación para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-115">A pointer to the callback function to be called whenever there is a notification for the app.</span></span> <span data-ttu-id="d0ba0-116">Las notificaciones que se pueden enviar se describen en la [**devolución de llamada de notificación de receptor de visualización de WFD \_ \_ \_ \_**](wfd-display-sink-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="d0ba0-116">Notifications that can be sent are described in [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ba0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0ba0-117">Return value</span></span>

<span data-ttu-id="d0ba0-118">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="d0ba0-119">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-119">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="d0ba0-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d0ba0-120">Return code</span></span>                                                                                          | <span data-ttu-id="d0ba0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0ba0-121">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="d0ba0-122"><dt>**ERROR \_ no \_ admitido**</dt></span><span class="sxs-lookup"><span data-stu-id="d0ba0-122"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="d0ba0-123">El receptor de pantalla no es compatible con este hardware.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-123">The display sink is not supported on this hardware.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0ba0-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0ba0-124">Remarks</span></span>

<span data-ttu-id="d0ba0-125">Esta función realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d0ba0-125">This function performs the following tasks:</span></span>

-   <span data-ttu-id="d0ba0-126">Hace que el equipo sea reconocible</span><span class="sxs-lookup"><span data-stu-id="d0ba0-126">Makes the PC discoverable</span></span>
-   <span data-ttu-id="d0ba0-127">Establece la información del dispositivo P2P para reflejar la categoría y la subcategoría especificada.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-127">Sets the P2P device info to reflect the category and sub category specified</span></span>
-   <span data-ttu-id="d0ba0-128">Establece las s de Miracast en todas Wi-Fi tramas directas con el tipo de dispositivo como receptor</span><span class="sxs-lookup"><span data-stu-id="d0ba0-128">Sets the Miracast IEs on all Wi-Fi Direct frames with the device type as the sink</span></span>
-   <span data-ttu-id="d0ba0-129">Registra la devolución de llamada especificada que se va a invocar siempre que haya una conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="d0ba0-129">Registers the specified callback to be invoked whenever there is an incoming connection</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ba0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0ba0-130">Requirements</span></span>



| <span data-ttu-id="d0ba0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0ba0-131">Requirement</span></span> | <span data-ttu-id="d0ba0-132">Value</span><span class="sxs-lookup"><span data-stu-id="d0ba0-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ba0-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0ba0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ba0-134">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="d0ba0-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d0ba0-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0ba0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ba0-136">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0ba0-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0ba0-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d0ba0-137">End of client support</span></span><br/>    | <span data-ttu-id="d0ba0-138">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d0ba0-138">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="d0ba0-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d0ba0-139">End of server support</span></span><br/>    | <span data-ttu-id="d0ba0-140">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d0ba0-140">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="d0ba0-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0ba0-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0ba0-142"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0ba0-142"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="d0ba0-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0ba0-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0ba0-144"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0ba0-144"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="d0ba0-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0ba0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0ba0-146"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0ba0-146"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ba0-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0ba0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ba0-148">**\_devolución de \_ llamada de notificación de receptor de pantalla de \_ WFD \_**</span><span class="sxs-lookup"><span data-stu-id="d0ba0-148">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




