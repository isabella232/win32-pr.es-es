---
title: Acerca de la entrada sin formato
description: En este tema se describe la entrada del usuario desde dispositivos como joysticks, pantallas táctiles y micrófonos.
ms.assetid: 013ed309-f667-47ed-ade0-5e7ca5a0997a
keywords:
- entrada de usuario, entrada sin formato
- captura de entradas de usuario, entrada sin formato
- entrada sin formato
- registrar entradas sin formato
- lectura de entrada sin formato
- entrada sin formato de joystick
- entrada sin formato de pantalla táctil
- entrada sin formato de micrófono
- Dispositivo de interfaz humana (HID)
- HID (Dispositivo de interfaz humana)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3535e5601ec63a254c76060611999a1a2f08aeb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077745"
---
# <a name="about-raw-input"></a>Acerca de la entrada sin formato

Hay muchos dispositivos de entrada de usuario junto con el teclado y el mouse tradicionales. Por ejemplo, los datos proporcionados por el usuario pueden provienen de un joystick, una pantalla táctil, un micrófono u otros dispositivos que permiten una gran flexibilidad en los datos proporcionados por el usuario. Estos dispositivos se conocen colectivamente como dispositivos de interfaz humana (oculta). La API de entrada sin formato proporciona una forma estable y robusta para que las aplicaciones acepten entradas sin procesar de cualquier HID, incluido el teclado y el mouse.

En esta sección se describen los temas siguientes:

-   [Modelo de entrada sin formato](#raw-input-model)
-   [Registro para entradas sin procesar](#registration-for-raw-input)
-   [Lectura de entrada sin formato](#reading-raw-input)

## <a name="raw-input-model"></a>Modelo de entrada sin formato

Anteriormente, el teclado y el mouse normalmente generaban datos de entrada. El sistema interpreta los datos procedentes de estos dispositivos de forma que se eliminen los detalles específicos del dispositivo de la información sin procesar. Por ejemplo, el teclado genera el código de análisis específico del dispositivo, pero el sistema proporciona una aplicación con el código de tecla virtual. Además de ocultar los detalles de la entrada sin formato, el administrador de ventanas no admitía todas las nuevas oculta. Para obtener información de los oculta no admitidos, una aplicación tenía que hacer muchas cosas: abrir el dispositivo, administrar el modo compartido, leer periódicamente el dispositivo o configurar el puerto de finalización de e/s, etc. El modelo de entrada sin formato y las API asociadas se desarrollaron para permitir el acceso sencillo a la entrada sin formato de todos los dispositivos de entrada, incluidos el teclado y el mouse.

El modelo de entrada sin formato es diferente del modelo de entrada de Windows original para el teclado y el mouse. En el modelo de entrada original, una aplicación recibe entradas independientes del dispositivo en forma de mensajes que se envían o se publican en sus ventanas, como [**WM \_ Char**](wm-char.md), [**WM \_ MOUSEMOVE**](wm-mousemove.md)y [**WM \_ APPCOMMAND**](wm-appcommand.md). Por el contrario, para las entradas sin procesar, una aplicación debe registrar los dispositivos de los que desea obtener datos. Además, la aplicación obtiene la entrada sin formato a través del mensaje de [**\_ entrada de WM**](wm-input.md) .

El modelo de entrada sin formato tiene varias ventajas:

-   Una aplicación no tiene que detectar ni abrir el dispositivo de entrada.
-   Una aplicación obtiene los datos directamente del dispositivo y procesa los datos para sus necesidades.
-   Una aplicación puede distinguir el origen de la entrada aunque sea del mismo tipo de dispositivo. Por ejemplo, dos dispositivos de mouse.
-   Una aplicación administra el tráfico de datos especificando datos de una colección de dispositivos o solo tipos de dispositivo específicos.
-   Los dispositivos HID se pueden usar a medida que están disponibles en Marketplace, sin tener que esperar a que los nuevos tipos de mensajes o un SO actualizado tengan nuevos comandos en [**WM \_ APPCOMMAND**](wm-appcommand.md).

Tenga en cuenta que [**WM \_ APPCOMMAND**](wm-appcommand.md) proporciona para algunos dispositivos HID. Sin embargo, **WM \_ APPCOMMAND** es un evento de entrada independiente del dispositivo de nivel superior, mientras que la [**\_ entrada de WM**](wm-input.md) envía datos sin procesar y de bajo nivel que son específicos de un dispositivo.

## <a name="registration-for-raw-input"></a>Registro para entradas sin procesar

De forma predeterminada, ninguna aplicación recibe entradas sin formato. Para recibir entradas sin procesar de un dispositivo, una aplicación debe registrar el dispositivo.

Para registrar dispositivos, una aplicación crea primero una matriz de estructuras [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice) que especifican la [colección de nivel superior](/windows-hardware/drivers/hid/top-level-collections) (TLC) para los dispositivos que desea. La TLC se define mediante una [Página de uso](/windows-hardware/drivers/hid/hid-usages#usage-page) (la clase del dispositivo) y un [identificador de uso](/windows-hardware/drivers/hid/hid-usages#usage-id) (el dispositivo dentro de la clase). Por ejemplo, para obtener el TLC de teclado, establezca UsagePage = 0x01 y UsageID = 0x06. La aplicación llama a [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) para registrar los dispositivos.

Tenga en cuenta que una aplicación puede registrar un dispositivo que no está conectado actualmente al sistema. Cuando este dispositivo está conectado, el administrador de Windows enviará automáticamente la entrada sin formato a la aplicación. Para obtener la lista de dispositivos de entrada sin formato en el sistema, una aplicación llama a [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist). Mediante *hDevice* desde esta llamada, una aplicación llama a [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) para obtener la información del dispositivo.

A través del miembro **dwFlags** de [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice), una aplicación puede seleccionar los dispositivos que se van a escuchar y también aquellos que desea omitir. Por ejemplo, una aplicación puede solicitar información de todos los dispositivos de telefonía, excepto para responder a las máquinas. Para ver el código de ejemplo, consulte [registro para entradas sin procesar](using-raw-input.md).

Tenga en cuenta que el mouse y el teclado también se oculta, por lo que los datos de ellos pueden pasar por la [**\_ entrada de WM**](wm-input.md) de mensajes de HID y desde mensajes tradicionales. Una aplicación puede seleccionar cualquier método mediante la selección adecuada de marcas en [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice).

Para obtener el estado de registro de una aplicación, llame a [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) en cualquier momento.

## <a name="reading-raw-input"></a>Lectura de entrada sin formato

Una aplicación recibe una entrada sin formato de cualquier HID cuya [colección de nivel superior](/windows-hardware/drivers/hid/top-level-collections) (TLC) coincide con un TLC del registro. Cuando una aplicación recibe una entrada sin procesar, su cola de mensajes obtiene un mensaje de [**\_ entrada de WM**](wm-input.md) y se establece la marca de estado de la **cola, \_** **\_ RAWINPUT** Una aplicación puede recibir datos cuando está en primer plano y cuando está en segundo plano.

Hay dos maneras de leer los datos sin procesar: el método no almacenado en búfer (o estándar) y el método almacenado en búfer. El método no almacenado en búfer obtiene los datos sin procesar de una estructura [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) cada vez y es adecuado para muchas oculta. Aquí, la aplicación llama a [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) para obtener el mensaje de [**\_ entrada de WM**](wm-input.md) . A continuación, la aplicación llama a [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata) con el identificador **RAWINPUT** incluido en la **\_ entrada de WM**. Para obtener un ejemplo, vea [realizar una lectura estándar de entrada sin formato](using-raw-input.md).

En cambio, el método almacenado en búfer obtiene una matriz de estructuras [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) a la vez. Esto se proporciona para los dispositivos que pueden generar grandes cantidades de entradas sin procesar. En este método, la aplicación llama a [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) para obtener una matriz de estructuras **RAWINPUT** . Tenga en cuenta que la macro [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock) se usa para recorrer una matriz de estructuras **RAWINPUT** . Para obtener un ejemplo, vea [realizar una lectura almacenada en búfer de entrada sin formato](using-raw-input.md).

Para interpretar la entrada sin formato, se requiere información detallada sobre oculta. Una aplicación obtiene la información del dispositivo llamando a [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) con el identificador del dispositivo. Este identificador puede proviene de [**una \_ entrada de WM**](wm-input.md) o del miembro **hDevice** de [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader).