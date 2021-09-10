---
title: Dispositivos y tipos de datos
description: Dispositivos y tipos de datos
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- audio de onda, abrir dispositivos de salida
- interfaz de audio de onda, abrir dispositivos de salida
- abrir dispositivos de salida de audio y forma de onda
- audio de onda, consulta de dispositivos de salida
- interfaz de audio de onda, consulta de dispositivos de salida
- consultar dispositivos de salida de audio de forma de onda
- audio de forma de onda, identificadores de dispositivo
- interfaz de audio de onda, identificadores de dispositivo
- audio de forma de onda, identificadores de dispositivo
- interfaz de audio de onda, identificadores de dispositivo
- audio de forma de onda, tipos de datos de salida
- interfaz de audio de forma de onda, tipos de datos de salida
- audio de forma de onda, formatos de datos
- interfaz de audio de forma de onda, formatos de datos
- escribir datos de audio de forma de onda
- audio de onda, escribir datos
- interfaz de audio de forma de onda, escribir datos
- Datos de audio y forma de onda de PCM
- audio de forma de onda, datos de PCM
- interfaz de audio de onda, datos de PCM
- audio de onda, cierre de dispositivos de salida
- interfaz de audio de onda, cierre de dispositivos de salida
- cerrar dispositivos de salida de audio y forma de onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2abe0c2c20c52f4498316fb619885d41f85e41d6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371210"
---
# <a name="devices-and-data-types"></a>Dispositivos y tipos de datos

En esta sección se describe cómo trabajar con dispositivos de audio de forma de onda e incluye información sobre cómo abrirlos, cerrarlos y consultar sus funcionalidades. También se describe cómo realizar un seguimiento de los dispositivos en un sistema mediante identificadores de dispositivo e identificadores de dispositivo.

## <a name="opening-waveform-audio-output-devices"></a>Apertura de Waveform-Audio de salida

Use la [**función waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir un dispositivo de salida de audio de forma de onda para la reproducción. Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador de una ubicación de memoria especificada.

Algunos equipos multimedia tienen varios dispositivos de salida de audio de forma de onda. A menos que desee abrir un dispositivo de salida de audio de forma de onda específico en un sistema, debe usar la marca WAVE MAPPER para el identificador de dispositivo al \_ abrir un dispositivo. La **función waveOutOpen** elige el dispositivo del sistema que mejor puede reproducir el formato de datos especificado.

## <a name="querying-audio-devices"></a>Consulta de dispositivos de audio

Windows proporciona las siguientes funciones para determinar cuántos dispositivos de un tipo determinado están disponibles en un sistema.



| Función                                       | Descripción                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Recupera el número de dispositivos de salida auxiliares presentes en el sistema.      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Recupera el número de dispositivos de entrada de audio de forma de onda presentes en el sistema.  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Recupera el número de dispositivos de salida de audio de forma de onda presentes en el sistema. |



 

Los dispositivos de audio se identifican mediante un identificador de dispositivo. El identificador de dispositivo se determina implícitamente a partir del número de dispositivos presentes en un sistema. Los identificadores de dispositivo oscilan entre cero y uno menos que el número de dispositivos presentes. Por ejemplo, si hay dos dispositivos de salida de audio de forma de onda en un sistema, los identificadores de dispositivo válidos son 0 y 1.

Después de determinar cuántos dispositivos de un tipo determinado están presentes en un sistema, puede usar una de las siguientes funciones para consultar las funcionalidades de cada dispositivo.



| Función                                       | Descripción                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Recupera las funciones de un dispositivo de salida auxiliar especificado.      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Recupera las funciones de un dispositivo de entrada de audio de forma de onda especificado.  |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Recupera las funcionalidades de un dispositivo de salida de audio de forma de onda especificado. |



 

Cada una de estas funciones rellena una estructura con información sobre las funcionalidades de un dispositivo especificado. En la tabla siguiente se enumeran las estructuras que corresponden a cada una de estas funciones.



|  Función                                              |  Estructura                                  |
|------------------------------------------------|------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

Los formatos estándar se enumeran en el **miembro dwFormats** de la **estructura WAVEOUTCAPS.** Los dispositivos de audio de onda pueden admitir formatos no estándar. Para determinar si un dispositivo admite un formato determinado (estándar o no estándar), puede llamar a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) con la marca WAVE \_ FORMAT \_ QUERY. Esta marca no abre el dispositivo. Especifique el formato en cuestión en la estructura [**DESATEX a**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) la que apunta el parámetro *pwfx* pasado **a waveOutOpen**.

Los dispositivos de salida de audio de onda varían en función de las funcionalidades que admiten. El **miembro dwSupport** de la [**estructura WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) indica si un dispositivo admite funcionalidades como cambios de volumen y tono.

## <a name="device-handles-and-device-identifiers"></a>Identificadores de dispositivo e identificadores de dispositivo

Cada función que abre un dispositivo de audio especifica un identificador de dispositivo, un puntero a una ubicación de memoria y algunos parámetros que son únicos para cada tipo de dispositivo. La ubicación de memoria se rellena con un identificador de dispositivo. Use este identificador de dispositivo para identificar el dispositivo de audio abierto al llamar a otras funciones de audio.

La diferencia entre los identificadores y los identificadores de los dispositivos de audio es sutil pero importante:

-   Los identificadores de dispositivo se determinan implícitamente a partir del número de dispositivos presentes en un sistema. Este número se obtiene mediante la función [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)o [**waveOutGetNumDevs.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)
-   Los identificadores de dispositivo se devuelven cuando se abren los controladores de dispositivo mediante la [**función waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) [**o waveOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)

No hay funciones que abran o cierren dispositivos de audio auxiliares. Los dispositivos de audio auxiliares no deben abrirse y cerrarse como dispositivos de audio de forma de onda porque no hay ninguna transferencia de datos continua asociada a ellos. Todas las funciones de audio auxiliares usan identificadores de dispositivo para identificar dispositivos.

## <a name="waveform-audio-output-data-types"></a>Waveform-Audio de datos de salida

Los siguientes tipos de datos se definen para las funciones de salida de audio de forma de onda.



| Tipo                                 | Descripción                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | Controle un dispositivo abierto de salida de audio de forma de onda.                                                                                                               |
| [**FORMA DE ONDAATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Estructura que especifica los formatos de datos admitidos por un dispositivo de entrada de audio de forma de onda determinado. Esta estructura también se usa para dispositivos de entrada de audio de forma de onda. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Estructura que se usa como encabezado para un bloque de datos de entrada de audio de forma de onda. Esta estructura también se usa para dispositivos de entrada de audio de forma de onda.                            |
| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | Estructura que se usa para consultar las funcionalidades de un dispositivo de salida de audio de forma de onda determinado.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Especificación de Waveform-Audio formatos de datos

Cuando se llama a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir un controlador de dispositivo para su reproducción o para consultar si el controlador admite un formato de datos determinado, use el parámetro *pwfx* para especificar un puntero a una estructura [**DETENTEATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) que contenga el formato de datos de audio de forma de onda solicitado. **WAVEATEX reemplaza** las estructuras [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) [**y PCMWAVEFORMAT.**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)

Para los datos de audio que están separados en más de dos canales o tienen un tamaño de muestra que no es un múltiplo de 8, debe usar [**FORMADEDATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible). Esta estructura simplemente configura los bytes adicionales a los que apunta el **miembro cbSize** de **LAATEX PARA** proporcionar información adicional sobre el formato. **SE puede convertir DE FORMADEDATOSTEXTENSIBLE** **como FORMA DE ONDAATEX.**

También hay dos formatos de Portapapeles que puede usar para representar datos de audio: CF \_ WAVE y CF \_ RIFF. Use el formato CF WAVE para representar los datos en uno de los formatos estándar, como PCM de \_ 11 kHz o 22 kHz. Use el formato CF RIFF para representar formatos de datos más complejos que no se pueden representar como archivos de audio de forma \_ de onda estándar.

## <a name="writing-waveform-audio-data"></a>Escribir Waveform-Audio datos

Después de abrir correctamente un controlador de dispositivo de salida de audio de forma de onda, puede empezar a reproducir un sonido. Windows proporciona la [**función waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) para enviar bloques de datos a dispositivos de salida de audio de forma de onda.

Use la [**estructura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para especificar el bloque de datos de audio de forma de onda que va a enviar mediante **waveOutWrite**. Esta estructura contiene un puntero a un bloque de datos bloqueado, la longitud del bloque de datos y algunas marcas. Este bloque de datos debe estar preparado antes de usarlo; Para obtener información sobre cómo preparar un bloque de datos, vea [Bloques de datos de audio](audio-data-blocks.md).

Después de enviar un bloque de datos a un dispositivo de salida mediante **waveOutWrite**, debe esperar hasta que el controlador de dispositivo finalice con el bloque de datos antes de liberarlo. Si va a enviar varios bloques de datos, debe supervisar la finalización de bloques de datos para saber cuándo enviar bloques adicionales. Para obtener más información sobre los bloques de datos, vea [Bloques de datos de audio](audio-data-blocks.md).

## <a name="pcm-waveform-audio-data-format"></a>Formato de datos de Waveform-Audio PCM

El **miembro lpData** de la [**estructura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) apunta a los ejemplos de datos de audio de forma de onda. En el caso de los datos pcm de 8 bits, cada muestra se representa mediante un solo byte de datos sin signo. Para los datos PCM de 16 bits, cada muestra se representa mediante un valor de 16 bits con firma. En la tabla siguiente se resumen los valores máximo, mínimo y punto medio para los datos de audio de forma de onda de PCM.



| Formato de datos | Valor máximo   | Valor mínimo    | Valor de punto medio |
|-------------|-----------------|------------------|----------------|
| PCM de 8 bits   | 255 (0xFF)      | 0                | 128 (0x80)     |
| PCM de 16 bits  | 32 767 (0x7FFF) | –32 768 (0x8000) | 0              |



 

## <a name="pcm-data-packing"></a>Empaquetado de datos de PCM

El orden de los bytes de datos varía entre los formatos de 8 y 16 bits y entre los formatos mono y estéreo. En la lista siguiente se describe el empaquetado de datos para los diferentes formatos de datos de audio de forma de onda de PCM.



| Formato de audio de forma de onda de PCM | Descripción                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mono de 8 bits                | Cada muestra es de 1 byte que corresponde a un único canal de audio. El ejemplo 1 va seguido de las muestras 2, 3, 4, y así sucesivamente.                                                                                                                                                                                                                           |
| Estéreo de 8 bits              | Cada muestra es de 2 bytes. El ejemplo 1 va seguido de las muestras 2, 3, 4, y así sucesivamente. Para cada ejemplo, el primer byte es el canal 0 (el canal izquierdo) y el segundo byte es el canal 1 (el canal derecho).                                                                                                                                               |
| Mono de 16 bits               | Cada muestra es de 2 bytes. El ejemplo 1 va seguido de las muestras 2, 3, 4, y así sucesivamente. Para cada ejemplo, el primer byte es el byte de orden bajo del canal 0 y el segundo byte es el byte de orden superior del canal 0.                                                                                                                                         |
| Estéreo de 16 bits             | Cada ejemplo es de 4 bytes. El ejemplo 1 va seguido de las muestras 2, 3, 4, y así sucesivamente. Para cada ejemplo, el primer byte es el byte de orden inferior del canal 0 (canal izquierdo); el segundo byte es el byte de orden superior del canal 0; el tercer byte es el byte de orden bajo del canal 1 (canal derecho); y el cuarto byte es el byte de orden superior del canal 1. |
| Otros                    | Cada muestra está contenida en un bloque que es un múltiplo de 4 bytes, pero los ejemplos pueden no estar alineados con bytes. La organización de canales se especifica mediante una máscara. Para obtener más información, [**vea ESTALAATEXTENSIBLE.**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>Cerrar dispositivos Waveform-Audio salida

Una vez completada la reproducción de audio de forma de onda, llame [**a waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) para cerrar el dispositivo de salida. Si se llama a **waveOutClose** mientras se reproduce un archivo de audio de forma de onda, se produce un error en la operación de cierre y la función devuelve un código de error que indica que el dispositivo no se ha cerrado. Si no desea esperar a que finalice la reproducción antes de cerrar el dispositivo, llame a la [**función waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) antes de cerrar. Esto finaliza la reproducción y permite cerrar el dispositivo. Asegúrese de usar la función [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) para limpiar la preparación en todos los bloques de datos antes de cerrar el dispositivo.

 

 