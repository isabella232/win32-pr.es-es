---
description: Cadenas de identificador de punto de conexión
ms.assetid: 3c955e2d-daaa-4b77-8ca5-890383bb2d39
title: Cadenas de identificador de punto de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fdfbf12f3e037a23163bb3e8fef525db89c15904328c9e0fd8a71e5de004b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957314"
---
# <a name="endpoint-id-strings"></a>Cadenas de identificador de punto de conexión

En Windows Vista, el sistema genera cadenas de identificador de punto de conexión para identificar los dispositivos de punto de conexión de [audio](audio-endpoint-devices.md) en el sistema. Una cadena de identificador de punto de conexión es una cadena de caracteres anchos terminada en NULL. La cadena de identificador de punto de conexión para un dispositivo de punto de conexión de audio determinado identifica de forma única el dispositivo entre todos los dispositivos de punto de conexión de audio del sistema.

Si un sistema contiene dos o más dispositivos de adaptador de audio idénticos, los dispositivos de punto de conexión de audio correspondientes tendrán nombres descriptivos idénticos, pero cada dispositivo de punto de conexión tendrá una cadena de identificador de punto de conexión única. Para obtener más información sobre cómo obtener el nombre descriptivo de un dispositivo de punto de conexión, vea [Propiedades del dispositivo.](device-properties.md)

Después de obtener una instancia de interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para un dispositivo de punto de conexión de audio, un cliente puede llamar al método [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener la cadena de identificador de punto de conexión para el dispositivo. Un cliente puede usar la cadena de identificador de punto de conexión para crear una instancia del dispositivo de punto de conexión de audio más adelante o en un proceso diferente mediante una llamada al método [**IMMDeviceEnumerator::GetDevice.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)

Un cliente puede organizar para recibir una notificación cuando cambia el estado de cualquier dispositivo de punto de conexión de audio. Para recibir notificaciones, el cliente implementa una [**interfaz IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) y registra esa interfaz con la API MMDevice. Cuando cambia el estado de un dispositivo de punto de conexión, la API MMDevice llama al método adecuado en la interfaz [**EDataFlow del**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) cliente. Uno de los parámetros de entrada para el método es la cadena de identificador de punto de conexión que identifica el dispositivo de punto de conexión cuyo estado ha cambiado. Para obtener más información sobre **EDataFlow,** vea [Eventos de dispositivo.](device-events.md)

Las API de audio heredadas, como Direct Sound y las Windows multimedia, tienen sus propias interfaces para enumerar e identificar dispositivos de audio. En Windows Vista, estas interfaces se han ampliado para proporcionar las cadenas de identificador de punto de conexión que identifican los dispositivos de punto de conexión que subyacen a las abstracciones de dispositivos presentadas por las API.

Durante la enumeración de dispositivos Direct Sound, Direct Sound proporciona la cadena de identificador de punto de conexión para cada dispositivo que enumera. Para obtener más información, vea [Eventos de audio para aplicaciones de audio heredadas.](audio-events-for-legacy-audio-applications.md)

Para obtener la cadena de identificador de punto de conexión para un dispositivo de onda heredado, use la función [**waveOutMessage**](/previous-versions//dd743865(v=vs.85)) o [**waveInMessage**](/previous-versions//dd743846(v=vs.85)) para enviar un mensaje QUERYFUNCTIONINSTANCEID DRV al controlador de dispositivo de forma de \_ onda. Para obtener un ejemplo de código que muestra el uso de este mensaje, vea Roles de dispositivo para aplicaciones [Windows multimedia heredadas.](device-roles-for-legacy-windows-multimedia-applications.md)

Para obtener más información sobre el uso de las funcionalidades de las API de audio principales para mejorar las aplicaciones que usan API de audio heredadas, consulte Interoperabilidad con api [de audio heredadas.](interoperability-with-legacy-audio-apis.md)

Los clientes deben tratar el contenido de la cadena de identificador de punto de conexión como opaco. Es decir, los clientes no deben intentar analizar el contenido de la cadena para obtener información sobre el dispositivo. El motivo es que el formato de cadena no está definido y podría cambiar de una implementación del módulo del sistema de API MMDevice a la siguiente.

La duración de una cadena de identificador de punto de conexión está asociada a la instalación del dispositivo. La cadena de identificador de punto de conexión de un dispositivo cambia si el usuario actualiza el controlador de dispositivo o si el usuario desinstala el dispositivo y lo vuelve a instalar. Sin embargo, la cadena de identificador de punto de conexión permanece sin cambios en los reinicios del sistema y la cadena de identificador de punto de conexión de un dispositivo de audio USB permanece sin cambios si el usuario desconecta el dispositivo y lo vuelve a conectar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> </dl>

 

 
