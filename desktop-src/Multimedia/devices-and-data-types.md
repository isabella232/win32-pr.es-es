---
title: Dispositivos y tipos de datos
description: Dispositivos y tipos de datos
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- audio de onda, abrir dispositivos de salida
- 'onda: interfaz de audio, abrir dispositivos de salida'
- apertura de los dispositivos de salida de audio de onda
- audio de onda, consulta de dispositivos de salida
- 'onda: interfaz de audio, consulta de dispositivos de salida'
- consultar los dispositivos de salida de onda-audio
- audio de la onda, identificadores de dispositivo
- 'onda: interfaz de audio y controladores de dispositivo'
- audio de la onda, identificadores de dispositivo
- 'onda: interfaz de audio, identificadores de dispositivo'
- audio de la onda, tipos de datos de salida
- 'onda: interfaz de audio, tipos de datos de salida'
- audio de una onda, formatos de datos
- 'onda: interfaz de audio, formatos de datos'
- escribir datos de audio de onda
- audio de onda, escritura de datos
- 'onda: interfaz de audio, escritura de datos'
- Onda PCM-datos de audio
- audio de una onda, datos PCM
- 'onda: interfaz de audio, datos PCM'
- audio de onda, cerrar dispositivos de salida
- 'onda: interfaz de audio, cierre de dispositivos de salida'
- 'cerrar la onda: dispositivos de salida de audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29561a74695fb8bde950e2e75a430803a1a0351b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651368"
---
# <a name="devices-and-data-types"></a>Dispositivos y tipos de datos

En esta sección se describe cómo trabajar con dispositivos de audio de forma de onda y se incluye información sobre cómo abrirlos, cerrarlos y consultarlos en busca de sus capacidades. También se describe cómo realizar un seguimiento de los dispositivos de un sistema mediante el uso de identificadores de dispositivo e identificadores de dispositivo.

## <a name="opening-waveform-audio-output-devices"></a>Apertura de Waveform-Audio dispositivos de salida

Use la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir un dispositivo de salida de onda y audio para la reproducción. Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador de una ubicación de memoria especificada.

Algunos equipos multimedia tienen varios dispositivos de salida de onda-audio. A menos que desee abrir un dispositivo de salida de onda de onda específico en un sistema, debe usar la \_ marca del asignador de onda para el identificador de dispositivo al abrir un dispositivo. La función **waveOutOpen** elige el dispositivo en el sistema que es mejor capaz de reproducir el formato de datos especificado.

## <a name="querying-audio-devices"></a>Consultar dispositivos de audio

Windows proporciona las siguientes funciones para determinar el número de dispositivos de un tipo determinado que están disponibles en un sistema.



| Función                                       | Descripción                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Recupera el número de dispositivos de salida auxiliares presentes en el sistema.      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Recupera el número de dispositivos de entrada de audio de onda presentes en el sistema.  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Recupera el número de dispositivos de salida de onda y audio presentes en el sistema. |



 

Los dispositivos de audio se identifican mediante un identificador de dispositivo. El identificador de dispositivo se determina implícitamente a partir del número de dispositivos presentes en un sistema. Los identificadores de dispositivo van desde cero hasta uno menos que el número de dispositivos presentes. Por ejemplo, si hay dos dispositivos de salida de onda-audio en un sistema, los identificadores de dispositivo válidos son 0 y 1.

Después de determinar el número de dispositivos de un tipo determinado que están presentes en un sistema, puede usar una de las siguientes funciones para consultar las capacidades de cada dispositivo.



| Función                                       | Descripción                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Recupera las capacidades de un dispositivo de salida auxiliar especificado.      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Recupera las capacidades de un dispositivo de entrada de onda-audio especificado.  |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Recupera las capacidades de un dispositivo de salida de onda-audio especificado. |



 

Cada una de estas funciones rellena una estructura con información sobre las capacidades de un dispositivo especificado. En la tabla siguiente se enumeran las estructuras que corresponden a cada una de estas funciones.



|                                                |                                    |
|------------------------------------------------|------------------------------------|
| Función                                       | Estructura                          |
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

Los formatos estándar se enumeran en el miembro **dwFormats** de la estructura **WAVEOUTCAPS** . Los dispositivos de audio de onda pueden admitir formatos no estándar. Para determinar si un dispositivo admite un formato determinado (estándar o no estándar), puede llamar a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) con la marca de consulta de formato de onda \_ \_ . Esta marca no abre el dispositivo. El formato en cuestión se especifica en la estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) señalada por el parámetro *Pwfx* pasado a **waveOutOpen**.

La función de onda: los dispositivos de salida de audio varían en función de las capacidades que admiten. El miembro **dwSupport** de la estructura [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) indica si un dispositivo admite tales capacidades como cambios de volumen y de tono.

## <a name="device-handles-and-device-identifiers"></a>Identificadores de dispositivo e identificadores de dispositivo

Cada función que abre un dispositivo de audio especifica un identificador de dispositivo, un puntero a una ubicación de memoria y algunos parámetros que son únicos para cada tipo de dispositivo. La ubicación de memoria se rellena con un identificador de dispositivo. Use este identificador de dispositivo para identificar el dispositivo de audio abierto al llamar a otras funciones de audio.

La diferencia entre los identificadores y los identificadores de los dispositivos de audio es sutil pero importante:

-   Los identificadores de dispositivo se determinan implícitamente desde el número de dispositivos presentes en un sistema. Este número se obtiene mediante la función [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)o [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) .
-   Se devuelven los identificadores de dispositivo cuando se abren controladores de dispositivos mediante la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .

No hay funciones que abran o cierren dispositivos de audio auxiliares. Los dispositivos de audio auxiliares no deben abrirse y cerrarse como los dispositivos de audio de forma de onda porque no hay ninguna transferencia de datos continua asociada a ellos. Todas las funciones de audio auxiliares usan identificadores de dispositivo para identificar dispositivos.

## <a name="waveform-audio-output-data-types"></a>Waveform-Audio tipos de datos de salida

Los siguientes tipos de datos se definen para las funciones de salida de audio de onda.



| Tipo                                 | Descripción                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | Identificador de un dispositivo de salida de onda de audio abierto.                                                                                                               |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Estructura que especifica los formatos de datos admitidos por un dispositivo de entrada de audio de forma de onda determinado. Esta estructura también se usedfor los dispositivos de entrada de audio de forma de onda. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Estructura utilizada como encabezado para un bloque de datos de entrada de audio de forma de onda. Esta estructura también se utiliza para los dispositivos de entrada de audio de forma de onda.                            |
| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | Estructura usada para consultar las capacidades de un dispositivo de salida de onda de audio determinado.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Especificar formatos de datos de Waveform-Audio

Cuando llame a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir un controlador de dispositivo para la reproducción o para consultar si el controlador admite un formato de datos determinado, use el parámetro *pwfx* para especificar un puntero a una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que contenga el formato de datos de audio de forma de onda solicitado. **WAVEFORMATEX** sustituye a las estructuras [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) y [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) .

En el caso de los datos de audio que se separan en más de dos canales o tiene un tamaño de muestra que no es múltiplo de 8, debe utilizar [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible). Esta estructura simplemente configura los bytes adicionales a los que apunta el miembro **cbSize** de **WAVEFORMATEX** para proporcionar información adicional sobre el formato. **WAVEFORMATEXTENSIBLE** se puede convertir en **WAVEFORMATEX**.

También hay dos formatos de Portapapeles que puede usar para representar datos de audio: CF \_ Wave y CF \_ riff. Use el formato de onda de CF \_ para representar los datos en uno de los formatos estándar, como el PCM de 11 kHz o 22 kHz. Use el \_ formato CF riff para representar formatos de datos más complejos que no se pueden representar como archivos de audio de forma de onda estándar.

## <a name="writing-waveform-audio-data"></a>Escribir datos de Waveform-Audio

Después de abrir correctamente un controlador de dispositivo de salida de onda de audio, puede empezar a reproducir un sonido. Windows proporciona la función [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) para enviar bloques de datos a dispositivos de salida de onda-audio.

Use la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para especificar el bloque de datos de audio de onda que está enviando con **waveOutWrite**. Esta estructura contiene un puntero a un bloque de datos bloqueado, la longitud del bloque de datos y algunas marcas. Este bloque de datos debe estar preparado antes de usarlo; para obtener información sobre cómo preparar un bloque de datos, vea [bloques de datos de audio](audio-data-blocks.md).

Después de enviar un bloque de datos a un dispositivo de salida mediante **waveOutWrite**, debe esperar hasta que el controlador de dispositivo termine con el bloque de datos antes de liberarlo. Si va a enviar varios bloques de datos, debe supervisar la finalización de los bloques de datos para saber cuándo enviar bloques adicionales. Para obtener más información acerca de los bloques de datos, consulte [bloques de datos de audio](audio-data-blocks.md).

## <a name="pcm-waveform-audio-data-format"></a>Formato de datos de Waveform-Audio PCM

El miembro **lpData** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pointsetts a los ejemplos de datos de audio de onda. En el caso de los datos PCM de 8 bits, cada ejemplo se representa mediante un único byte de datos sin signo. Para los datos PCM de 16 bits, cada ejemplo se representa mediante un valor con signo de 16 bits. En la tabla siguiente se resumen los valores máximo, mínimo y punto medio de los datos de audio de onda y de onda PCM.



|             |                 |                  |                |
|-------------|-----------------|------------------|----------------|
| Formato de datos | Valor máximo   | Valor mínimo    | Valor de punto medio |
| PCM de 8 bits   | 255 (0xFF)      | 0                | 128 (0x80)     |
| PCM de 16 bits  | 32.767 (0x7FFF) | – 32.768 (0x8000) | 0              |



 

## <a name="pcm-data-packing"></a>Empaquetado de datos PCM

El orden de los bytes de datos varía entre los formatos de 8 y 16 bits, y entre los formatos mono y estéreo. En la lista siguiente se describe el empaquetado de datos para los distintos formatos de datos de audio de onda de onda PCM.



| Forma de onda PCM: formato de audio | Descripción                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mono de 8 bits                | Cada ejemplo es 1 byte que corresponde a un solo canal de audio. El ejemplo 1 va seguido de los ejemplos 2, 3, 4, etc.                                                                                                                                                                                                                           |
| estéreo de 8 bits              | Cada ejemplo tiene 2 bytes. El ejemplo 1 va seguido de los ejemplos 2, 3, 4, etc. Para cada ejemplo, el primer byte es el canal 0 (el canal izquierdo) y el segundo byte es el canal 1 (el canal derecho).                                                                                                                                               |
| mono de 16 bits               | Cada ejemplo tiene 2 bytes. El ejemplo 1 va seguido de los ejemplos 2, 3, 4, etc. En cada ejemplo, el primer byte es el byte de orden inferior del canal 0 y el segundo byte es el byte de orden superior del canal 0.                                                                                                                                         |
| estéreo de 16 bits             | Cada ejemplo es 4 bytes. El ejemplo 1 va seguido de los ejemplos 2, 3, 4, etc. En cada ejemplo, el primer byte es el byte de orden inferior del canal 0 (canal izquierdo). el segundo byte es el byte de orden superior del canal 0; el tercer byte es el byte de orden inferior del canal 1 (canal derecho). y el cuarto byte es el byte de orden superior del canal 1. |
| Otros                    | Cada ejemplo se encuentra en un bloque que es un múltiplo de 4 bytes, pero los ejemplos pueden no estar alineados por bytes. La organización de los canales se especifica mediante una máscara. Para obtener más información, vea [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>Cerrar Waveform-Audio dispositivos de salida

Después de completar la reproducción de la forma de onda, llame a [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) para cerrar el dispositivo de salida. Si se llama a **waveOutClose** mientras se reproduce un archivo de audio de forma de onda, se produce un error en la operación de cierre y la función devuelve un código de error que indica que el dispositivo no se cerró. Si no desea esperar a que finalice la reproducción antes de cerrar el dispositivo, llame a la función [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) antes de cerrar. Esto finaliza la reproducción y permite que el dispositivo se cierre. Asegúrese de usar la función [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) para limpiar la preparación en todos los bloques de datos antes de cerrar el dispositivo.

 

 