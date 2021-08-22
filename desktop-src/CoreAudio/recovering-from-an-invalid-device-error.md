---
description: Recuperación de un error Invalid-Device error
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: Recuperación de un error Invalid-Device error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9f56972aeeae5cfb370a656a621c6b6e206f8caa115bec33203cab7eded3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318565"
---
# <a name="recovering-from-an-invalid-device-error"></a>Recuperación de un error Invalid-Device error

Muchos de los métodos de WASAPI devuelven código de error AUDCLNT E DEVICE INVALIDATED si el dispositivo de punto de conexión de audio que usa la aplicación cliente \_ \_ deja de ser \_ válido. Este código de error indica que el dispositivo del punto de conexión se ha desconectado o que el hardware de audio o los recursos de hardware asociados se han reconfigurado, deshabilitado, quitado o dejado de estar disponible para su uso. Con frecuencia, la aplicación puede recuperarse de este error.

>[!NOTE]
> Para obtener información sobre cómo recuperarse de errores de dispositivo no válidos al usar las API de audio espacial (ISAC), consulte Recuperación de un error de Invalid-Device [(sonido espacial)](recovering-from-an-invalid-device-error-spatial-sound.md)

La estrategia que una aplicación debe usar para recuperarse de un error invalidado de AUDCLNT E DEVICE depende de cuál de las técnicas siguientes usa la aplicación para seleccionar un dispositivo de punto de \_ \_ conexión de \_ audio:

-   Seleccione siempre el dispositivo de representación o captura de audio predeterminado.
-   Seleccione un dispositivo de punto de conexión de audio específico.

En el último caso, la aplicación selecciona automáticamente un dispositivo específico en función de los requisitos internos o permite al usuario seleccionar explícitamente un dispositivo de una lista de dispositivos disponibles.

Una aplicación que usa el dispositivo predeterminado puede intentar recuperarse de un error invalidado de AUDCLNT \_ E DEVICE como se muestra a \_ \_ continuación:

1.  Libere la [**interfaz IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) y cualquier otra interfaz WASAPI que haya adquirido en el dispositivo.
2.  Llame al [**método IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener el dispositivo de audio predeterminado actual.
3.  Intente activar [**IAudioClient en**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) el dispositivo de audio predeterminado.

Al seguir los pasos anteriores, la aplicación tiende a responder correctamente independientemente de la causa del error invalidado de AUDCLNT \_ E \_ \_ DEVICE. Si la reconfiguración del dispositivo predeterminado produjo el error (por ejemplo, si el usuario cambió el formato de secuencia usado por el dispositivo), estos pasos, si se completan correctamente, permiten que la aplicación siga usando el mismo dispositivo. Si el usuario deshabilitó o quitó el dispositivo que usaba la aplicación y otro dispositivo está disponible para asumir el rol de dispositivo predeterminado, la aplicación puede continuar con el nuevo dispositivo predeterminado. En cualquier caso, la aplicación se adapta automáticamente sin necesidad de intervención del usuario.

Una aplicación que selecciona un dispositivo específico puede intentar recuperarse del error AUDCLNT \_ E \_ DEVICE \_ INVALIDATED como se muestra a continuación:

1.  Libere la [**interfaz IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) y cualquier otra interfaz WASAPI que haya adquirido en el dispositivo.
2.  Intente activar una [**interfaz IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) en el mismo dispositivo.
3.  Si se produce un error en el paso 2, la aplicación puede, como opción, solicitar al usuario que seleccione otro dispositivo.

El paso 2 puede realizarse correctamente si el dispositivo que usa la aplicación se ha reconfigurado, pero no se ha deshabilitado ni quitado. Si se realiza correctamente, el paso 2 permite que la aplicación siga usando automáticamente el mismo dispositivo sin necesidad de intervención del usuario. El paso 3 es adecuado si la aplicación permite al usuario seleccionar explícitamente otro dispositivo después de que el usuario haya deshabilitado o quitado el dispositivo usado anteriormente.

Una aplicación puede determinar de forma más precisa la causa de un error de dispositivo no válido si se registra para recibir una notificación cuando una sesión pierde su conexión a un dispositivo. Para habilitar esta notificación, la aplicación implementa una interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) y llama al método [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrar la interfaz. Cuando un error de dispositivo no válido hace que la sesión se desconecte, WASAPI llama al método [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) en la interfaz registrada. Mediante este método, WASAPI informa a la aplicación del motivo de la desconexión. En Windows Vista, la **llamada a OnSessionDisconnected** identifica los siguientes motivos:

-   El usuario quitó el dispositivo de punto de conexión de audio.
-   El Windows de audio se ha cerrado.
-   El formato de secuencia preferido ha cambiado para el dispositivo al que está conectada la sesión de audio.
-   El usuario ha cerrado la sesión Terminal Windows Services (WTS) en la que se estaba ejecutando la sesión de audio. Para más información sobre las WTS, consulte la documentación Windows SDK.
-   La WTS sesión en la que se estaba ejecutando la sesión de audio se desconectó.
-   La sesión de audio (modo compartido) se desconectó para que el dispositivo del punto de conexión de audio esté disponible para una conexión en modo exclusivo.

En respuesta al evento de desconexión, WASAPI cierra todas las secuencias que pertenecen a la sesión. Si posteriormente una aplicación intenta acceder a una secuencia cerrada a través de un método WASAPI como [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding), se produce un error en el método y devuelve el código de error AUDCLNT \_ E DEVICE \_ \_ INVALIDATED.

Una ventaja adicional de recibir notificaciones a través de [**la interfaz IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) es que las notificaciones llegan de forma asincrónica. Por lo tanto, incluso cuando el flujo no se está ejecutando, la aplicación seguirá recibiendo una notificación a tiempo de errores de dispositivo no válido que pueden impedir que se ejecute la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> </dl>

 

 



