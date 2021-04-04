---
title: Apertura de dispositivos de entrada MIDI
description: Apertura de dispositivos de entrada MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Interfaz digital de instrumentos musicales (MIDI), dispositivos de entrada
- MIDI (interfaz digital de instrumentos musicales), dispositivos de entrada
- grabación de audio MIDI, dispositivos de entrada
- Dispositivos de entrada MIDI
- Interfaz digital de instrumentos musicales (MIDI), abrir dispositivos de entrada
- MIDI (interfaz digital de instrumentos musicales), abrir dispositivos de entrada
- grabar audio MIDI, abrir dispositivos de entrada
- apertura de dispositivos de entrada MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790888"
---
# <a name="opening-midi-input-devices"></a>Apertura de dispositivos de entrada MIDI

Para abrir un dispositivo de entrada MIDI para grabar, utilice la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) . Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador en una ubicación de memoria especificada.

Si usa la marca de \_ Estado de e/s de MIDI \_ con **midiInOpen**, el sistema utiliza el mensaje [**\_ MOREDATA de MIM**](mim-moredata.md) para avisar de la función de devolución de llamada de la aplicación cuando no está procesando los datos MIDI lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de entrada. (El [**mensaje \_ \_ MOREDATA de MIM de mm**](mm-mim-moredata.md) realiza el mismo trabajo con devoluciones de llamada de ventana. Sin embargo, por motivos de rendimiento, la mayoría de las aplicaciones usarán funciones de devolución de llamada en lugar de devoluciones de llamada de ventana). Si la aplicación procesa datos MIDI en un subproceso independiente, el aumento de la prioridad del subproceso puede tener un impacto significativo en la capacidad de la aplicación para mantener el flujo de datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 