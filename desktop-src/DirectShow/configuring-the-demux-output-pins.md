---
description: Configuración de los pin de salida de Demux
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: Configuración de los pin de salida de Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56a24af3f49f26efe4ff6afad075a3cef61fcd1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152453"
---
# <a name="configuring-the-demux-output-pins"></a>Configuración de los pin de salida de Demux

Cuando el Demux de MPEG-2 recibe un paquete de datos, debe determinar qué PIN de salida debe analizar y proporcionar los datos. En el modo de flujo de programa, Demux asigna los identificadores de flujo a los pin de salida. En el modo de flujo de transporte, asigna los PID a los pin de salida. Por ejemplo, en el modo de flujo de transporte, si el PID 0x31 está asignado al pin 0, cada paquete de TS con ese número de PID se enruta a la clavija de salida 0. Si el Demux recibe un paquete cuyo identificador de secuencia o PID no esté asignado a ningún PIN de salida, simplemente descartará el paquete.

En el modo de extracción, el Demux crea automáticamente clavijas de salida para las secuencias de audio y vídeo en el archivo, y asigna los identificadores de flujo a los pin.

En el modo de extracción, los pin de salida deben ser configurados por la aplicación o por otro filtro. En el caso de las fuentes de televisión digital que usan la arquitectura de controlador de difusión (BDA), el filtro de proveedor de red trabaja con el filtro TIF para configurar Demux. La aplicación no tiene que hacer nada. En otros escenarios, la aplicación debe configurar los pin de salida.

Demux comienza sin clavijas de salida. Para crear un PIN de salida, llame al método [**IMpeg2Demultiplexer:: CreateOutputPin**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) en el filtro. Este método toma un tipo de medio y un nombre de PIN, y devuelve un puntero **IPin** . El tipo de medio se usa cuando el PIN se conecta a otro filtro, normalmente un descodificador, se proporciona un ejemplo de la sección [mediante Demux con secuencias elementales](using-the-demux-with-elementary-streams.md). El nombre del pin puede ser cualquier cosa que desee, con la excepción de que no se permiten nombres de anclaje duplicados.

A continuación, asigne uno o más identificadores o PID de flujo al nuevo PIN de salida. En el caso de las secuencias de programa, consulte el PIN de **IMPEG2StreamIdMap** y llame a [**IMPEG2StreamIdMap:: MapStreamId**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid). En el caso de las secuencias de transporte, consulte el PIN de **IMPEG2PIDMap** y llame a [**IMPEG2PIDMap:: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid).

Los Demux pueden analizar paquetes de TS de varias maneras. Para cada pin de salida, el método de análisis viene determinado por el parámetro *MediaSampleContent* para el método **MapPID** .



| Value                     | Descripción                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_secuencia básica de medios \_ | El filtro proporciona cargas de PES. En este modo, el filtro depacketizes los paquetes PES, por lo que el filtro de nivel inferior recibe el flujo de bytes ES, sin los encabezados de paquete de PES. (Solo secuencias de audio y vídeo).                                                                                                                                                     |
| MEDIA \_ MPEG2 \_ PSI         | El filtro ofrece secciones de PSI completas, como tablas de PAT, tablas de pago, tablas de gatos, etc.                                                                                                                                                                                                                                                               |
| \_carga de transporte multimedia \_ | El filtro extrae las cargas de los paquetes de TS y las entrega sin más análisis. En el caso de las secuencias elementales, esto significa que el Demux proporcionará paquetes PES completos, incluidos los encabezados de paquetes de PES.                                                                                                                                                    |
| \_paquete de transporte de medios \_  | El filtro entrega los paquetes de TS completos. El Demux enruta los paquetes de TS de acuerdo con sus PID, pero no examina ni procesa los paquetes de otra manera. Los paquetes con errores no se filtran. Demux no vuelve a multiplexar los paquetes y el flujo de salida resultante no es una secuencia de transporte MPEG-2 compatible. Este modo se denomina modo de *paso a través* . |



 

En el caso de las secuencias de programa, Demux siempre proporciona cargas de PES.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



