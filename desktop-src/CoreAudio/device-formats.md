---
description: Formatos de dispositivo
ms.assetid: 591437e4-21ef-42f1-a752-7f50440cbd63
title: Formatos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcd1b611075191e522cf00d959f120abfb3baa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152750"
---
# <a name="device-formats"></a>Formatos de dispositivo

En el caso de una aplicación de audio, una ventaja de usar una API de audio de nivel superior, como DirectSound o las funciones de **waveOutXxx** multimedia de Windows, es que la API se convierte automáticamente entre los formatos de flujo usados por la aplicación y los formatos usados por el dispositivo de audio. Por el contrario, las API de audio principales son más restrictivas porque requieren que los flujos de aplicaciones utilicen formatos que son iguales que los formatos usados por el dispositivo, o están estrechamente relacionados con ellos. Por lo tanto, las aplicaciones que usan las API de audio principales para reproducir o grabar secuencias de audio pueden ser necesarias para realizar algunas o todas las conversiones entre formatos de secuencia.

Una aplicación que usa WASAPI para administrar secuencias en modo compartido puede basarse en el motor de audio para realizar solo conversiones de formato limitado. El motor de audio puede realizar la conversión entre un tamaño de ejemplo PCM estándar utilizado por la aplicación y los ejemplos de punto flotante que el motor utiliza para su procesamiento interno. Sin embargo, el formato de una secuencia de aplicación normalmente debe tener el mismo número de canales y la misma velocidad de muestra que el formato de secuencia que usa el dispositivo.

Si una aplicación usa un dispositivo en modo exclusivo, la aplicación debe usar un formato de secuencia que el hardware de audio admita explícitamente. En el modo exclusivo, la aplicación y el dispositivo intercambian datos de audio directamente, sin intervención del motor de audio.

Muchos dispositivos de audio admiten formatos de secuencias PCM y no PCM. Sin embargo, el motor de audio solo puede mezclar flujos PCM. Por lo tanto, solo los flujos de modo exclusivo pueden tener formatos que no sean PCM. Además, solo se admiten en modo exclusivo formatos no PCM con velocidades de datos fijas. Un ejemplo de un formato no PCM de velocidad fija es una secuencia de audio 48-kHz Windows Media Audio Professional (WMA Pro) que pasa a través de un vínculo de interfaz digital (S/PDIF) de Sony/Philips en formato digital sin descodificarse. Para obtener más información sobre el uso de secuencias de Pro WMA a través de S/PDIF, consulte la siguiente documentación:

-   La descripción de la etiqueta de formato de onda \_ \_ WMA \_ SPDIF Format en la documentación de Windows DDK.
-   Las notas del producto titulada "compatibilidad con controladores de audio para el formato WMA Pro-over-S/PDIF" en el sitio Web [de tecnologías de dispositivos de audio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

WASAPI usa una estructura **WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE** para especificar un formato de flujo. Una estructura **WAVEFORMATEXTENSIBLE** es, de hecho, una estructura **WAVEFORMATEX** que se ha ampliado para describir un mayor intervalo de formatos. Cualquier formato que se pueda describir mediante una estructura **WAVEFORMATEX** independiente también se puede describir mediante una estructura **WAVEFORMATEXTENSIBLE** .

El primer miembro de la estructura **WAVEFORMATEXTENSIBLE** es una estructura **WAVEFORMATEX** . El contenido de una estructura **WaveFormatEx** indica si es una estructura de **WaveFormatEx** independiente o una parte de una estructura **WAVEFORMATEXTENSIBLE** .

Una estructura de **WAVEFORMATEX** independiente puede describir adecuadamente un formato con uno o dos canales y un tamaño de muestra que es un múltiplo de 8 bits. Por sí sola, una estructura **WAVEFORMATEX** no puede especificar la asignación de canales a las posiciones del orador. Además, aunque **WAVEFORMATEX** especifica el tamaño del contenedor para cada ejemplo de audio, no puede especificar el número de bits de precisión en un ejemplo (por ejemplo, 20 bits de precisión en un contenedor de 24 bits). Por el contrario, la estructura **WAVEFORMATEXTENSIBLE** puede especificar la asignación de canales a los altavoces y el número de bits de precisión en cada ejemplo.

Para obtener más información acerca de **WAVEFORMATEX** y **WAVEFORMATEXTENSIBLE**, consulte la documentación de DDK de Windows.

A partir de Windows 7, **WAVEFORMATEXTENSIBLE** se ha ampliado para representar formatos de dispositivo para transmitir audio codificado sobre una interfaz compatible con IEC 61937. Para obtener información sobre la nueva estructura, vea [representar formatos para transmisiones IEC 61937](representing-formats-for-iec-61937-transmissions.md).

### <a name="specifying-the-device-format"></a>Especificar el formato del dispositivo

Los siguientes métodos de WASAPI usan las estructuras **WAVEFORMATEX** y **WAVEFORMATEXTENSIBLE** para describir los formatos de flujo:

-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)
-   [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

El método **GetMixFormat** recupera el formato de secuencia que usa el motor de audio para su procesamiento interno de flujos de modo compartido. El método siempre usa una estructura **WAVEFORMATEXTENSIBLE** , en lugar de una estructura **WAVEFORMATEX** independiente, para especificar el formato.

El método **IsFormatSupported** indica si un dispositivo de punto de conexión de audio admite un formato de flujo determinado. El autor de la llamada debe especificar si el formato del flujo está pensado para su uso en modo compartido o en modo exclusivo. En el caso de los formatos de modo compartido, el método consulta el motor de audio para determinar si admite el formato especificado. En el caso de los formatos de modo exclusivo, el método consulta el controlador de dispositivo. Algunos controladores de dispositivos informarán de que admiten un formato PCM de 1 o 2 canales si el formato se especifica mediante una estructura de **WAVEFORMATEX** independiente, pero rechazará el mismo formato si se especifica mediante una estructura **WAVEFORMATEXTENSIBLE** . Para obtener resultados confiables de estos controladores, las aplicaciones en modo exclusivo deben llamar a **IsFormatSupported** dos veces para cada formato PCM de 1 canal o de 2 canales; una llamada debe usar una estructura de **WAVEFORMATEX** independiente para especificar el formato y la otra llamada debe usar una estructura **WAVEFORMATEXTENSIBLE** para especificar el mismo formato.

Después de que una aplicación ha usado **GetMixFormat** o **IsFormatSupported** para encontrar un formato adecuado para un flujo en modo compartido o en modo exclusivo, la aplicación puede llamar al método **Initialize** para inicializar una secuencia con ese formato. Una aplicación que intenta inicializar una secuencia en modo compartido con un formato que no es idéntico al formato de combinación obtenido del método **GetMixFormat** , pero que tiene el mismo número de canales y la misma velocidad de muestra que el formato de combinación, es probable que tenga éxito. Antes de llamar a **Initialize**, la aplicación puede llamar a **IsFormatSupported** para comprobar que **Initialize** aceptará el formato.

El formato de combinación que usa el motor de audio para su procesamiento interno de flujos de modo compartido está estrechamente relacionado con el formato de secuencia que el dispositivo de punto de conexión de audio usa en modo compartido, pero no necesariamente idéntico a él. A través del panel de control multimedia de Windows, Mmsys.cpl, el usuario puede seleccionar el formato de secuencia que usará un dispositivo de extremo de audio cuando funcione en modo compartido. Los pasos son los siguientes:

1.  Para ejecutar Mmsys.cpl, abra una ventana del símbolo del sistema y escriba el siguiente comando:

    **mmsys.cplde control**

    Como alternativa, puede ejecutar Mmsys.cpl haciendo clic con el botón secundario en el icono de altavoz en el área de notificación, que se encuentra en el lado derecho de la barra de tareas, y seleccionando **dispositivos de reproducción** o **dispositivos de grabación**.

2.  Una vez que se abra la ventana de Mmsys.cpl, seleccione un dispositivo de la lista de dispositivos de reproducción o de la lista de dispositivos de grabación y haga clic en **propiedades**.
3.  Cuando se abra la ventana Propiedades, haga clic en **Opciones avanzadas** y seleccione un formato en la lista de formatos disponibles en el cuadro con la etiqueta **formato predeterminado**.

Por ejemplo, supongamos que el usuario selecciona el siguiente formato predeterminado en la lista de formatos disponibles para un dispositivo de reproducción:

**2 canales, 16 bits, 44100 Hz (calidad de CD)**

Este es el formato que el dispositivo usará posteriormente cuando funcione en modo compartido. En Windows Vista, el motor de audio usará una versión ligeramente modificada de este formato para su procesamiento interno de flujos en modo compartido. El motor de audio usará un formato con el mismo número de canales (dos) y la misma velocidad de muestra (44100 Hz), pero convertirá los ejemplos en números de punto flotante antes de procesarlos. El motor de audio convertirá los ejemplos de punto flotante de la combinación de salida en enteros de 16 bits antes de reproducirlos a través del dispositivo.

Una aplicación puede consultar la propiedad [**PKEY \_ Audioengine \_ DeviceFormat**](pkey-audioengine-deviceformat.md) de un dispositivo de punto de conexión de audio para obtener el formato de modo compartido que el usuario ha seleccionado para el dispositivo. Para obtener información sobre cómo consultar las propiedades de un dispositivo, consulte [propiedades del dispositivo](device-properties.md).

Es posible que algunas aplicaciones encuentren el formato especificado por la propiedad **PKEY \_ Audioengine \_ DeviceFormat** de un dispositivo como un formato adecuado para abrir una secuencia de modo exclusivo en el dispositivo. Otras aplicaciones que administran secuencias en modo exclusivo pueden tener requisitos adicionales que exijan una negociación de formato complejo con el dispositivo. Normalmente, una de estas aplicaciones crea una lista de formatos adecuados, con los formatos preferidos al principio de la lista. A continuación, la aplicación llama a **IsFormatSupported** de forma iterativa con cada formato sucesivo de la lista, empezando por el principio de la lista, hasta que encuentre un formato que admita el dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



