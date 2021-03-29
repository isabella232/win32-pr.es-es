---
title: Conectar una ventana de captura a un controlador de captura
description: Conectar una ventana de captura a un controlador de captura
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- Mensaje WM_CAP_DRIVER_CONNECT
- capDriverConnect (macro)
- capGetDriverDescription función)
- Mensaje WM_CAP_DRIVER_GET_NAME
- capDriverGetName (macro)
- Mensaje WM_CAP_DRIVER_GET_VERSION
- capDriverGetVersion (macro)
- Mensaje WM_CAP_DRIVER_DISCONNECT
- capDriverDisconnect (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775691"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a><span data-ttu-id="b5f25-112">Conectar una ventana de captura a un controlador de captura</span><span class="sxs-lookup"><span data-stu-id="b5f25-112">Connecting a Capture Window to a Capture Driver</span></span>

<span data-ttu-id="b5f25-113">Puede conectar dinámicamente o desconectar una ventana de captura a un controlador de captura.</span><span class="sxs-lookup"><span data-stu-id="b5f25-113">You can dynamically connect or disconnect a capture window to a capture driver.</span></span> <span data-ttu-id="b5f25-114">Puede conectar o asociar una ventana de captura con un controlador de captura mediante el mensaje de conexión de controlador de Cap de WM (o la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) ). [**\_ \_ \_**](wm-cap-driver-connect.md)</span><span class="sxs-lookup"><span data-stu-id="b5f25-114">You can connect or associate a capture window with a capture driver by using the [**WM\_CAP\_DRIVER\_CONNECT**](wm-cap-driver-connect.md) message (or the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro).</span></span> <span data-ttu-id="b5f25-115">Después de conectar una ventana de captura y un controlador de captura, puede enviar mensajes específicos del dispositivo al controlador de captura asociado a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="b5f25-115">After a capture window and capture driver are connected, you can send device-specific messages to the capture driver associated with a capture window.</span></span>

<span data-ttu-id="b5f25-116">Si tiene más de un dispositivo de captura instalado en un sistema, puede conectar una ventana de captura a un determinado controlador de dispositivo de captura de vídeo especificando un entero para el parámetro *wParam* del mensaje de conexión del controlador de Cap de WM \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b5f25-116">If you have more than one capture device installed on a system, you can connect a capture window to a particular video capture device driver by specifying an integer for the *wParam* parameter of the WM\_CAP\_DRIVER\_CONNECT message.</span></span> <span data-ttu-id="b5f25-117">El entero es un índice que identifica un controlador de captura de vídeo incluido en el registro o en \[ la \] sección de controladores del archivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="b5f25-117">The integer is an index that identifies a video capture driver listed in the registry or in the \[drivers\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="b5f25-118">Use cero para la primera entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="b5f25-118">Use zero for the first index entry.</span></span>

<span data-ttu-id="b5f25-119">Puede recuperar el nombre y la versión de un controlador de captura instalado mediante la función [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) .</span><span class="sxs-lookup"><span data-stu-id="b5f25-119">You can retrieve the name and version of an installed capture driver by using the [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) function.</span></span> <span data-ttu-id="b5f25-120">La aplicación puede usar esta función para enumerar los dispositivos y controladores de captura instalados, de modo que el usuario pueda seleccionar un dispositivo de captura para conectarse a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="b5f25-120">Your application can use this function to enumerate the installed capture devices and drivers, so the user can select a capture device to connect to a capture window.</span></span>

<span data-ttu-id="b5f25-121">Puede recuperar el nombre del controlador de dispositivo de captura conectado a una ventana de captura mediante el uso del [**controlador de Cap de WM \_ \_ \_ Get \_ Name**](wm-cap-driver-get-name.md) Message (o la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) ).</span><span class="sxs-lookup"><span data-stu-id="b5f25-121">You can retrieve the name of the capture device driver connected to a capture window by using the [**WM\_CAP\_DRIVER\_GET\_NAME**](wm-cap-driver-get-name.md) message (or the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro).</span></span> <span data-ttu-id="b5f25-122">Para recuperar la versión de un controlador de captura instalado, use el mensaje de [**versión del controlador de Cap de WM \_ \_ \_ Get \_**](wm-cap-driver-get-version.md) (o la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) ).</span><span class="sxs-lookup"><span data-stu-id="b5f25-122">To retrieve the version of an installed capture driver, use the [**WM\_CAP\_DRIVER\_GET\_VERSION**](wm-cap-driver-get-version.md) message (or the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro).</span></span>

<span data-ttu-id="b5f25-123">Puede desconectar una ventana de captura de un controlador de captura mediante el mensaje de [**\_ \_ \_ desconexión del controlador de Cap de WM**](wm-cap-driver-disconnect.md) (o la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) ).</span><span class="sxs-lookup"><span data-stu-id="b5f25-123">You can disconnect a capture window from a capture driver by using the [**WM\_CAP\_DRIVER\_DISCONNECT**](wm-cap-driver-disconnect.md) message (or the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro).</span></span>

<span data-ttu-id="b5f25-124">Cuando se destruye una ventana de captura, los controladores de dispositivo de captura de vídeo conectados se desconectan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b5f25-124">When an capture window is destroyed, any connected video capture device drivers are automatically disconnected.</span></span>

 

 




