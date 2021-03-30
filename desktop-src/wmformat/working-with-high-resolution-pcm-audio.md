---
title: Trabajar con High-Resolution PCM audio
description: Trabajar con High-Resolution PCM audio
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Advanced Systems Format (ASF), audio PCM de alta resolución
- ASF (formato de sistemas avanzados), audio PCM de alta resolución
- perfiles, audio PCM de alta resolución
- códecs, audio PCM de alta resolución
- Advanced Systems Format (ASF), PCM audio
- ASF (formato de sistemas avanzados), audio PCM
- perfiles, audio PCM
- códecs, audio PCM
- audio PCM de alta resolución
- Audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995370"
---
# <a name="working-with-high-resolution-pcm-audio"></a>Trabajar con High-Resolution PCM audio

Algunos de los formatos de entrada para el códec Windows Media Audio 9 Professional y el códec Windows Media Audio 9 Lossless son formatos PCM de alta resolución. Se trata de formatos PCM que tienen más de dos canales o más de 16 bits por muestra (el audio con más de dos canales también se denomina audio multicanal).

Estos formatos se configuran mediante una extensión estructurada de la estructura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) , denominada [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)). La estructura **WAVEFORMATEXTENSIBLE** incluye información sobre los canales incluidos en el audio. Esta estructura es necesaria cuando se usa audio PCM de alta resolución, ya que algunas API de Windows no aceptarán estructuras **WAVEFORMATEX** que contengan valores de alta resolución.

Los formatos PCM de alta resolución tienen 22 bytes de datos extendidos, que se especifican en el miembro **cbSize** de la estructura **WAVEFORMATEX** . Los formatos de audio de Windows Media de alta resolución no usan la estructura **WAVEFORMATEXTENSIBLE** , pero tienen datos extendidos anexados a la estructura **WAVEFORMATEX** .

Los códecs de audio de Windows Media solo admiten la descodificación de formatos PCM de alta resolución cuando la aplicación se ejecuta en Windows XP o posterior. En versiones anteriores de Microsoft Windows, los códecs se descodifican en un formato con un máximo de 16 bits por muestra y 2 canales. Además, debe especificar que desea que el códec descodifique en PCM de alta definición estableciendo el \_ valor de salida g wszEnableDiscreteOutput en **true** mediante el método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) . Después de efectuar esta llamada, las salidas enumeradas por el lector incluirán formatos de alta definición.

El audio multicanal requiere más configuración. Para obtener más información, consulte [lectura de audio multicanal](reading-multichannel-audio.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> </dl>

 

 