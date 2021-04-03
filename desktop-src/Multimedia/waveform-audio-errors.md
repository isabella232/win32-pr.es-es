---
title: Errores de Waveform-Audio
description: Errores de Waveform-Audio
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Valores devueltos de MCIERR, errores de audio de onda
- referencia multimedia, errores de audio de onda
- referencia de errores de audio multimedia y de onda
- Interfaz de control de medios (MCI), errores de audio de onda
- MCI (interfaz de control multimedia), errores de audio de onda
- referencia de errores de audio y de onda
- Referencia de MCI, errores de audio de onda
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- onda-errores de audio
- 'Onda de onda de MCI: errores de audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075317"
---
# <a name="waveform-audio-errors"></a>Errores de Waveform-Audio

Se definen los siguientes valores devueltos adicionales para los dispositivos de audio de onda de onda MCI:



| Value                             | Significado                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ Wave \_ INPUTSINUSE         | Todos los dispositivos de forma de onda que pueden grabar archivos en el formato actual están en uso. Espere hasta que uno de estos dispositivos sea gratuito; a continuación, vuelva a intentarlo.                              |
| MCIERR \_ Wave \_ INPUTSUNSUITABLE    | Ningún dispositivo de forma de onda instalado puede grabar archivos en el formato actual. Use la opción controladores del panel de control para instalar un dispositivo de grabación de forma de onda adecuado. |
| MCIERR \_ Wave \_ INPUTUNSPECIFIED    | Puede especificar cualquier dispositivo de grabación de onda compatible.                                                                                                           |
| MCIERR \_ Wave \_ OUTPUTSINUSE        | Todos los dispositivos de forma de onda que pueden reproducir archivos en el formato actual están en uso. Espere hasta que uno de estos dispositivos sea gratuito; a continuación, vuelva a intentarlo.                                |
| MCIERR \_ Wave \_ OUTPUTSUNSUITABLE   | Ningún dispositivo de forma de onda instalado puede reproducir archivos en el formato actual. Use la opción controladores del panel de control para instalar un dispositivo de forma de onda adecuado.             |
| MCIERR \_ Wave \_ OUTPUTUNSPECIFIED   | Puede especificar cualquier dispositivo de reproducción de onda de onda compatible.                                                                                                            |
| MCIERR \_ Wave \_ SETINPUTINUSE       | El dispositivo de forma de onda actual está en uso. Espere hasta que el dispositivo sea gratuito; a continuación, vuelva a intentar establecer el dispositivo para la grabación.                                              |
| MCIERR \_ Wave \_ SETINPUTUNSUITABLE  | El dispositivo que está usando para grabar una forma de onda no puede reconocer el formato de los datos.                                                                                     |
| MCIERR \_ Wave \_ SETOUTPUTINUSE      | El dispositivo de forma de onda actual está en uso. Espere hasta que el dispositivo sea gratuito; después, vuelva a intentar establecer el dispositivo para la reproducción.                                               |
| MCIERR \_ Wave \_ SETOUTPUTUNSUITABLE | El dispositivo que está usando para reproducir una forma de onda no puede reconocer el formato de los datos.                                                                                   |



 

 

 




