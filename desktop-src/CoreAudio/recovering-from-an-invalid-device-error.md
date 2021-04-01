---
description: Recuperación de un error de Invalid-Device
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: Recuperación de un error de Invalid-Device
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca20c32be46367f53a14ce26c39f980e3649b652
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153398"
---
# <a name="recovering-from-an-invalid-device-error"></a>Recuperación de un error de Invalid-Device

Muchos de los métodos de WASAPI devuelven el código de error AUDCLNT \_ E \_ \_ se invalidan si el dispositivo de punto de conexión de audio que utiliza la aplicación cliente deja de ser válido. Este código de error indica que el dispositivo de punto de conexión se ha desconectado, o que el hardware de audio o los recursos de hardware asociados se han reconfigurado, deshabilitado, quitado o no está disponible para su uso. Con frecuencia, la aplicación puede recuperarse de este error.

>[!NOTE]
> Para obtener información sobre cómo recuperarse de errores de dispositivo no válidos al usar las API de audio espacial (ISAC), consulte [recuperación de un error de Invalid-Device (sonido espacial)](recovering-from-an-invalid-device-error-spatial-sound.md) .

La estrategia que debe usar una aplicación para recuperarse de un \_ \_ \_ error invalidado del dispositivo AUDCLNT depende de cuál de las siguientes técnicas use la aplicación para seleccionar un dispositivo de punto de conexión de audio:

-   Seleccione siempre el dispositivo de captura o representación de audio predeterminado.
-   Seleccione un dispositivo de punto de conexión de audio específico.

En el último caso, la aplicación selecciona automáticamente un dispositivo específico según los requisitos internos o permite al usuario seleccionar explícitamente un dispositivo en una lista de dispositivos disponibles.

Una aplicación que usa el dispositivo predeterminado puede intentar recuperarse de un \_ \_ \_ error invalidado del dispositivo AUDCLNT E:

1.  Libere la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) y cualquier otra interfaz WASAPI que haya adquirido en el dispositivo.
2.  Llame al método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener el dispositivo de audio predeterminado actual.
3.  Intente activar [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) en el dispositivo de audio predeterminado.

Al seguir los pasos anteriores, la aplicación tiende a responder correctamente, independientemente de la causa del \_ \_ \_ error invalidado del dispositivo AUDCLNT E. Si la reconfiguración del dispositivo predeterminado provocó el error (por ejemplo, si el usuario cambia el formato de secuencia usado por el dispositivo), estos pasos, si se realizan correctamente, permiten que la aplicación siga usando el mismo dispositivo. Si el usuario ha deshabilitado o quitado el dispositivo que estaba usando la aplicación y hay otro dispositivo disponible para asumir el rol de dispositivo predeterminado, la aplicación puede continuar usando el nuevo dispositivo predeterminado. En cualquier caso, la aplicación se adapta automáticamente sin requerir la intervención del usuario.

Una aplicación que selecciona un dispositivo específico puede intentar recuperarse del \_ \_ \_ error invalidado del dispositivo AUDCLNT E, como se indica a continuación:

1.  Libere la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) y cualquier otra interfaz WASAPI que haya adquirido en el dispositivo.
2.  Intenta activar una interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) en el mismo dispositivo.
3.  Si se produce un error en el paso 2, la aplicación puede, opcionalmente, pedir al usuario que seleccione otro dispositivo.

El paso 2 puede realizarse correctamente si el dispositivo que usa la aplicación se ha reconfigurado pero no se ha deshabilitado o quitado. Si se realiza correctamente, el paso 2 permite que la aplicación siga usando automáticamente el mismo dispositivo sin necesidad de que el usuario intervenga. El paso 3 es adecuado si la aplicación permite al usuario seleccionar otro dispositivo explícitamente después de que el usuario haya deshabilitado o quitado el dispositivo usado anteriormente.

Una aplicación puede determinar con mayor precisión la causa de un error de dispositivo no válido al registrarse para recibir una notificación cuando una sesión pierde su conexión con un dispositivo. Para habilitar esta notificación, la aplicación implementa una interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) y llama al método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrar la interfaz. Cuando un error de dispositivo no válido hace que se desconecte la sesión, WASAPI llama al método [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) en la interfaz registrada. A través de este método, WASAPI informa a la aplicación de la razón de la desconexión. En Windows Vista, la llamada a **OnSessionDisconnected** identifica los siguientes motivos:

-   El usuario quitó el dispositivo de punto de conexión de audio.
-   El servicio audio de Windows se ha cerrado.
-   El formato de flujo preferido cambió para el dispositivo al que está conectada la sesión de audio.
-   El usuario cerró la sesión de Windows Terminal Services (WTS) en la que se estaba ejecutando la sesión de audio. Para obtener más información acerca de las sesiones de WTS, consulte la documentación de Windows SDK.
-   La sesión de WTS en la que se estaba ejecutando la sesión de audio estaba desconectada.
-   La sesión de audio (modo compartido) se desconectó para que el dispositivo de extremo de audio esté disponible para una conexión de modo exclusivo.

En respuesta al evento de desconexión, WASAPI cierra todas las secuencias que pertenecen a la sesión. Si una aplicación intenta posteriormente acceder a un flujo cerrado a través de un método WASAPI como [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding), entonces se produce un error en el método y se devuelve el código de error AUDCLNT \_ E \_ \_ invalidado.

Una ventaja adicional para recibir notificaciones a través de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) es que las notificaciones llegan de forma asincrónica. Por lo tanto, aunque la secuencia no se esté ejecutando, la aplicación seguirá recibiendo notificaciones oportunas de errores de dispositivo no válidos que pueden impedir la ejecución de la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> </dl>

 

 



