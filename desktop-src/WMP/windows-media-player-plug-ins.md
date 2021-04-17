---
title: Complementos de Media Player de Windows
description: Complementos de Media Player de Windows
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Media Player de Windows, Complementos
- Complementos de Media Player de Windows, acerca de
- complementos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714420"
---
# <a name="windows-media-player-plug-ins"></a>Complementos de Media Player de Windows

Microsoft Windows Media Player expone interfaces que permiten ampliar la funcionalidad de varias maneras. En las secciones siguientes se describen las arquitecturas de complementos admitidas y el proceso de creación de un complemento:



| Sección                                                                                                         | Descripción                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compilar un complemento](building-a-plug-in.md)                                                                    | Puede crear varios tipos de complementos mediante Visual Studio y el Asistente para complementos de Media Player de Windows.                                                                                                                                                                                             |
| [Visualizaciones personalizadas de Windows Media Player](windows-media-player-custom-visualizations.md)                    | Las visualizaciones de Windows Media Player son objetos del modelo de objetos componentes (COM) que se usan para mostrar imágenes visuales que se sincronizan con la parte de audio de la reproducción multimedia del reproductor. Las visualizaciones personalizadas se pueden crear mediante Microsoft Visual C++.                                             |
| [Complementos de la interfaz de usuario de Windows Media Player](windows-media-player-user-interface-plug-ins.md)                | Los complementos de la interfaz de usuario de Windows Media Player agregan nuevas funciones al panel **reproducción en curso** del reproductor en modo completo. Puede crear complementos que usan el área de visualización, una ventana independiente, el área de configuración, el área de metadatos o los complementos de fondo que no exponen ninguna interfaz de usuario visible. |
| [Complementos DSP de Windows Media Player](windows-media-player-dsp-plug-ins.md)                                      | Los complementos DSP de Windows Media Player modifican o procesan datos de audio y vídeo antes de que los represente el reproductor. Los complementos DSP son objetos multimedia de DirectX (DMO) que se conectan al reproductor a través de interfaces COM.                                                                                           |
| [Complementos de representación de Windows Media Player (desusado)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85)) | Los complementos de representación de Windows Media Player descodifican (si es necesario) y representan los datos personalizados contenidos en una secuencia de formato de Windows Media. Los complementos de representación son objetos multimedia de DirectX (DMO) que se conectan al reproductor a través de interfaces COM.                                                                  |
| [Complementos de conversión de Windows Media Player](windows-media-player-conversion-plug-ins.md)                        | Los complementos de conversión de Windows Media Player convierten archivos multimedia digitales creados con tecnologías no proporcionadas por Microsoft, en formato de sistema avanzado (ASF).                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**SDK de Media Player de Windows**](windows-media-player-sdk.md)
</dt> </dl>

 

 