---
title: Waveform-Audio errores
description: Waveform-Audio errores
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- MCIERR devuelve valores, errores de audio de forma de onda
- referencia multimedia, errores de audio de forma de onda
- referencia de multimedia, errores de audio de forma de onda
- Interfaz de control multimedia (MCI), errores de audio de onda
- MCI (interfaz de control multimedia), errores de audio de onda
- referencia de MCI, errores de audio de forma de onda
- Referencia de MCI, errores de audio de forma de onda
- Interfaz de control multimedia (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- errores de audio de forma de onda
- Errores de audio de forma de onda de MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d626ad885d2c06a856a0c2444dcfcaee919942b0d57616671dc07d35a5acd062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804075"
---
# <a name="waveform-audio-errors"></a>Waveform-Audio errores

Los siguientes valores devueltos adicionales se definen para los dispositivos MCI de audio y forma de onda:



| Valor                             | Significado                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ WAVE \_ INPUTSINUSE         | Todos los dispositivos de forma de onda que pueden registrar archivos en el formato actual están en uso. Espere hasta que uno de estos dispositivos sea gratuito. a continuación, inténtelo de nuevo.                              |
| ENTRADAS DE \_ ONDA \_ MCIERRUNSUITABLE    | Ningún dispositivo de forma de onda instalado puede registrar archivos en el formato actual. Use la opción Controladores de la Panel de control instalar un dispositivo de grabación de forma de onda adecuado. |
| MCIERR \_ WAVE \_ INPUTUNSPECIFIED    | Puede especificar cualquier dispositivo de grabación de forma de onda compatible.                                                                                                           |
| MCIERR \_ WAVE \_ OUTPUTSINUSE        | Todos los dispositivos de forma de onda que pueden reproducir archivos en el formato actual están en uso. Espere hasta que uno de estos dispositivos sea gratuito. a continuación, inténtelo de nuevo.                                |
| SALIDAS \_ DE MCIERR \_ WAVEUNSUITABLE   | Ningún dispositivo de forma de onda instalado puede reproducir archivos en el formato actual. Use la opción Controladores de la Panel de control para instalar un dispositivo de forma de onda adecuado.             |
| MCIERR \_ WAVE \_ OUTPUTUNSPECIFIED   | Puede especificar cualquier dispositivo de reproducción de forma de onda compatible.                                                                                                            |
| MCIERR \_ WAVE \_ SETINPUTINUSE       | El dispositivo de forma de onda actual está en uso. Espere hasta que el dispositivo esté libre; a continuación, vuelva a intentar establecer el dispositivo para la grabación.                                              |
| MCIERR \_ WAVE \_ SETINPUTUNSUITABLE  | El dispositivo que usa para grabar una forma de onda no puede reconocer el formato de datos.                                                                                     |
| MCIERR \_ WAVE \_ SETOUTPUTINUSE      | El dispositivo de forma de onda actual está en uso. Espere hasta que el dispositivo esté libre; a continuación, vuelva a intentar establecer el dispositivo para la reproducción.                                               |
| MCIERR \_ WAVE \_ SETOUTPUTUNSUITABLE | El dispositivo que usa para reproducir una forma de onda no puede reconocer el formato de datos.                                                                                   |



 

 

 




