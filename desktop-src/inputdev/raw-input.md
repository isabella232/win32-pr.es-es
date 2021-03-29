---
title: Entrada sin formato
description: En esta sección se describe cómo el sistema proporciona entradas sin formato a la aplicación y cómo una aplicación recibe y procesa esa entrada.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Interfaz de usuario de Windows, entrada de usuario
- Interfaz de usuario de Windows, entrada sin formato
- entrada de usuario, entrada sin formato
- captura de entradas de usuario, entrada sin formato
- entrada sin formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420642"
---
# <a name="raw-input"></a><span data-ttu-id="21d1d-108">Entrada sin formato</span><span class="sxs-lookup"><span data-stu-id="21d1d-108">Raw Input</span></span>

<span data-ttu-id="21d1d-109">En esta sección se describe cómo el sistema proporciona entradas sin formato a la aplicación y cómo una aplicación recibe y procesa esa entrada.</span><span class="sxs-lookup"><span data-stu-id="21d1d-109">This section describes how the system provides raw input to your application and how an application receives and processes that input.</span></span> <span data-ttu-id="21d1d-110">La entrada sin formato se denomina a veces entrada genérica.</span><span class="sxs-lookup"><span data-stu-id="21d1d-110">Raw input is sometimes referred to as generic input.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="21d1d-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="21d1d-111">In This Section</span></span>



| <span data-ttu-id="21d1d-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="21d1d-112">Name</span></span>                                           | <span data-ttu-id="21d1d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="21d1d-113">Description</span></span>                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21d1d-114">Acerca de la entrada sin formato</span><span class="sxs-lookup"><span data-stu-id="21d1d-114">About Raw Input</span></span>](about-raw-input.md)         | <span data-ttu-id="21d1d-115">Describe la entrada del usuario desde dispositivos como joysticks, pantallas táctiles y micrófonos.</span><span class="sxs-lookup"><span data-stu-id="21d1d-115">Discusses user-input from devices such as joysticks, touch screens, and microphones.</span></span><br/> |
| [<span data-ttu-id="21d1d-116">Uso de entrada sin procesar</span><span class="sxs-lookup"><span data-stu-id="21d1d-116">Using Raw Input</span></span>](using-raw-input.md)         | <span data-ttu-id="21d1d-117">Proporciona código de ejemplo para las tareas relacionadas con la entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="21d1d-117">Provides sample code for tasks relating to raw input.</span></span><br/>                                |
| [<span data-ttu-id="21d1d-118">Referencia de entrada sin formato</span><span class="sxs-lookup"><span data-stu-id="21d1d-118">Raw Input Reference</span></span>](raw-input-reference.md) | <span data-ttu-id="21d1d-119">Contiene la referencia de la API.</span><span class="sxs-lookup"><span data-stu-id="21d1d-119">Contains the API reference.</span></span><br/>                                                          |



 

### <a name="functions"></a><span data-ttu-id="21d1d-120">Functions</span><span class="sxs-lookup"><span data-stu-id="21d1d-120">Functions</span></span>



| <span data-ttu-id="21d1d-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="21d1d-121">Name</span></span>                                                                 | <span data-ttu-id="21d1d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="21d1d-122">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21d1d-123">**DefRawInputProc**</span><span class="sxs-lookup"><span data-stu-id="21d1d-123">**DefRawInputProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | <span data-ttu-id="21d1d-124">Llama al procedimiento de entrada sin formato predeterminado para proporcionar el procesamiento predeterminado de los mensajes de entrada sin formato que una aplicación no procesa.</span><span class="sxs-lookup"><span data-stu-id="21d1d-124">Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process.</span></span> <span data-ttu-id="21d1d-125">Esta función garantiza que se procesan todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="21d1d-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="21d1d-126">Se llama a [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) con los mismos parámetros recibidos por el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="21d1d-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) is called with the same parameters received by the window procedure.</span></span> <br/> |
| [<span data-ttu-id="21d1d-127">**GetRawInputBuffer**</span><span class="sxs-lookup"><span data-stu-id="21d1d-127">**GetRawInputBuffer**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | <span data-ttu-id="21d1d-128">Realiza una lectura almacenada en búfer de los datos de entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="21d1d-128">Performs a buffered read of the raw input data.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="21d1d-129">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="21d1d-129">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | <span data-ttu-id="21d1d-130">Obtiene la entrada sin formato del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="21d1d-130">Gets the raw input from the specified device.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="21d1d-131">**GetRawInputDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="21d1d-131">**GetRawInputDeviceInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | <span data-ttu-id="21d1d-132">Obtiene información sobre el dispositivo de entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="21d1d-132">Gets information about the raw input device.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="21d1d-133">**GetRawInputDeviceList**</span><span class="sxs-lookup"><span data-stu-id="21d1d-133">**GetRawInputDeviceList**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | <span data-ttu-id="21d1d-134">Enumera los dispositivos de entrada sin formato conectados al sistema.</span><span class="sxs-lookup"><span data-stu-id="21d1d-134">Enumerates the raw input devices attached to the system.</span></span> <br/>                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="21d1d-135">**GetRegisteredRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="21d1d-135">**GetRegisteredRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | <span data-ttu-id="21d1d-136">Obtiene la información sobre los dispositivos de entrada sin formato para la aplicación actual.</span><span class="sxs-lookup"><span data-stu-id="21d1d-136">Gets the information about the raw input devices for the current application.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="21d1d-137">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="21d1d-137">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | <span data-ttu-id="21d1d-138">Registra los dispositivos que proporcionan los datos de entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="21d1d-138">Registers the devices that supply the raw input data.</span></span><br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a><span data-ttu-id="21d1d-139">Macros</span><span class="sxs-lookup"><span data-stu-id="21d1d-139">Macros</span></span>



| <span data-ttu-id="21d1d-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="21d1d-140">Name</span></span>                                                            | <span data-ttu-id="21d1d-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="21d1d-141">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21d1d-142">**OBTENCIÓN \_ del \_ código RAWINPUT \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="21d1d-142">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | <span data-ttu-id="21d1d-143">Obtiene el código de entrada de *wParam* en la [**\_ entrada de WM**](wm-input.md).</span><span class="sxs-lookup"><span data-stu-id="21d1d-143">Gets the input code from *wParam* in [**WM\_INPUT**](wm-input.md).</span></span><br/>                              |
| [<span data-ttu-id="21d1d-144">**NEXTRAWINPUTBLOCK**</span><span class="sxs-lookup"><span data-stu-id="21d1d-144">**NEXTRAWINPUTBLOCK**</span></span>](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | <span data-ttu-id="21d1d-145">Obtiene la ubicación de la siguiente estructura en una matriz de estructuras [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) .</span><span class="sxs-lookup"><span data-stu-id="21d1d-145">Gets the location of the next structure in an array of [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structures.</span></span> <br/> |



 

### <a name="notifications"></a><span data-ttu-id="21d1d-146">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="21d1d-146">Notifications</span></span>



| <span data-ttu-id="21d1d-147">Nombre</span><span class="sxs-lookup"><span data-stu-id="21d1d-147">Name</span></span>                                                        | <span data-ttu-id="21d1d-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="21d1d-148">Description</span></span>                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="21d1d-149">**entrada de WM \_**</span><span class="sxs-lookup"><span data-stu-id="21d1d-149">**WM\_INPUT**</span></span>](wm-input.md)                               | <span data-ttu-id="21d1d-150">Se envía a la ventana que obtiene la entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="21d1d-150">Sent to the window that is getting raw input.</span></span> <br/>            |
| [<span data-ttu-id="21d1d-151">**\_cambio de \_ dispositivo de entrada de WM \_**</span><span class="sxs-lookup"><span data-stu-id="21d1d-151">**WM\_INPUT\_DEVICE\_CHANGE**</span></span>](wm-input-device-change.md) | <span data-ttu-id="21d1d-152">Se envía a la ventana que se registró para recibir entradas sin procesar.</span><span class="sxs-lookup"><span data-stu-id="21d1d-152">Sent to the window that registered to receive raw input.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="21d1d-153">Estructuras</span><span class="sxs-lookup"><span data-stu-id="21d1d-153">Structures</span></span>



| <span data-ttu-id="21d1d-154">Nombre</span><span class="sxs-lookup"><span data-stu-id="21d1d-154">Name</span></span>                                                            | <span data-ttu-id="21d1d-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="21d1d-155">Description</span></span>                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="21d1d-156">**RAWHID**</span><span class="sxs-lookup"><span data-stu-id="21d1d-156">**RAWHID**</span></span>](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | <span data-ttu-id="21d1d-157">Describe el formato de la entrada sin formato de una Dispositivo de interfaz humana (HID).</span><span class="sxs-lookup"><span data-stu-id="21d1d-157">Describes the format of the raw input from a Human Interface Device (HID).</span></span> <br/> |
| [<span data-ttu-id="21d1d-158">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="21d1d-158">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | <span data-ttu-id="21d1d-159">Contiene la entrada sin formato de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="21d1d-159">Contains the raw input from a device.</span></span> <br/>                                      |
| [<span data-ttu-id="21d1d-160">**RAWINPUTDEVICE**</span><span class="sxs-lookup"><span data-stu-id="21d1d-160">**RAWINPUTDEVICE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | <span data-ttu-id="21d1d-161">Define la información de los dispositivos de entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="21d1d-161">Defines information for the raw input devices.</span></span> <br/>                             |
| [<span data-ttu-id="21d1d-162">**RAWINPUTDEVICELIST**</span><span class="sxs-lookup"><span data-stu-id="21d1d-162">**RAWINPUTDEVICELIST**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | <span data-ttu-id="21d1d-163">Contiene información sobre un dispositivo de entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="21d1d-163">Contains information about a raw input device.</span></span><br/>                              |
| [<span data-ttu-id="21d1d-164">**RAWINPUTHEADER**</span><span class="sxs-lookup"><span data-stu-id="21d1d-164">**RAWINPUTHEADER**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | <span data-ttu-id="21d1d-165">Contiene la información de encabezado que forma parte de los datos de entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="21d1d-165">Contains the header information that is part of the raw input data.</span></span> <br/>        |
| [<span data-ttu-id="21d1d-166">**RAWKEYBOARD**</span><span class="sxs-lookup"><span data-stu-id="21d1d-166">**RAWKEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | <span data-ttu-id="21d1d-167">Contiene información sobre el estado del teclado.</span><span class="sxs-lookup"><span data-stu-id="21d1d-167">Contains information about the state of the keyboard.</span></span> <br/>                      |
| [<span data-ttu-id="21d1d-168">**RAWMOUSE**</span><span class="sxs-lookup"><span data-stu-id="21d1d-168">**RAWMOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | <span data-ttu-id="21d1d-169">Contiene información sobre el estado del mouse.</span><span class="sxs-lookup"><span data-stu-id="21d1d-169">Contains information about the state of the mouse.</span></span> <br/>                         |
| [<span data-ttu-id="21d1d-170">**\_información del dispositivo RID \_**</span><span class="sxs-lookup"><span data-stu-id="21d1d-170">**RID\_DEVICE\_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | <span data-ttu-id="21d1d-171">Define los datos de entrada sin formato procedentes de cualquier dispositivo.</span><span class="sxs-lookup"><span data-stu-id="21d1d-171">Defines the raw input data coming from any device.</span></span> <br/>                         |
| [<span data-ttu-id="21d1d-172">**\_información de dispositivo RID \_ \_ HID**</span><span class="sxs-lookup"><span data-stu-id="21d1d-172">**RID\_DEVICE\_INFO\_HID**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | <span data-ttu-id="21d1d-173">Define los datos de entrada sin formato procedentes del HID especificado.</span><span class="sxs-lookup"><span data-stu-id="21d1d-173">Defines the raw input data coming from the specified HID.</span></span> <br/>                  |
| [<span data-ttu-id="21d1d-174">**\_teclado de \_ información del dispositivo RID \_**</span><span class="sxs-lookup"><span data-stu-id="21d1d-174">**RID\_DEVICE\_INFO\_KEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | <span data-ttu-id="21d1d-175">Define los datos de entrada sin formato procedentes del teclado especificado.</span><span class="sxs-lookup"><span data-stu-id="21d1d-175">Defines the raw input data coming from the specified keyboard.</span></span> <br/>             |
| [<span data-ttu-id="21d1d-176">**\_ \_ mouse información del dispositivo RID \_**</span><span class="sxs-lookup"><span data-stu-id="21d1d-176">**RID\_DEVICE\_INFO\_MOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | <span data-ttu-id="21d1d-177">Define los datos de entrada sin formato procedentes del mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="21d1d-177">Defines the raw input data coming from the specified mouse.</span></span><br/>                 |



 

 

