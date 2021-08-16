---
title: Acerca de la entrada sin formato
description: En este tema se describe la entrada del usuario desde dispositivos como auriculares, pantallas táctiles y micrófonos.
ms.assetid: 013ed309-f667-47ed-ade0-5e7ca5a0997a
keywords:
- entrada del usuario, entrada sin procesar
- captura de la entrada del usuario, entrada sin procesar
- entrada sin procesar
- registro de entrada sin procesar
- leer la entrada sin procesar
- entrada sin procesar de raw
- entrada sin formato de pantalla táctil
- entrada sin formato de micrófono
- Dispositivo de interfaz humana (HID)
- HID (dispositivo de interfaz humana)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fed3772406cc85df57b95c4b11dbcfeaf60804e94da5602059ec790e87e0439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884332"
---
# <a name="about-raw-input"></a>Acerca de la entrada sin formato

Hay muchos dispositivos de entrada de usuario junto al teclado y el mouse tradicionales. Por ejemplo, la entrada del usuario puede procede de un micrófono, una pantalla táctil, un micrófono u otros dispositivos que permiten una gran flexibilidad en la entrada del usuario. Estos dispositivos se conocen colectivamente como dispositivos de interfaz humana (HID). La API de entrada sin procesar proporciona una manera estable y sólida para que las aplicaciones acepten la entrada sin procesar de cualquier HID, incluidos el teclado y el mouse.

En esta sección se describen los temas siguientes:

-   [Modelo de entrada sin formato](#raw-input-model)
-   [Registro para la entrada sin formato](#registration-for-raw-input)
-   [Lectura de la entrada sin formato](#reading-raw-input)

## <a name="raw-input-model"></a>Modelo de entrada sin formato

Anteriormente, el teclado y el mouse generaba normalmente datos de entrada. El sistema interpretó los datos procedentes de estos dispositivos de una manera que eliminaba los detalles específicos del dispositivo de la información sin procesar. Por ejemplo, el teclado genera el código de examen específico del dispositivo, pero el sistema proporciona a una aplicación el código de clave virtual. Además de ocultar los detalles de la entrada sin procesar, el administrador de ventanas no admite todos los nuevos HID. Para obtener la entrada de los ED no admitidos, una aplicación tenía que hacer muchas cosas: abrir el dispositivo, administrar el modo compartido, leer periódicamente el dispositivo o configurar el puerto de finalización de E/S, etc. El modelo de entrada sin procesar y las API asociadas se desarrollaron para permitir un acceso sencillo a la entrada sin procesar desde todos los dispositivos de entrada, incluidos el teclado y el mouse.

El modelo de entrada sin formato es diferente del modelo de Windows de entrada original para el teclado y el mouse. En el modelo de entrada original, una aplicación recibe entradas independientes del dispositivo en forma de mensajes que se envían o publican en sus ventanas, como [**WM \_ CHAR,**](wm-char.md) [**WM \_ MOUSEMOVE**](wm-mousemove.md)y [**WM \_ APPCOMMAND**](wm-appcommand.md). Por el contrario, para la entrada sin procesar, una aplicación debe registrar los dispositivos de los que quiere obtener datos. Además, la aplicación obtiene la entrada sin procesar a través del [**mensaje \_ WM INPUT.**](wm-input.md)

El modelo de entrada sin procesar tiene varias ventajas:

-   Una aplicación no tiene que detectar ni abrir el dispositivo de entrada.
-   Una aplicación obtiene los datos directamente del dispositivo y los procesa según sus necesidades.
-   Una aplicación puede distinguir el origen de la entrada incluso si es del mismo tipo de dispositivo. Por ejemplo, dos dispositivos del mouse.
-   Una aplicación administra el tráfico de datos especificando datos de una colección de dispositivos o solo tipos de dispositivos específicos.
-   Los dispositivos HID se pueden usar a medida que están disponibles en Marketplace, sin tener que esperar a nuevos tipos de mensaje o a un sistema operativo actualizado para tener nuevos comandos en [**WM \_ APPCOMMAND**](wm-appcommand.md).

Tenga en cuenta [**que WM \_ APPCOMMAND**](wm-appcommand.md) proporciona algunos dispositivos HID. Sin embargo, **WM \_ APPCOMMAND** es un evento de entrada independiente del dispositivo de nivel superior, mientras que [**WM \_ INPUT**](wm-input.md) envía datos sin procesar de bajo nivel específicos de un dispositivo.

## <a name="registration-for-raw-input"></a>Registro para la entrada sin formato

De forma predeterminada, ninguna aplicación recibe entrada sin procesar. Para recibir la entrada sin procesar de un dispositivo, una aplicación debe registrar el dispositivo.

Para registrar dispositivos, una aplicación crea primero una [](/windows-hardware/drivers/hid/top-level-collections) matriz de estructuras [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice) que especifican la colección de nivel superior (TLC) para los dispositivos que desea. El TLC se define mediante una [página](/windows-hardware/drivers/hid/hid-usages#usage-page) de uso (la clase del dispositivo) y un identificador de uso [(el](/windows-hardware/drivers/hid/hid-usages#usage-id) dispositivo dentro de la clase ). Por ejemplo, para obtener el TLC del teclado, establezca UsagePage = 0x01 y UsageID = 0x06. La aplicación llama [**a RegisterRawInputDevices para**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) registrar los dispositivos.

Tenga en cuenta que una aplicación puede registrar un dispositivo que no está conectado actualmente al sistema. Cuando este dispositivo está conectado, Windows Manager enviará automáticamente la entrada sin procesar a la aplicación. Para obtener la lista de dispositivos de entrada sin procesar en el sistema, una aplicación llama a [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist). Mediante el *hDevice de* esta llamada, una aplicación llama a [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) para obtener la información del dispositivo.

A través **del miembro dwFlags** de [**RAWINPUTDEVICE,**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)una aplicación puede seleccionar los dispositivos a los que desea escuchar y también los que quiere omitir. Por ejemplo, una aplicación puede solicitar la entrada de todos los dispositivos de telefonía, excepto los equipos de respuesta. Para obtener código de ejemplo, [vea Registering for Raw Input](using-raw-input.md).

Tenga en cuenta que el mouse y el teclado también son HID, por lo que los datos de ellos pueden llegar a través del mensaje HID [**WM \_ INPUT**](wm-input.md) y de los mensajes tradicionales. Una aplicación puede seleccionar cualquiera de los métodos mediante la selección adecuada de marcas en [**RAWINPUTDEVICE.**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)

Para obtener el estado de registro de una aplicación, llame a [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) en cualquier momento.

## <a name="reading-raw-input"></a>Lectura de la entrada sin formato

Una aplicación recibe la entrada sin procesar de cualquier HID cuya [colección de nivel](/windows-hardware/drivers/hid/top-level-collections) superior (TLC) coincida con un TLC del registro. Cuando una aplicación recibe una entrada sin procesar, su cola de mensajes obtiene un mensaje DE ENTRADA [**DE \_ WM**](wm-input.md) y se establece la marca de estado de la cola **QS \_ RAWINPUT** **(QS \_ INPUT** también incluye esta marca). Una aplicación puede recibir datos cuando está en primer plano y cuando está en segundo plano.

Hay dos maneras de leer los datos sin procesar: el método sin búfer (o estándar) y el método almacenado en búfer. El método sin búfer obtiene los datos sin procesar de una estructura [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) a la vez y es adecuado para muchos HID. En este caso, la aplicación [**llama a GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) para obtener el [**mensaje WM \_ INPUT.**](wm-input.md) A continuación, la aplicación llama a [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata) mediante el **identificador RAWINPUT** contenido en **WM \_ INPUT**. Para obtener un ejemplo, vea [Realizar una lectura estándar de la entrada sin formato.](using-raw-input.md)

Por el contrario, el método almacenado en búfer obtiene una matriz de [**estructuras RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) a la vez. Esto se proporciona para dispositivos que pueden generar grandes cantidades de entrada sin procesar. En este método, la aplicación llama [**a GetRawInputBuffer para**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) obtener una matriz de **estructuras RAWINPUT.** Tenga en cuenta que la macro [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock) se usa para recorrer una matriz de **estructuras RAWINPUT.** Para obtener un ejemplo, vea [Realizar una lectura en búfer de la entrada sin formato.](using-raw-input.md)

Para interpretar la entrada sin formato, se requiere información detallada sobre los ED. Una aplicación obtiene la información del dispositivo mediante una [**llamada a GetRawInputDeviceInfo con**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) el identificador del dispositivo. Este identificador puede procede de [**WM \_ INPUT**](wm-input.md) o del **miembro hDevice** de [**RAWINPUTHEADER.**](/windows/win32/api/winuser/ns-winuser-rawinputheader)