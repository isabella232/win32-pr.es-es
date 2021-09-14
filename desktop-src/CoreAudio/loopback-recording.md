---
description: Grabación de bucles bucles
ms.assetid: 71c567f7-fffa-4b75-897a-63ed30c4c9b0
title: Grabación de bucles bucles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374da7497096118905f5e4c79bbacda832a42a7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164953"
---
# <a name="loopback-recording"></a>Grabación de bucles bucles

En el modo de bucle atrás, un cliente de WASAPI puede capturar la secuencia de audio que reproduce un dispositivo de punto de conexión de representación. Para abrir una secuencia en modo de bucle atrás, el cliente debe:

-   Obtenga una interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) para el dispositivo de punto de conexión de representación.
-   Inicialice una secuencia de captura en modo de bucle atrás en el dispositivo del punto de conexión de representación.

Después de seguir estos pasos, el cliente puede llamar al método [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) para obtener una [**interfaz IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) en el dispositivo del punto de conexión de representación.

WASAPI proporciona el modo de bucle atrás principalmente para admitir la cancelación de eco acústico (AEC). Sin embargo, otros tipos de aplicaciones de audio pueden resultar útiles para capturar la combinación del sistema que reproduce el motor de audio.

En el ejemplo de código de [Captura de](capturing-a-stream.md)una secuencia , la función RecordAudioStream se puede modificar fácilmente para configurar una secuencia de captura en modo de bucleback. Las modificaciones necesarias son:

-   En la llamada al método [**IMMDeviceEnumerator::GetDefaultAudioEndpoint,**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) cambie el primer parámetro (*dataFlow*) de eCapture a eRender.
-   En la llamada al método [**IAudioClient::Initialize,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) cambie el valor del segundo parámetro (*StreamFlags*) de 0 a AUDCLNT \_ STREAMFLAGS \_ LOOPBACK.

En versiones de Windows anteriores a Windows 10 1703, el cliente de captura de modo de extracción no recibe ningún evento cuando una secuencia se inicializa con el almacenamiento en búfer controlado por eventos y está habilitado para bucles bucles. Para evitarlo, inicialice una secuencia de representación en modo controlado por eventos. Cada vez que el cliente recibe un evento para la secuencia de representación, debe indicar al cliente de captura que ejecute el subproceso de captura que lee el siguiente conjunto de ejemplos del búfer del punto de conexión de captura. En Windows 10 versiones 1703 y posteriores, se admiten clientes de bucles atrás controlados por eventos y ya no necesitan la solución alternativa que implica la secuencia de representación.  

Un cliente puede habilitar el modo de bucle atrás solo para una secuencia en modo compartido (AUDCLNT \_ SHAREMODE \_ SHARED). Las secuencias en modo exclusivo no pueden funcionar en modo de bucle atrás.

La implementación del bucle de recuperación mediante WASAPI depende de las funcionalidades del hardware. Si el hardware admite un pin de bucle atrás en el punto de conexión de representación, WASAPI usa el audio proporcionado en este pin para la secuencia de bucles. Cuando el hardware no admite un pin de bucle atrás, WASAPI copia el flujo de salida del motor de audio en el búfer de captura de la aplicación de bucles bucles, además de copiar los datos de audio en el pin de representación del hardware.

Algunos proveedores de hardware implementan dispositivos de bucleback (en lugar de anclar instancias en dispositivos de representación) en sus adaptadores de audio. Aunque los dispositivos de bucle recuperación de hardware son similares en funcionamiento al modo de bucle atrás WASAPI, pueden ser más difíciles de usar.

Los dispositivos de bucle de retorno de hardware tienen las siguientes desventajas para las aplicaciones de audio:

-   No todos los adaptadores de audio tienen dispositivos de bucle atrás. Por lo tanto, las aplicaciones que dependen de ellas no funcionarán en todos los sistemas.
-   Antes de que una aplicación pueda grabar desde un dispositivo de bucle atrás, el usuario debe identificar el dispositivo de bucle atrás y habilitarlo para su uso.

Distintos proveedores asignan nombres diferentes a sus dispositivos de bucles de recuperación de hardware. Los nombres siguientes son ejemplos:

-   Combinación estéreo
-   Combinación de onda
-   Salida mixta
-   Lo que se escucha

La falta de nombres estandarizados podría hacer que los usuarios tengan dificultades para identificar un dispositivo de bucle atrás en una lista de nombres de dispositivo.

Un dispositivo de bucle recuperación de hardware es un dispositivo de captura. Por lo tanto, si un adaptador admite un dispositivo de bucle atrás, una aplicación de audio puede grabar desde el dispositivo de la misma manera que lo hace desde cualquier otro dispositivo de captura.

Por ejemplo, si selecciona un dispositivo de bucle recuperación de hardware para que sea el dispositivo de captura predeterminado, puede usar la función RecordAudioStream (sin modificaciones) en el ejemplo de código de [Captura](capturing-a-stream.md) de una secuencia para capturar la secuencia del dispositivo. (También puede usar una API de audio heredada, como Windows funciones **waveInXxx** multimedia, para capturar la secuencia desde el dispositivo).

Si el adaptador de audio contiene un dispositivo de bucle atrás de hardware, puede usar el panel de control multimedia Windows, Mmsys.cpl, para designar el dispositivo como dispositivo de captura predeterminado. Los pasos son los siguientes:

1.  Para ejecutar Mmsys.cpl, abra una ventana del símbolo del sistema y escriba el siguiente comando:

    ```C++
    control mmsys.cpl,,1
    ```

    

    Como alternativa, puede ejecutar Mmsys.cpl haciendo clic con el botón derecho en el icono del hablante en el área de notificación, que se encuentra en el lado derecho de la barra de tareas, y seleccionando Grabar **dispositivos**.

2.  Una vez Mmsys.cpl ventana, haga clic con el botón derecho en  cualquier parte de la lista de dispositivos de grabación y compruebe que la opción Mostrar dispositivos deshabilitados está activada. (De lo contrario, si el dispositivo de bucle recuperación está deshabilitado, no aparecerá en la lista).
3.  Examine la lista de dispositivos de grabación para buscar el dispositivo de bucle recuperación (si existe). Si el dispositivo de bucle atrás está deshabilitado, para habilitarlo, haga clic con el botón derecho en el dispositivo y haga clic **en Habilitar**.
4.  Por último, para seleccionar el dispositivo de bucle atrás para que sea el dispositivo de captura predeterminado, haga clic con el botón derecho en el dispositivo y haga clic **en Establecer como dispositivo predeterminado.**

WASAPI admite la grabación de bucles bucles, independientemente de si el hardware de audio contiene un dispositivo de bucle atrás o si el usuario ha habilitado el dispositivo.

Windows Vista proporciona administración de derechos digitales (DRM). Los proveedores de contenido dependen de DRM para proteger su música de propiedad u otro contenido frente a copias no autorizadas y otros usos no autorizados. De forma similar, un controlador de audio de confianza no permite que un dispositivo de bucle atrás capture secuencias digitales que contengan contenido protegido. Windows Vista solo permite a los controladores de confianza reproducir contenido protegido. Para obtener más información sobre los controladores de confianza y DRM, consulte la documentación Windows DDK.

El bucleback WASAPI contiene la combinación de todo el audio que se reproduce, independientemente de la sesión de Terminal Services de la que se originó el audio. Por ejemplo, puede ejecutar un cliente de bucle atrás en un servicio que se ejecuta en la sesión 0 y capturar audio de todas las sesiones de usuario, así como audio que se reproduce desde la sesión 0.

Escritorio remoto permite redirigir el audio al cliente. Esto se implementa mediante la creación de nuevos dispositivos de audio que solo aparecen para esa sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> </dl>

 

 



