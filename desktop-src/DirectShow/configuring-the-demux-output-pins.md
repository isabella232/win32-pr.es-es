---
description: Configuración de los pines de salida de Demux
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: Configuración de los pines de salida de Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0456b7354c23048bafe012439d5d2c4fa1843df601ee2d8e49aa62dfc01a4b9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813615"
---
# <a name="configuring-the-demux-output-pins"></a>Configuración de los pines de salida de Demux

Cuando la demux MPEG-2 recibe un paquete de datos, debe determinar qué pin de salida debe analizar y entregar los datos. En el modo de secuencia de programa, demux asigna los ID de secuencia a los pines de salida. En el modo de secuencia de transporte, asigna los PIN a los pines de salida. Por ejemplo, en el modo de secuencia de transporte, si pid 0x31 está asignado al pin 0, cada paquete TS con ese número de PID se enruta al pin de salida 0. Si demux recibe un paquete cuyo id. de flujo o PID no está asignado a ningún pin de salida, simplemente descarta el paquete.

En el modo de extracción, demux crea automáticamente los pines de salida para las secuencias de audio y vídeo en el archivo y asigna los IDs de secuencia a los pins.

En el modo de inserción, la aplicación o otro filtro deben configurar las clavijas de salida. En el caso de los orígenes de televisión digital que usan la arquitectura del controlador de difusión (BDA), el filtro del proveedor de red funciona con el filtro TIF para configurar la demux. La aplicación no tiene que hacer nada. En otros escenarios, la aplicación debe configurar los pines de salida.

La demux comienza sin pasadores de salida. Para crear un pin de salida, llame [**al método IMpeg2Demultiplexer::CreateOutputPin**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) en el filtro. Este método toma un tipo de medio y un nombre de pin, y devuelve un **puntero IPin.** El tipo de medio se usa cuando el pin se conecta a otro filtro, normalmente un descodificador; se proporciona un ejemplo de la sección Using [the Demux with Elementary Secuencias](using-the-demux-with-elementary-streams.md). El nombre del pin puede ser cualquier cosa que quiera, salvo que no se permiten nombres de pin duplicados.

A continuación, asigne uno o varios IDs o PID de secuencia al nuevo pin de salida. Para las secuencias de programa, consulte el pin **de IMPEG2StreamIdMap** y llame a [**IMPEG2StreamIdMap::MapStreamId**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid). Para las secuencias de transporte, consulte el pin **de IMPEG2PIDMap** y llame a [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid).

Hay varias maneras en que demux puede analizar paquetes TS. Para cada pin de salida, el método de análisis viene determinado por el *parámetro MediaSampleContent* en el **método MapPID.**



| Valor                     | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MEDIA \_ ELEMENTARY \_ STREAM | El filtro entrega cargas de PES. En este modo, el filtro desempaqueta los paquetes PES, por lo que el filtro de bajada recibe la secuencia de bytes ES, sin los encabezados de paquete PES. (Solo secuencias de audio y vídeo).                                                                                                                                                     |
| MEDIA \_ MPEG2 \_ PSI         | El filtro proporciona secciones psi completas, como tablas PAT, tablas PMT, tablas CAT, etc.                                                                                                                                                                                                                                                               |
| CARGA DE \_ TRANSPORTE \_ DE MEDIOS | El filtro extrae las cargas de los paquetes de TS y las entrega sin más análisis. En el caso de las secuencias elementales, esto significa que la demux entregará paquetes PES completos, incluidos los encabezados de paquete PES.                                                                                                                                                    |
| PAQUETE DE \_ TRANSPORTE \_ DE MEDIOS  | El filtro entrega paquetes de TS completos. Demux enruta los paquetes TS según sus PID, pero no examina ni procesa los paquetes. Los paquetes con errores no se filtran. El demux no vuelve a multiplexar los paquetes y el flujo de salida resultante no es un flujo de transporte MPEG-2 compatible. Este modo se denomina *modo de paso a* través. |



 

En el caso de las secuencias de programa, demux siempre entrega cargas de PES.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del demultiplexor MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



