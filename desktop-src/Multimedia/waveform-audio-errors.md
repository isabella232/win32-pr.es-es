---
title: Waveform-Audio errores
description: Waveform-Audio errores
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Valores devueltos de MCIERR, errores de audio de forma de onda
- referencia multimedia, errores de audio de forma de onda
- referencia de multimedia, errores de audio de forma de onda
- Interfaz de control multimedia (MCI), errores de audio de forma de onda
- MCI (interfaz de control multimedia), errores de audio de forma de onda
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
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071706"
---
# <a name="waveform-audio-errors"></a>Waveform-Audio errores

Los siguientes valores devueltos adicionales se definen para los dispositivos de audio de forma de onda de MCI:



| Value                             | Significado                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ENTRADAS DE \_ ONDA MCIERRINUSE \_         | Todos los dispositivos de forma de onda que pueden grabar archivos en el formato actual están en uso. Espere hasta que uno de estos dispositivos sea gratuito; a continuación, inténtelo de nuevo.                              |
| ENTRADAS DE \_ ONDA \_ MCIERRUNSUITABLE    | Ningún dispositivo de forma de onda instalado puede registrar archivos en el formato actual. Use la opción Controladores de la Panel de control para instalar un dispositivo de grabación de forma de onda adecuado. |
| ENTRADA DE \_ ONDA \_ MCIERRUNSPECIFIED    | Puede especificar cualquier dispositivo de grabación de forma de onda compatible.                                                                                                           |
| SALIDAS \_ DE ONDA \_ MCIERRINUSE        | Todos los dispositivos de forma de onda que pueden reproducir archivos en el formato actual están en uso. Espere hasta que uno de estos dispositivos sea gratuito; a continuación, inténtelo de nuevo.                                |
| SALIDAS \_ DE ONDA \_ MCIERRUNSUITABLE   | Ningún dispositivo de forma de onda instalado puede reproducir archivos en el formato actual. Use la opción Controladores de la Panel de control para instalar un dispositivo de forma de onda adecuado.             |
| MCIERR \_ WAVE \_ OUTPUTUNSPECIFIED   | Puede especificar cualquier dispositivo de reproducción de forma de onda compatible.                                                                                                            |
| MCIERR \_ WAVE \_ SETINPUTINUSE       | El dispositivo de forma de onda actual está en uso. Espere hasta que el dispositivo sea gratuito; a continuación, vuelva a intentar establecer el dispositivo para la grabación.                                              |
| MCIERR \_ WAVE \_ SETINPUTUNSUITABLE  | El dispositivo que usa para grabar una forma de onda no puede reconocer el formato de datos.                                                                                     |
| MCIERR \_ WAVE \_ SETOUTPUTINUSE      | El dispositivo de forma de onda actual está en uso. Espere hasta que el dispositivo sea gratuito; a continuación, vuelva a intentar establecer el dispositivo para la reproducción.                                               |
| MCIERR \_ WAVE \_ SETOUTPUTUNSUITABLE | El dispositivo que usa para reproducir una forma de onda no puede reconocer el formato de datos.                                                                                   |



 

 

 




