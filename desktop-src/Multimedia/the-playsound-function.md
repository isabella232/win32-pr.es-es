---
title: La función PlaySound
description: La función PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- audio multimedia, función PlaySound
- audio, función PlaySound
- audio de onda, función PlaySound
- Función PlaySound, acerca de
- sndPlaySound función)
- Función PlaySound, en comparación con la función sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270882"
---
# <a name="the-playsound-function"></a>La función PlaySound

Puede usar la función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) para reproducir audio de una onda si el sonido encaja en la memoria disponible. (La función [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) ofrece un subconjunto de las capacidades de PlaySound. Para maximizar la portabilidad de la aplicación basada en Win32, use **PlaySound**, no **sndPlaySound**).

La función **PlaySound** le permite especificar un sonido de una de estas tres maneras:

-   Como alerta del sistema, mediante el alias almacenado en el archivo WIN.INI o el registro
-   Como nombre de archivo
-   Como identificador de recursos

La función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) permite reproducir un sonido en un bucle continuo y finalizar solo cuando se vuelve a llamar a **PlaySound** , especificando **null** o el identificador de sonido de otro sonido para el parámetro *pszSound* .

Puede usar **PlaySound** para reproducir el sonido de forma sincrónica o asincrónica, y para controlar el comportamiento de la función de otras maneras cuando debe compartir recursos del sistema.

Para obtener más información sobre el uso de PlaySound, vea los temas siguientes:

-   [Usar PlaySound para reproducir archivos de Waveform-Audio](using-playsound-to-play-waveform-audio-files.md)
-   [Usar PlaySound para reproducir sonidos](using-playsound-to-loop-sounds.md)
-   [Usar PlaySound para reproducir sonidos del sistema](using-playsound-to-play-system-sounds.md)

Para obtener más ejemplos de cómo usar **PlaySound** en las aplicaciones basadas en Win32, vea [reproducir recursos de Wave](playing-wave-resources.md).

 

 