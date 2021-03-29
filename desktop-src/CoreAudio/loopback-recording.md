---
description: Grabación de bucle invertido
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: Grabación de bucle invertido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374da7497096118905f5e4c79bbacda832a42a7b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000718"
---
# <a name="loopback-recording"></a>Grabación de bucle invertido

En el modo de bucle invertido, un cliente de WASAPI puede capturar la secuencia de audio que reproduce un dispositivo de punto de conexión de representación. Para abrir un flujo en modo de bucle invertido, el cliente debe:

-   Obtenga una interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para el dispositivo de punto de conexión de representación.
-   Inicializa una secuencia de captura en modo de bucle invertido en el dispositivo de punto de conexión de representación.

Después de seguir estos pasos, el cliente puede llamar al método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) para obtener una interfaz [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) en el dispositivo de punto de conexión de representación.

WASAPI proporciona el modo de bucle invertido principalmente para admitir la cancelación del eco acústico (AEC). Sin embargo, otros tipos de aplicaciones de audio pueden encontrar el modo de bucle invertido útil para capturar la combinación del sistema que está reproduciendo por el motor de audio.

En el ejemplo de código de la [captura de una secuencia](capturing-a-stream.md), la función RecordAudioStream se puede modificar fácilmente para configurar una secuencia de captura en modo de bucle invertido. Las modificaciones necesarias son:

-   En la llamada al método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) , cambie el primer parámetro (*flujo de entrada*) de eCapture a eRender.
-   En la llamada al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , cambie el valor del segundo parámetro (*StreamFlags*) de 0 a AUDCLNT \_ StreamFlags \_ loopback.

En las versiones de Windows anteriores a Windows 10 1703, el cliente de captura de modo de extracción no recibe ningún evento cuando una secuencia se inicializa con el almacenamiento en búfer basado en eventos y está habilitada para bucles invertidos. Para evitar esto, inicialice una secuencia de representación en modo basado en eventos. Cada vez que el cliente recibe un evento para la secuencia de representación, debe indicar al cliente de captura que ejecute el subproceso de captura que lee el siguiente conjunto de muestras del búfer del extremo de captura. En las versiones 1703 y posteriores de Windows 10, se admiten clientes de bucle invertido orientados a eventos y ya no se necesita la solución que implique la secuencia de representación.  

Un cliente puede habilitar el modo de bucle invertido solo para un flujo en modo compartido (AUDCLNT \_ SHAREMODE \_ Shared). Los flujos de modo exclusivo no pueden funcionar en modo de bucle invertido.

La implementación de bucle invertido por WASAPI depende de las capacidades del hardware. Si el hardware admite un PIN de bucle invertido en el punto de conexión de representación, WASAPI usa el audio proporcionado en este pin para la secuencia de bucle invertido. Cuando el hardware no admite un PIN de bucle invertido, WASAPI copia el flujo de salida del motor de audio en el búfer de captura de la aplicación de bucle invertido, además de copiar los datos de audio en el PIN de representación del hardware.

Algunos proveedores de hardware implementan dispositivos de bucle invertido (en lugar de anclar instancias en dispositivos de representación) en sus adaptadores de audio. Aunque los dispositivos de bucle invertido de hardware tienen una operación similar en el modo de bucle invertido WASAPI, pueden ser más difíciles de usar.

Los dispositivos de bucle invertido de hardware tienen las siguientes desventajas para las aplicaciones de audio:

-   No todos los adaptadores de audio tienen dispositivos de bucle invertido. Por lo tanto, las aplicaciones que dependen de ellos no funcionarán en todos los sistemas.
-   Para que una aplicación pueda grabar desde un dispositivo de bucle invertido, el usuario debe identificar el dispositivo de bucle invertido y habilitarlo para su uso.

Distintos proveedores asignan nombres diferentes a sus dispositivos de bucle invertido de hardware. Los nombres siguientes son ejemplos:

-   Mezcla estéreo
-   Combinación de WaveOut
-   Salida mixta
-   Qué oye

La falta de nombres normalizados puede hacer que los usuarios tengan dificultades para identificar un dispositivo de bucle invertido en una lista de nombres de dispositivo.

Un dispositivo de bucle invertido de hardware es un dispositivo de captura. Por lo tanto, si un adaptador es compatible con un dispositivo de bucle invertido, una aplicación de audio puede grabar desde el dispositivo de la misma manera que se registra desde cualquier otro dispositivo de captura.

Por ejemplo, si selecciona un dispositivo de bucle invertido de hardware para que sea el dispositivo de captura predeterminado, puede usar la función RecordAudioStream (sin modificación) en el ejemplo de código en la [captura de una secuencia](capturing-a-stream.md) para capturar la secuencia desde el dispositivo. (También puede usar una API de audio heredada, como las funciones de **waveInXxx** multimedia de Windows, para capturar el flujo del dispositivo).

Si el adaptador de audio contiene un dispositivo de bucle invertido de hardware, puede usar el panel de control multimedia de Windows, Mmsys.cpl, para designar el dispositivo como el dispositivo de captura predeterminado. Los pasos son los siguientes:

1.  Para ejecutar Mmsys.cpl, abra una ventana del símbolo del sistema y escriba el siguiente comando:

    ```C++
    control mmsys.cpl,,1
    ```

    

    Como alternativa, puede ejecutar Mmsys.cpl haciendo clic con el botón secundario en el icono de altavoz en el área de notificación, que se encuentra en el lado derecho de la barra de tareas, y seleccionando **grabar dispositivos**.

2.  Una vez que se abra la ventana de Mmsys.cpl, haga clic con el botón secundario en cualquier parte de la lista de dispositivos de grabación y compruebe que la opción **Mostrar dispositivos deshabilitados** está activada. (De lo contrario, si el dispositivo de bucle invertido está deshabilitado, no aparecerá en la lista).
3.  Examine la lista de dispositivos de grabación para buscar el dispositivo de bucle invertido (si existe). Si el dispositivo de bucle invertido está deshabilitado, habilítelo haciendo clic con el botón secundario en el dispositivo y haciendo clic en **Habilitar**.
4.  Por último, para seleccionar el dispositivo de bucle invertido como dispositivo de captura predeterminado, haga clic con el botón derecho en el dispositivo y haga clic en **establecer como dispositivo predeterminado**.

WASAPI admite la grabación de bucle invertido independientemente de si el hardware de audio contiene un dispositivo de bucle invertido o si el usuario ha habilitado el dispositivo.

Windows Vista ofrece administración de derechos digitales (DRM). Los proveedores de contenido se basan en DRM para proteger su música de su propiedad u otro contenido de la copia no autorizada y otros usos no válidos. De forma similar, un controlador de audio de confianza no permite que un dispositivo de bucle invertido Capture secuencias digitales que contengan contenido protegido. Windows Vista solo permite a los controladores de confianza reproducir contenido protegido. Para obtener más información acerca de los controladores de confianza y DRM, consulte la documentación de DDK de Windows.

WASAPI loopback contiene la combinación de todo el audio que se está reproduciendo, independientemente de la sesión de Terminal Services de la que se originó el audio. Por ejemplo, puede ejecutar un cliente de bucle invertido en un servicio que se ejecuta en la sesión 0 y capturar audio de todas las sesiones de usuario, así como el audio que se reproduce desde la sesión 0.

Escritorio remoto permite redirigir el audio al cliente. Esto se implementa mediante la creación de nuevos dispositivos de audio que solo aparecen para esa sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> </dl>

 

 



