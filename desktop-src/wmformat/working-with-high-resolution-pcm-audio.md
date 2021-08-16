---
title: Trabajar con High-Resolution pcm audio
description: Trabajar con High-Resolution pcm audio
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Formato de sistemas avanzados (ASF), audio PCM de alta resolución
- ASF (formato de sistemas avanzados), audio PCM de alta resolución
- perfiles, audio PCM de alta resolución
- códecs, audio PCM de alta resolución
- Formato de sistemas avanzados (ASF), audio PCM
- ASF (formato de sistemas avanzados), audio PCM
- profiles,PCM audio
- códecs, audio PCM
- audio PCM de alta resolución
- Audio de PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a76cfb8397cacd6d39f62ea3594c8be655f4543e0b48b60cafbf15b9783c7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194860"
---
# <a name="working-with-high-resolution-pcm-audio"></a>Trabajar con High-Resolution pcm audio

Algunos de los formatos de entrada para el códec de Windows Media Audio 9 Professional y el códec sin pérdida de Windows Media Audio 9 son formatos PCM de alta resolución. Se trata de formatos PCM que tienen más de dos canales o más de 16 bits por muestra (el audio con más de dos canales también se denomina audio multicanal).

Estos formatos se configuran mediante una extensión estructurada de la estructura [**DE FORMADEDATOSTEX,**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) [**denominada FORMADETEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) La **estructura WAVEFORMATEXTENSIBLE** incluye información sobre los canales incluidos en el audio. Esta estructura es necesaria cuando se usa audio PCM de alta resolución, ya que algunas API de Windows no aceptarán estructuras **DESATEX que** contengan valores de alta resolución.

Los formatos PCM de alta resolución tienen 22 bytes de datos extendidos, que se especifican en el **miembro cbSize** de la **estructura DESMODATEX.** Los formatos de Windows de audio multimedia de alta resolución no usan la estructura **FORMADEDATOATEXTENSIBLE,** pero sí tienen datos extendidos anexados a la **estructura DESATEX.**

Los códecs de audio Windows Media solo admiten lacoding a formatos PCM de alta resolución cuando la aplicación se ejecuta en Windows XP o posterior. En versiones anteriores de Microsoft Windows, los códecs descodifican en un formato con un máximo de 16 bits por muestra y 2 canales. Además, debe especificar que desea que el códec descodifique en PCM de alta definición estableciendo la configuración de salida g \_ wszEnableDiscreteOutput en **TRUE** mediante el método [**IWMReaderAdvanced2::SetOutputSetting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) Después de realizar esta llamada, las salidas enumeradas por el lector incluirán formatos de alta definición.

El audio multicanal requiere más configuración. Para obtener más información, vea [Lectura de audio multicanal.](reading-multichannel-audio.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> </dl>

 

 