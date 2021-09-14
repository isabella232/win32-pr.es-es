---
title: Entrada sin formato
description: En esta sección se describe cómo el sistema proporciona una entrada sin procesar a la aplicación y cómo una aplicación recibe y procesa esa entrada.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Windows Interfaz de usuario,entrada de usuario
- Windows Interfaz de usuario, entrada sin formato
- entrada del usuario, entrada sin procesar
- captura de la entrada del usuario, entrada sin procesar
- entrada sin procesar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072396"
---
# <a name="raw-input"></a>Entrada sin formato

En esta sección se describe cómo el sistema proporciona una entrada sin procesar a la aplicación y cómo una aplicación recibe y procesa esa entrada. La entrada sin procesar a veces se conoce como entrada genérica.

### <a name="in-this-section"></a>En esta sección



| Nombre                                           | Descripción                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Acerca de la entrada sin procesar](about-raw-input.md)         | Describe la entrada del usuario desde dispositivos como auriculares, pantallas táctiles y micrófonos.<br/> |
| [Uso de entrada sin procesar](using-raw-input.md)         | Proporciona código de ejemplo para las tareas relacionadas con la entrada sin formato.<br/>                                |
| [Referencia de entrada sin formato](raw-input-reference.md) | Contiene la referencia de API.<br/>                                                          |



 

### <a name="functions"></a>Functions



| Nombre                                                                 | Descripción                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | Llama al procedimiento de entrada sin procesar predeterminado para proporcionar el procesamiento predeterminado de los mensajes de entrada sin procesar que una aplicación no procesa. Esta función garantiza que se procese cada mensaje. [**Se llama a DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) con los mismos parámetros recibidos por el procedimiento de ventana. <br/> |
| [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | Realiza una lectura en búfer de los datos de entrada sin procesar.<br/>                                                                                                                                                                                                                                                              |
| [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | Obtiene la entrada sin formato del dispositivo especificado.<br/>                                                                                                                                                                                                                                                                |
| [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | Obtiene información sobre el dispositivo de entrada sin procesar.<br/>                                                                                                                                                                                                                                                                 |
| [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | Enumera los dispositivos de entrada sin procesar conectados al sistema. <br/>                                                                                                                                                                                                                                                    |
| [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | Obtiene la información sobre los dispositivos de entrada sin procesar de la aplicación actual.<br/>                                                                                                                                                                                                                                |
| [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | Registra los dispositivos que suministran los datos de entrada sin procesar.<br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>Macros



| Nombre                                                            | Descripción                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**GET \_ RAWINPUT \_ CODE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | Obtiene el código de entrada de *wParam* en [**WM \_ INPUT**](wm-input.md).<br/>                              |
| [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | Obtiene la ubicación de la siguiente estructura en una matriz de [**estructuras RAWINPUT.**](/windows/win32/api/winuser/ns-winuser-rawinput) <br/> |



 

### <a name="notifications"></a>Notificaciones



| Nombre                                                        | Descripción                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [**ENTRADA \_ WM**](wm-input.md)                               | Se envía a la ventana en la que se está obteniendo la entrada sin procesar. <br/>            |
| [**CAMBIO \_ DE DISPOSITIVO DE ENTRADA DE \_ \_ WM**](wm-input-device-change.md) | Se envía a la ventana que se registró para recibir la entrada sin procesar. <br/> |



 

### <a name="structures"></a>Estructuras



| Nombre                                                            | Descripción                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**RAWHID**](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | Describe el formato de la entrada sin procesar de un dispositivo de interfaz humana (HID). <br/> |
| [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | Contiene la entrada sin procesar de un dispositivo. <br/>                                      |
| [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | Define información para los dispositivos de entrada sin procesar. <br/>                             |
| [**RAWINPUTDEVICELIST**](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | Contiene información sobre un dispositivo de entrada sin procesar.<br/>                              |
| [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | Contiene la información de encabezado que forma parte de los datos de entrada sin procesar. <br/>        |
| [**RAWKEYBOARD**](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | Contiene información sobre el estado del teclado. <br/>                      |
| [**RAWMOUSE**](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | Contiene información sobre el estado del mouse. <br/>                         |
| [**INFORMACIÓN DEL \_ DISPOSITIVO \_ RID**](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | Define los datos de entrada sin procesar procedentes de cualquier dispositivo. <br/>                         |
| [**RID \_ DEVICE \_ INFO \_ HID**](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | Define los datos de entrada sin procesar procedentes del ELEMENTO HID especificado. <br/>                  |
| [**TECLADO DE \_ INFORMACIÓN \_ DEL DISPOSITIVO \_ RID**](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | Define los datos de entrada sin procesar procedentes del teclado especificado. <br/>             |
| [**MOUSE DE \_ INFORMACIÓN \_ DE DISPOSITIVO \_ RID**](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | Define los datos de entrada sin procesar procedentes del mouse especificado.<br/>                 |



 

 

