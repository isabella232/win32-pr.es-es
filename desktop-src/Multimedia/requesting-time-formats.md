---
title: Solicitar formatos de hora
description: Solicitar formatos de hora
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- Interfaz digital de instrumentar música (MIDI),formatos de tiempo
- MIDI (Interfaz digital de instrumentar música), formatos de tiempo
- Servicios DE MIDI, formatos de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370939"
---
# <a name="requesting-time-formats"></a>Solicitar formatos de hora

Windows utiliza la estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) para representar el tiempo en uno o varios formatos diferentes, incluidos milisegundos, ejemplos, formatos de puntero de canción SMPTE y MIDI. El **miembro wType** especifica el formato de hora.

La [**función midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) usa la **estructura MMTIME.** Antes de llamar a esta función, debe establecer el **miembro wType** para indicar el formato de hora solicitado. Para ver si se admite el formato de hora solicitado, **compruebe wType** después de la llamada. Si no se admite el formato de hora solicitado, la hora se especifica en un formato de hora alternativo seleccionado por el controlador de dispositivo y el miembro **wType** cambia para indicar el formato de hora seleccionado.

Para obtener más información sobre la **estructura MMTIME,** vea [Temporizadores multimedia](multimedia-timers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 