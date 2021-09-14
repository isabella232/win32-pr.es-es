---
title: La función Play Sound
description: La función Play Sound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- audio multimedia, función Play Sound
- audio, función Play Sound
- audio de forma de onda, función Play Sound
- Función Play Sound, acerca de
- Función sndPlay Sound
- Función Play Sound, en comparación con la función sndPlay Sound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260676"
---
# <a name="the-playsound-function"></a>La función Play Sound

Puede usar la función [**Play Sound para**](/previous-versions//dd743680(v=vs.85)) reproducir audio de forma de onda si el sonido cabe en la memoria disponible. (La [**función sndPlay Sound**](/previous-versions//dd798676(v=vs.85)) ofrece un subconjunto de las funcionalidades de Play Sound. Para maximizar la portabilidad de la aplicación basada en Win32, use **Play Sound**, no **sndPlay Sound).**

La **función Play Sound** permite especificar un sonido de una de estas tres maneras:

-   Como alerta del sistema, mediante el alias almacenado en el archivo WIN.INI o el registro
-   Como nombre de archivo
-   Como identificador de recursos

La [**función Play Sound**](/previous-versions//dd743680(v=vs.85)) permite reproducir un sonido en un bucle continuo, finalizando solo cuando se vuelve a llamar a Play **Sound,** especificando **NULL** o el identificador de sonido de otro sonido para el *parámetro psz Sound.*

Puede usar **Play Sound para** reproducir el sonido de forma sincrónica o asincrónica, y para controlar el comportamiento de la función de otras maneras cuando debe compartir recursos del sistema.

Para obtener más información sobre el uso de Play Sound, consulte los temas siguientes:

-   [Uso de Play Sound para reproducir Waveform-Audio archivos](using-playsound-to-play-waveform-audio-files.md)
-   [Uso de Play Sound para sonidos de bucle](using-playsound-to-loop-sounds.md)
-   [Uso de Play Sound para reproducir sonidos del sistema](using-playsound-to-play-system-sounds.md)

Para obtener más ejemplos de cómo usar **Play Sound en** las aplicaciones basadas en Win32, vea Playing WAVE [Resources](playing-wave-resources.md).

 

 