---
description: Configuración de los pines de salida de Demux
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: Configuración de los pines de salida de Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56a24af3f49f26efe4ff6afad075a3cef61fcd1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161591"
---
# <a name="configuring-the-demux-output-pins"></a>Configuración de los pines de salida de Demux

Cuando la demux MPEG-2 recibe un paquete de datos, debe determinar qué pin de salida debe analizar y entregar los datos. En el modo de secuencia del programa, demux asigna los IDs de secuencia a los pines de salida. En el modo de secuencia de transporte, asigna los PIN a los pines de salida. Por ejemplo, en el modo de secuencia de transporte, si pid 0x31 está asignado al pin 0, todos los paquetes TS con ese número de PID se enrutan al pin de salida 0. Si el demux recibe un paquete cuyo id. de flujo o PID no está asignado a ningún pin de salida, simplemente descarta el paquete.

En el modo de extracción, demux crea automáticamente los pines de salida para las secuencias de audio y vídeo del archivo y asigna los IDs de secuencia a los pines.

En el modo de inserción, la aplicación o otro filtro deben configurar los pines de salida. En el caso de los orígenes de televisión digital que usan la arquitectura del controlador de difusión (BDA), el filtro del proveedor de red funciona con el filtro TIF para configurar el demux. La aplicación no tiene que hacer nada. En otros escenarios, la aplicación debe configurar los pines de salida.

La demux comienza sin pins de salida. Para crear un pin de salida, llame al método [**IMpeg2Demultiplexer::CreateOutputPin**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) en el filtro. Este método toma un tipo de medio y un nombre de pin y devuelve un **puntero IPin.** El tipo de medio se usa cuando el pin se conecta a otro filtro, normalmente un descodificador; se proporciona un ejemplo de la sección Using [the Demux with Elementary Secuencias](using-the-demux-with-elementary-streams.md). El nombre del pin puede ser cualquier cosa que quiera, excepto que no se permiten nombres de pin duplicados.

A continuación, asigne uno o varios ID de flujo o PIN a la nueva patilla de salida. Para secuencias de programa, consulte el pin **de IMPEG2StreamIdMap** y llame a [**IMPEG2StreamIdMap::MapStreamId**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid). Para flujos de transporte, consulte el pin de **IMPEG2PIDMap** y llame a [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid).

Hay varias maneras de que la demux pueda analizar paquetes de TS. Para cada pin de salida, el método de análisis viene determinado por el *parámetro MediaSampleContent* en el **método MapPID.**



| Value                     | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SECUENCIA \_ ELEMENTAL DE \_ MEDIOS | El filtro proporciona cargas de PES. En este modo, el filtro desempaqueta los paquetes PES, por lo que el filtro de nivel inferior recibe la secuencia de bytes ES, sin los encabezados de paquete PES. (Solo secuencias de audio y vídeo).                                                                                                                                                     |
| MEDIA \_ MPEG2 \_ PSI         | El filtro proporciona secciones completas de PSI, como tablas PAT, tablas PMT, tablas CAT, etc.                                                                                                                                                                                                                                                               |
| CARGA DE \_ TRANSPORTE \_ MULTIMEDIA | El filtro extrae las cargas de los paquetes de TS y las entrega sin más análisis. En el caso de las secuencias elementales, esto significa que la demux entregará paquetes PES completos, incluidos los encabezados de paquete PES.                                                                                                                                                    |
| PAQUETE DE \_ TRANSPORTE \_ DE MEDIOS  | El filtro entrega paquetes de TS completos. El demux enruta los paquetes TS según sus PID, pero no examina ni procesa los paquetes. Los paquetes con errores no se filtran. Demux no vuelve a multiplexar los paquetes y el flujo de salida resultante no es una secuencia de transporte MPEG-2 compatible. Este modo se denomina *modo de paso a* través. |



 

En el caso de las secuencias de programa, demux siempre entrega cargas PES.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del demultiplexor MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



