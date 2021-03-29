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
# <a name="raw-input"></a>Entrada sin formato

En esta sección se describe cómo el sistema proporciona entradas sin formato a la aplicación y cómo una aplicación recibe y procesa esa entrada. La entrada sin formato se denomina a veces entrada genérica.

### <a name="in-this-section"></a>En esta sección



| Nombre                                           | Descripción                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Acerca de la entrada sin formato](about-raw-input.md)         | Describe la entrada del usuario desde dispositivos como joysticks, pantallas táctiles y micrófonos.<br/> |
| [Uso de entrada sin procesar](using-raw-input.md)         | Proporciona código de ejemplo para las tareas relacionadas con la entrada sin formato.<br/>                                |
| [Referencia de entrada sin formato](raw-input-reference.md) | Contiene la referencia de la API.<br/>                                                          |



 

### <a name="functions"></a>Functions



| Nombre                                                                 | Descripción                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | Llama al procedimiento de entrada sin formato predeterminado para proporcionar el procesamiento predeterminado de los mensajes de entrada sin formato que una aplicación no procesa. Esta función garantiza que se procesan todos los mensajes. Se llama a [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) con los mismos parámetros recibidos por el procedimiento de ventana. <br/> |
| [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | Realiza una lectura almacenada en búfer de los datos de entrada sin formato.<br/>                                                                                                                                                                                                                                                              |
| [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | Obtiene la entrada sin formato del dispositivo especificado.<br/>                                                                                                                                                                                                                                                                |
| [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | Obtiene información sobre el dispositivo de entrada sin formato.<br/>                                                                                                                                                                                                                                                                 |
| [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | Enumera los dispositivos de entrada sin formato conectados al sistema. <br/>                                                                                                                                                                                                                                                    |
| [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | Obtiene la información sobre los dispositivos de entrada sin formato para la aplicación actual.<br/>                                                                                                                                                                                                                                |
| [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | Registra los dispositivos que proporcionan los datos de entrada sin formato.<br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>Macros



| Nombre                                                            | Descripción                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**OBTENCIÓN \_ del \_ código RAWINPUT \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | Obtiene el código de entrada de *wParam* en la [**\_ entrada de WM**](wm-input.md).<br/>                              |
| [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | Obtiene la ubicación de la siguiente estructura en una matriz de estructuras [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) . <br/> |



 

### <a name="notifications"></a>Notificaciones



| Nombre                                                        | Descripción                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [**entrada de WM \_**](wm-input.md)                               | Se envía a la ventana que obtiene la entrada sin formato. <br/>            |
| [**\_cambio de \_ dispositivo de entrada de WM \_**](wm-input-device-change.md) | Se envía a la ventana que se registró para recibir entradas sin procesar. <br/> |



 

### <a name="structures"></a>Estructuras



| Nombre                                                            | Descripción                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**RAWHID**](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | Describe el formato de la entrada sin formato de una Dispositivo de interfaz humana (HID). <br/> |
| [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | Contiene la entrada sin formato de un dispositivo. <br/>                                      |
| [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | Define la información de los dispositivos de entrada sin formato. <br/>                             |
| [**RAWINPUTDEVICELIST**](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | Contiene información sobre un dispositivo de entrada sin formato.<br/>                              |
| [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | Contiene la información de encabezado que forma parte de los datos de entrada sin formato. <br/>        |
| [**RAWKEYBOARD**](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | Contiene información sobre el estado del teclado. <br/>                      |
| [**RAWMOUSE**](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | Contiene información sobre el estado del mouse. <br/>                         |
| [**\_información del dispositivo RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | Define los datos de entrada sin formato procedentes de cualquier dispositivo. <br/>                         |
| [**\_información de dispositivo RID \_ \_ HID**](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | Define los datos de entrada sin formato procedentes del HID especificado. <br/>                  |
| [**\_teclado de \_ información del dispositivo RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | Define los datos de entrada sin formato procedentes del teclado especificado. <br/>             |
| [**\_ \_ mouse información del dispositivo RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | Define los datos de entrada sin formato procedentes del mouse especificado.<br/>                 |



 

 

