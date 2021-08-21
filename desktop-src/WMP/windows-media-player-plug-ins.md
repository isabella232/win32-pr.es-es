---
title: Reproductor de Windows Media Complementos
description: Reproductor de Windows Media Complementos
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Reproductor de Windows Media,complementos
- Reproductor de Windows Media complementos, acerca de
- complementos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ee8ac885d088095157375a04dd3af48bbfcdfd080349f652b68cae26cbb419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053993"
---
# <a name="windows-media-player-plug-ins"></a>Reproductor de Windows Media Complementos

Microsoft Reproductor de Windows Media expone interfaces que le permiten ampliar la funcionalidad de varias maneras. En las secciones siguientes se describen las arquitecturas de complemento admitidas y el proceso de creación de un complemento:



| Sección                                                                                                         | Descripción                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creación de un complemento](building-a-plug-in.md)                                                                    | Puede crear varios tipos de complementos mediante Visual Studio y el asistente para Reproductor de Windows Media complementos.                                                                                                                                                                                             |
| [Reproductor de Windows Media Visualizaciones personalizadas](windows-media-player-custom-visualizations.md)                    | Reproductor de Windows Media visualizaciones son objetos del Modelo de objetos componentes (COM) que se usan para mostrar imágenes visuales que se sincronizan con la parte de audio de la reproducción multimedia del reproductor. Las visualizaciones personalizadas se pueden crear mediante Microsoft Visual C++.                                             |
| [Reproductor de Windows Media Interfaz de usuario complementos](windows-media-player-user-interface-plug-ins.md)                | Reproductor de Windows Media complementos de interfaz de usuario agregan nueva funcionalidad al panel **Reproducción** ahora del reproductor en modo completo. Puede crear complementos que usen el área de visualización, una ventana independiente, el área de configuración, el área de metadatos o complementos en segundo plano que no exponen ninguna interfaz de usuario visible. |
| [Reproductor de Windows Media Complementos DE DSP](windows-media-player-dsp-plug-ins.md)                                      | Reproductor de Windows Media Los complementos de DSP modifican o procesan datos de audio y vídeo antes de que los represente el reproductor. Los complementos DSP son objetos multimedia DirectX (DMO) que se conectan al reproductor a través de interfaces COM.                                                                                           |
| [Reproductor de Windows Media Complementos de representación (en desuso)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85)) | Reproductor de Windows Media los complementos de representación descodifican (si es necesario) y representan los datos personalizados contenidos en una secuencia Windows de formato multimedia. Los complementos de representación son objetos multimedia directX (DMO) que se conectan al reproductor a través de interfaces COM.                                                                  |
| [Reproductor de Windows Media Complementos de conversión](windows-media-player-conversion-plug-ins.md)                        | Reproductor de Windows Media de conversión de archivos multimedia digitales creados mediante tecnologías no proporcionadas por Microsoft, en formato de sistemas avanzados (ASF).                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media Sdk**](windows-media-player-sdk.md)
</dt> </dl>

 

 