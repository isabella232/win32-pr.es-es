---
title: La función PlaySound
description: La función PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- audio multimedia, función Play Sound
- audio, función Play Sound
- audio de forma de onda, función PlaySound
- Función PlaySound, acerca de
- Función sndPlaySound
- Función PlaySound, en comparación con la función sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1921ec4ef91f6266b48ee80d7f42be4540124c0b5c98dc18438ce0d16c398c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370855"
---
# <a name="the-playsound-function"></a>La función PlaySound

Puede usar la función [**Play Sound**](/previous-versions//dd743680(v=vs.85)) para reproducir audio de forma de onda si el sonido cabe en la memoria disponible. (La [**función sndPlaySound**](/previous-versions//dd798676(v=vs.85)) ofrece un subconjunto de las funcionalidades de PlaySound. Para maximizar la portabilidad de la aplicación basada en Win32, use **PlaySound**, no **sndPlaySound**).

La **función PlaySound** permite especificar un sonido de una de estas tres maneras:

-   Como alerta del sistema, mediante el alias almacenado en el archivo WIN.INI o el registro
-   Como nombre de archivo
-   Como identificador de recurso

La [**función PlaySound**](/previous-versions//dd743680(v=vs.85)) permite reproducir un sonido en un bucle continuo, finalizando solo cuando se vuelve a llamar a **PlaySound,** especificando **NULL** o el identificador de sonido de otro sonido para el *parámetro pszSound.*

Puede usar **PlaySound para** reproducir el sonido de forma sincrónica o asincrónica, y para controlar el comportamiento de la función de otras maneras cuando debe compartir recursos del sistema.

Para obtener más información sobre el uso de PlaySound, consulte los temas siguientes:

-   [Uso de PlaySound para reproducir Waveform-Audio archivos](using-playsound-to-play-waveform-audio-files.md)
-   [Uso de Sonidos de reproducción para bucles](using-playsound-to-loop-sounds.md)
-   [Uso de Play Sound para reproducir sonidos del sistema](using-playsound-to-play-system-sounds.md)

Para obtener más ejemplos de cómo usar **PlaySound** en las aplicaciones basadas en Win32, consulte [Reproducción de recursos de WAVE.](playing-wave-resources.md)

 

 