---
title: Administración de la grabación de Waveform-Audio
description: Administración de la grabación de Waveform-Audio
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- audio de onda, grabación
- 'onda: interfaz de audio, grabación'
- grabar audio de onda de onda, acerca de
- Estructura WAVEHDR
- waveInAddBuffer función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358853"
---
# <a name="managing-waveform-audio-recording"></a>Administración de la grabación de Waveform-Audio

Después de abrir un dispositivo de entrada de onda-audio, puede empezar a grabar datos de audio de onda. La forma de onda: los datos de audio se registran en los búferes proporcionados por la aplicación especificados por una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) . Estos bloques de datos se deben preparar antes de usarse; para obtener más información, consulte [bloques de datos de audio](audio-data-blocks.md).

Windows proporciona las siguientes funciones para administrar la grabación de audio de onda.



| Función                                   | Descripción                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | Envía un búfer al controlador de dispositivo para que se pueda rellenar con datos de audio de forma de onda grabados. |
| [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | Detiene la grabación de la forma de onda y marca todos los búferes pendientes como terminados.                      |
| [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | Inicia la grabación de onda y de audio.                                                           |
| [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | Detiene la grabación de audio de onda.                                                            |



 

Utilice la función [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) para enviar búferes al controlador de dispositivo. A medida que los búferes se rellenan con datos de audio de forma de onda grabados, se notifica a la aplicación con un mensaje de ventana, un mensaje de devolución de llamada, un mensaje de subproceso o un evento, en función de la marca especificada al abrir el dispositivo.

Antes de empezar a grabar mediante [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), debe enviar al menos un búfer al controlador o se pueden perder los datos entrantes.

Antes de cerrar el dispositivo con [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), llame a [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) para marcar los bloques de datos pendientes como realizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 