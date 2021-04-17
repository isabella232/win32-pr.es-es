---
description: Cadenas de ID. de punto de conexión
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: Cadenas de ID. de punto de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04c07da78b92795ebadd7d8f9731f7188ae8dc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659311"
---
# <a name="endpoint-id-strings"></a>Cadenas de ID. de punto de conexión

En Windows Vista, el sistema genera cadenas de ID. de punto de conexión para identificar los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md) en el sistema. Una cadena de identificador de punto de conexión es una cadena de caracteres anchos terminada en NULL. La cadena de identificador de punto de conexión de un dispositivo de punto de conexión de audio determinado identifica de forma única el dispositivo entre todos los dispositivos de punto de conexión de audio del sistema.

Si un sistema contiene dos o más dispositivos de adaptador de audio idénticos, los dispositivos de punto de conexión de audio correspondientes tendrán nombres descriptivos idénticos, pero cada dispositivo de extremo tendrá una cadena de identificador de punto de conexión única. Para obtener más información sobre cómo obtener el nombre descriptivo de un dispositivo de punto de conexión, consulte [propiedades del dispositivo](device-properties.md).

Después de obtener una instancia de la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para un dispositivo de punto de conexión de audio, un cliente puede llamar al método [**IMMDevice:: getId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener la cadena de identificador de punto de conexión para el dispositivo. Un cliente puede usar la cadena de identificador de punto de conexión para crear una instancia del dispositivo de punto de conexión de audio más adelante o en un proceso diferente llamando al método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .

Un cliente puede organizar para recibir una notificación cuando cambia el estado de cualquier dispositivo de punto de conexión de audio. Para recibir notificaciones, el cliente implementa una interfaz [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) y registra esa interfaz con la API de MMDevice. Cuando el estado de un dispositivo de punto de conexión cambia, la API de MMDevice llama al método adecuado en la interfaz [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) del cliente. Uno de los parámetros de entrada para el método es la cadena de identificador de extremo que identifica el dispositivo de extremo cuyo estado ha cambiado. Para obtener más información sobre **EDataFlow**, consulte [eventos de dispositivo](device-events.md).

Las API de audio heredadas, como DirectSound y las funciones multimedia de Windows, tienen sus propias interfaces para enumerar e identificar los dispositivos de audio. En Windows Vista, estas interfaces se han ampliado para proporcionar las cadenas de identificador de punto de conexión que identifican los dispositivos de punto de conexión que subyacen a las abstracciones de dispositivo presentadas por las API.

Durante la enumeración de dispositivos DirectSound, DirectSound proporciona la cadena de identificador de punto de conexión para cada dispositivo que enumera. Para obtener más información, consulte [eventos de audio para aplicaciones de audio heredadas](audio-events-for-legacy-audio-applications.md).

Para obtener la cadena de identificador de punto de conexión para un dispositivo de onda de onda heredado, utilice la función [**waveOutMessage**](/previous-versions//dd743865(v=vs.85)) o [**waveInMessage**](/previous-versions//dd743846(v=vs.85)) para enviar un \_ mensaje DRV QUERYFUNCTIONINSTANCEID al controlador de dispositivo de onda. Para ver un ejemplo de código que muestra el uso de este mensaje, consulte [roles de dispositivo para aplicaciones multimedia heredadas de Windows](device-roles-for-legacy-windows-multimedia-applications.md).

Para obtener más información sobre el uso de las funcionalidades de las API de audio principales para mejorar las aplicaciones que usan las API de audio heredadas, consulte [interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md).

Los clientes deben tratar el contenido de la cadena de ID. de punto de conexión como opaco. Es decir, los clientes no deben intentar analizar el contenido de la cadena para obtener información sobre el dispositivo. La razón es que el formato de la cadena no está definido y puede cambiar de una implementación del módulo del sistema de la API de MMDevice al siguiente.

La duración de una cadena de identificador de punto de conexión está ligada a la instalación del dispositivo. La cadena de identificador de punto de conexión de un dispositivo cambia si el usuario actualiza el controlador de dispositivo o si el usuario desinstala el dispositivo y lo vuelve a instalar. Sin embargo, la cadena de identificador de punto de conexión permanece inalterada a lo largo de los reinicios del sistema y la cadena de identificador de punto de conexión de un dispositivo de audio USB permanece sin cambios si el usuario desconecta el dispositivo y lo vuelve a conectar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> </dl>

 

 
