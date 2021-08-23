---
description: Interfaces de captura de vídeo
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfaces de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfee9807a94f381fef3a294dcd405de6fe8b67fafef3ace562309fe5e10d2ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633065"
---
# <a name="video-capture-interfaces"></a>Interfaces de captura de vídeo

Estas interfaces admiten la captura de vídeo mediante dispositivos microsoft® Windows® Driver Model (WDM) o dispositivos heredados de Microsoft® Video para Windows® (VFW).



| Interfaz                                                        | Descripción                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMAnalogVideoDecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | Controlar la digitalización de vídeo en una tarjeta de captura de vídeo WDM.                                                      |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | Controlar cómo un pin asigna búferes.                                                                         |
| [**IAMCopyCaptureFileProgress**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | Interfaz de devolución de llamada para recibir el progreso de una operación de copia de archivos.                                         |
| [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | Cree una conexión de hardware entre un origen de audio o vídeo WDM y un dispositivo de captura WDM.                   |
| [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | Consultar un filtro de captura sobre el rendimiento de la captura.                                                            |
| [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | Controlar las horas de inicio y de detenerse de secuencias individuales.                                                      |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | Consulte y establezca el formato de salida del filtro de captura.                                                            |
| [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | Muestra los cuadros de diálogo proporcionados por los controladores de captura vfw.                                                    |
| [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | Controlar la imagen desde un dispositivo de captura.                                                                   |
| [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | Ajuste las calidades de una señal de vídeo, como el brillo, el contraste, el matiz, la saturación, el gamma y la nidez. |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | Cree gráficos de filtro para la captura de vídeo.                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | Especifique el nombre y los atributos de un archivo de salida.                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de control de dispositivos externos](external-device-control-interfaces.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



