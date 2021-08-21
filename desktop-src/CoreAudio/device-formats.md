---
description: Formatos de dispositivo
ms.assetid: 591437e4-21ef-42f1-a752-7f50440cbd63
title: Formatos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332f3ecd4b30213328552077bdef040a63e31992deaf217b77838dd0cd0797f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957344"
---
# <a name="device-formats"></a>Formatos de dispositivo

Para una aplicación de audio, una ventaja de usar una API de audio de nivel superior, como Direct Sound o las funciones **waveOutXxx** multimedia de Windows, es que la API convierte automáticamente entre los formatos de secuencia usados por la aplicación y los formatos usados por el dispositivo de audio. Por el contrario, las API de audio principales son más restrictivas porque requieren que las secuencias de la aplicación usen formatos que son iguales o están estrechamente relacionados con los formatos que usa el dispositivo. Por lo tanto, es posible que las aplicaciones que usan las API de audio principales para reproducir o grabar secuencias de audio sean necesarias para realizar algunas o todas las conversiones entre formatos de secuencia.

Una aplicación que usa WASAPI para administrar secuencias en modo compartido puede basarse en el motor de audio para realizar solo conversiones de formato limitadas. El motor de audio puede convertir entre un tamaño de muestra de PCM estándar utilizado por la aplicación y las muestras de punto flotante que el motor usa para su procesamiento interno. Sin embargo, el formato de una secuencia de aplicación normalmente debe tener el mismo número de canales y la misma frecuencia de muestreo que el formato de secuencia usado por el dispositivo.

Si una aplicación usa un dispositivo en modo exclusivo, la aplicación debe usar un formato de secuencia que el hardware de audio admita explícitamente. En modo exclusivo, la aplicación y el dispositivo intercambian datos de audio directamente, sin intervención del motor de audio.

Muchos dispositivos de audio admiten formatos de secuencia PCM y no PCM. Sin embargo, el motor de audio solo puede mezclar secuencias PCM. Por lo tanto, solo las secuencias en modo exclusivo pueden tener formatos que no son PCM. Además, solo se admiten formatos que no son PCM con velocidades de datos fijas en modo exclusivo. Un ejemplo de un formato de velocidad fija que no es PCM es una secuencia de audio Windows Media Audio Professional (WMA Pro) de 48 kHz que pasa a través de un vínculo de interfaz digital (S/PDIF) en formato digital sin descodificarse. Para obtener más información sobre el uso de secuencias Pro WMA a través de S/PDIF, consulte la siguiente documentación:

-   La descripción de la etiqueta de formato de onda WAVE FORMAT WMA SPDIF en la \_ documentación Windows \_ \_ DDK.
-   Las white paper tituladas "Audio Driver Support for the WMA Pro-over-S/PDIF Format" (Compatibilidad del controlador de audio para el formato de WMA Pro sobre S/PDIF) en el sitio web de [Audio Device Technologies for Windows.](https://www.microsoft.com/whdc/device/audio/default.mspx)

WASAPI usa una **estructura DE FORMASONATEX** **o FORMADETEXTENSIBLE** para especificar un formato de secuencia. Una **estructura DESATEXTENSIBLE** es efectivamente una estructura **DE FORMA DEDATOSTEX** que se ha ampliado para describir una mayor variedad de formatos. Cualquier formato que se pueda describir mediante una estructura **DE FORMA DESATEX** independiente también se puede describir mediante una **estructura DE FORMADETEXTENSIBLE.**

El primer miembro de la estructura **DESATEXTENSIBLE es** **una estructura DE FORMADETEATEX.** El contenido de una estructura **DE DESATEX** indica si se trata de una estructura **DE FORMA DESATEX** independiente o parte de una estructura **DESATEXTENSIBLE.**

Una estructura **STANDATEX** independiente puede describir adecuadamente un formato con uno o dos canales y un tamaño de muestra que es un múltiplo de 8 bits. Por sí misma, una **estructura DESATEX NO** puede especificar la asignación de canales a las posiciones del hablante. Además, aunque **ESTAMÁTEX** especifica el tamaño del contenedor para cada muestra de audio, no puede especificar el número de bits de precisión en una muestra (por ejemplo, 20 bits de precisión en un contenedor de 24 bits). Por el contrario, la estructura **DESATEXTENSIBLE puede** especificar tanto la asignación de canales a los hablantes como el número de bits de precisión de cada muestra.

Para obtener más información acerca **de LA FORMADETEATEX** **y DESATEXTENSIBLE,** consulte la documentación Windows DDK.

A partir de Windows 7, SE HA AMPLIADO **LA FORMADETEXTENSIBLE** para representar formatos de dispositivo para transmitir audio codificado a través de una interfaz compatible con IEC 61937. Para obtener información sobre la nueva estructura, vea [Representing Formats for IEC 61937 Transmissions](representing-formats-for-iec-61937-transmissions.md).

### <a name="specifying-the-device-format"></a>Especificar el formato de dispositivo

Los siguientes métodos WASAPI usan las estructuras **DE FORMASONATEX** **y DESATEXTENSIBLE** para describir los formatos de secuencia:

-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)
-   [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

El **método GetMixFormat** recupera el formato de secuencia que usa el motor de audio para su procesamiento interno de secuencias en modo compartido. El método siempre usa una **estructura DESATEXTENSIBLE,** en lugar de una estructura **STANDATEX** independiente, para especificar el formato.

El **método IsFormatSupported** indica si un dispositivo de punto de conexión de audio admite un formato de secuencia determinado. El autor de la llamada debe especificar si el formato de secuencia está pensado para su uso en modo compartido o en modo exclusivo. En el caso de los formatos de modo compartido, el método consulta el motor de audio para determinar si admite el formato especificado. Para los formatos de modo exclusivo, el método consulta el controlador de dispositivo. Algunos controladores de dispositivos informan de que admiten un formato PCM de 1 o 2 canales si el formato se especifica mediante una estructura **de FORMATEMAATEX** independiente, pero rechazarán el mismo formato si se especifica mediante una estructura **DESANTEXTENSIBLE.** Para obtener resultados confiables de estos controladores, las aplicaciones en modo exclusivo deben llamar a **IsFormatSupported** dos veces para cada formato PCM de 1 o 2 canales: una llamada debe usar una estructura **DE FORMATEATEX** independiente para especificar el formato y la otra llamada debe usar una estructura **DE 1** o 2 canales para especificar el mismo formato.

Una vez que una aplicación ha usado **GetMixFormat** o **IsFormatSupported** para buscar un formato adecuado para una secuencia en modo compartido o en modo exclusivo, la aplicación puede llamar al método **Initialize** para inicializar una secuencia con ese formato. Es probable que una aplicación que intente inicializar una secuencia en modo compartido con un formato que no sea idéntico al formato de combinación obtenido del método **GetMixFormat,** pero que tenga el mismo número de canales y la misma frecuencia de muestreo que el formato de combinación, sea correcta. Antes de **llamar a Initialize**, la aplicación puede llamar a **IsFormatSupported** para comprobar que **Initialize** aceptará el formato.

El formato de combinación que usa el motor de audio para su procesamiento interno de secuencias en modo compartido está estrechamente relacionado con el formato de secuencia que usa el dispositivo de punto de conexión de audio en modo compartido, pero no es necesariamente idéntico al formato de secuencia. A través Windows panel de control multimedia, Mmsys.cpl, el usuario puede seleccionar el formato de secuencia que usará un dispositivo de punto de conexión de audio cuando funcione en modo compartido. Los pasos son los siguientes:

1.  Para ejecutar Mmsys.cpl, abra una ventana del símbolo del sistema y escriba el siguiente comando:

    **control mmsys.cpl**

    Como alternativa, puede ejecutar Mmsys.cpl haciendo clic con el botón derecho en el icono del altavoz en el área  de notificación, que se encuentra en el lado derecho de la barra de tareas, y seleccionando Dispositivos de reproducción o Grabación de **dispositivos**.

2.  Una vez Mmsys.cpl ventana, seleccione un dispositivo de la lista de dispositivos de reproducción o de la lista de dispositivos de grabación y haga clic en **Propiedades.**
3.  Cuando se abra la ventana de propiedades, haga clic **en Avanzadas** y seleccione un formato de la lista de formatos disponibles en el cuadro con la etiqueta **Formato predeterminado**.

Por ejemplo, suponga que el usuario selecciona el siguiente formato predeterminado de la lista de formatos disponibles para un dispositivo de reproducción:

**2 canales, 16 bits, 44100 Hz (calidad de CD)**

Este es el formato que el dispositivo usará posteriormente cuando funcione en modo compartido. En Windows Vista, el motor de audio usará una versión ligeramente modificada de este formato para su procesamiento interno de secuencias en modo compartido. El motor de audio usará un formato con el mismo número de canales (dos) y la misma frecuencia de muestreo (44100 Hz), pero convertirá las muestras en números de punto flotante antes de procesarlos. El motor de audio convertirá los ejemplos de punto flotante de la combinación de salida en enteros de 16 bits antes de reproducirlos a través del dispositivo.

Una aplicación puede consultar la propiedad [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md) de un dispositivo de punto de conexión de audio para obtener el formato de modo compartido que el usuario ha seleccionado para el dispositivo. Para obtener información sobre cómo consultar las propiedades de un dispositivo, vea [Propiedades del dispositivo.](device-properties.md)

Algunas aplicaciones podrían encontrar el formato especificado por la propiedad **PKEY \_ AudioEngine \_ DeviceFormat** de un dispositivo como un formato adecuado para abrir una secuencia en modo exclusivo en el dispositivo. Otras aplicaciones que administran secuencias en modo exclusivo pueden tener requisitos adicionales que exigen una negociación de formato compleja con el dispositivo. Normalmente, una de estas aplicaciones crea una lista de formatos adecuados, con los formatos preferidos al principio de la lista. A continuación, la aplicación llama iterativamente a **IsFormatSupported** con cada formato sucesivo de la lista, comenzando al principio de la lista, hasta que encuentra un formato compatible con el dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



