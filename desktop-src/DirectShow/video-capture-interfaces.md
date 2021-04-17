---
description: Interfaces de captura de vídeo
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfaces de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677544"
---
# <a name="video-capture-interfaces"></a>Interfaces de captura de vídeo

Estas interfaces admiten la captura de vídeo, mediante dispositivos de Microsoft® Windows® Driver Model (WDM) o los dispositivos heredados de Microsoft® video para Windows® (VFW).



| Interfaz                                                        | Descripción                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMAnalogVideoDecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | Controlar la digitalización de vídeo en una tarjeta de captura de vídeo WDM.                                                      |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | Controla cómo un PIN asigna los búferes.                                                                         |
| [**IAMCopyCaptureFileProgress**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | Interfaz de devolución de llamada para recibir el progreso de una operación de copia de archivos.                                         |
| [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | Cree una conexión de hardware entre un origen de audio o vídeo WDM y un dispositivo de captura WDM.                   |
| [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | Consultar un filtro de captura sobre el rendimiento de la captura.                                                            |
| [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | Controlar las horas de inicio y detención de flujos individuales.                                                      |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | Consulta y establece el formato de salida del filtro de captura.                                                            |
| [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | Mostrar los cuadros de diálogo proporcionados por los controladores de captura VFW.                                                    |
| [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | Controle la imagen desde un dispositivo de captura.                                                                   |
| [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | Ajuste las cualidades de una señal de vídeo, como el brillo, el contraste, el matiz, la saturación, la gamma y la nitidez. |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | Cree gráficos de filtro para la captura de vídeo.                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | Especifique el nombre y los atributos de un archivo de salida.                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces de control de dispositivo externo](external-device-control-interfaces.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



