---
title: Administración de Waveform-Audio recording
description: Administración de Waveform-Audio recording
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- audio de forma de onda, grabación
- interfaz de audio de forma de onda, grabación
- audio de forma de onda de grabación, acerca de
- Estructura WAVEHDR
- Función waveInAddBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173642"
---
# <a name="managing-waveform-audio-recording"></a>Administración de Waveform-Audio recording

Después de abrir un dispositivo de entrada de audio de forma de onda, puede empezar a grabar datos de audio de forma de onda. Los datos de audio de forma de onda se graban en búferes proporcionados por la aplicación especificados por una [**estructura WAVEHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) Estos bloques de datos deben prepararse antes de que se utilicen. Para obtener más información, vea [Bloques de datos de audio](audio-data-blocks.md).

Windows proporciona las siguientes funciones para administrar la grabación de audio de forma de onda.



| Función                                   | Descripción                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | Envía un búfer al controlador del dispositivo para que se pueda rellenar con datos de audio de forma de onda grabados. |
| [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | Detiene la grabación de audio de forma de onda y marca todos los búferes pendientes como se ha hecho.                      |
| [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | Inicia la grabación de audio de forma de onda.                                                           |
| [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | Detiene la grabación de audio de forma de onda.                                                            |



 

Use la [**función waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) para enviar búferes al controlador de dispositivo. A medida que los búferes se rellenan con datos de audio de forma de onda grabados, la aplicación se notifica con un mensaje de ventana, un mensaje de devolución de llamada, un mensaje de subproceso o un evento, en función de la marca especificada cuando se abrió el dispositivo.

Antes de empezar a grabar mediante [**waveInStart,**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)debe enviar al menos un búfer al controlador o se podrían perder los datos entrantes.

Antes de cerrar el dispositivo mediante [**waveInClose,**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)llame a [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) para marcar los bloques de datos pendientes como se está haciendo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de forma de onda](recording-waveform-audio.md)
</dt> </dl>

 

 