---
title: Funciones XAudio2
description: Esta sección contiene información sobre las funciones proporcionadas por la API XAudio2 de Microsoft.
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b950ce33f55a4b834f3ee7a068f613e144c2e30633c67e887b8a24789140a618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109655"
---
# <a name="xaudio2-functions"></a>Funciones XAudio2

Esta sección contiene información sobre las funciones proporcionadas por la API XAudio2 de Microsoft.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                       | Descripción                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | Crea una instancia del efecto [XAPOFX](xapofx-overview.md) solicitado.<br/>                                                                                                                                                         |
| [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           | Crea una instancia de la [**interfaz IXAPO para**](/windows/desktop/api/XAPO/nn-xapo-ixapo) el procesamiento de la función de transferencia relacionada con la cabeza (HRTF).<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | Función insertada que convierte los parámetros I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) en parámetros XAudio2 nativos.<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | Calcula la configuración de DSP con respecto a los parámetros 3D.<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | Establece todas las constantes de audio 3D globales.<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | Función insertada que convierte un valor de relación de amplitud en un valor de decibelio.<br/>                                                                                                                                                         |
| [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | Crea un nuevo **objeto XAudio2** y devuelve un puntero a su [**interfaz IXAudio2.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               | Crea un nuevo objeto de procesamiento de audio de reverberación (APO) y devuelve un puntero a él.<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     | Crea un nuevo objeto de procesamiento de audio del medidor de volúmenes (APO) y devuelve un puntero a él.<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOneOneCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | Función insertada que convierte las frecuencias de límite de filtro expresadas en hertz en los coeficientes de filtro utilizados con el miembro **Frequency** de la estructura [**FILTER PARAMETERS \_ \_ de XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)<br/>   |
| [**XAudio2CutoffFrequencyToRadians**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | Función insertada que convierte de las frecuencias de límite de filtro expresadas en hertz a los valores de frecuencia radiánea utilizados en el miembro **Frequency** de la estructura [**FILTER PARAMETERS \_ \_ de XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | Función insertada que convierte un valor de decibelio en un valor de relación de amplitud.<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | Función inserta que convierte un valor de relación de frecuencia en un valor de semitono.<br/>                                                                                                                                                         |
| [**XAudio2RadiansToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | Función insertada que convierte de las frecuencias radiáneas usadas en [**XAUDIO2 \_ FILTER \_ PARAMETERS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) a frecuencias absolutas en hertz.<br/>                                                          |
| [**XAudio2SemidoresToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | Función inserta que convierte un valor de semitono en un valor de relación de frecuencia.<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[XAudio2::P rogramming Reference](programming-reference.md)
</dt> </dl>

 

 




