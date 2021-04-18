---
title: Funciones de XAudio2
description: Esta sección contiene información sobre las funciones que proporciona la API de Microsoft XAudio2.
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd8bcfdb00565d6f8bbc31ae0ee6a24f106dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706617"
---
# <a name="xaudio2-functions"></a>Funciones de XAudio2

Esta sección contiene información sobre las funciones que proporciona la API de Microsoft XAudio2.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                       | Descripción                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | Crea una instancia del efecto [XAPOFX](xapofx-overview.md) solicitado.<br/>                                                                                                                                                         |
| [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           | Crea una instancia de la interfaz [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) para el procesamiento de la función de transferencia relacionada con el encabezado (HRTF).<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | Función insertada que convierte los parámetros I3DL2 (2,0 nivel de instrucciones de representación de audio 3D interactivo) en parámetros de XAudio2 nativos.<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | Calcula la configuración de DSP con respecto a los parámetros 3D.<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | Establece todas las constantes de audio 3D global.<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | Función insertada que convierte un valor de relación de amplitud en un valor de decibelio.<br/>                                                                                                                                                         |
| [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | Crea un nuevo objeto **XAudio2** y devuelve un puntero a su interfaz [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               | Crea un nuevo objeto de procesamiento de audio (APO) de reverberación y le devuelve un puntero.<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     | Crea un nuevo objeto de procesamiento de audio (APO) de medición de volumen y devuelve un puntero a él.<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOnePoleCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | Función insertada que convierte las frecuencias de límite de filtro expresadas en hercios en los coeficientes de filtro utilizados con el miembro **Frequency** de la estructura de [**\_ \_ parámetros de filtro XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/>   |
| [**XAudio2CutoffFrequencyToRadians**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | Función insertada que convierte las frecuencias de límite de filtro expresadas en hercios en los valores de frecuencia de radianes utilizados en el miembro **Frequency** de la estructura de [**\_ \_ parámetros de filtro XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | Función insertada que convierte un valor de decibelios en un valor de proporción de amplitud.<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | Función insertada que convierte un valor de relación de frecuencia en un valor de semitono.<br/>                                                                                                                                                         |
| [**XAudio2RadiansToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | Función insertada que convierte de las frecuencias radiales usadas en [**\_ \_ los parámetros de filtro de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) a frecuencias absolutas en hercios.<br/>                                                          |
| [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | Función insertada que convierte un valor de semitono en un valor de relación de frecuencia.<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[XAudio2: referencia de:P rogramming](programming-reference.md)
</dt> </dl>

 

 




