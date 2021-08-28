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
ms.openlocfilehash: db5a77fa3f137babe3b6da77cb089688fe18380c281107c14e8440a702df7652
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037525"
---
# <a name="requesting-time-formats"></a>Solicitar formatos de hora

Windows utiliza la estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) para representar el tiempo en uno o varios formatos diferentes, incluidos milisegundos, ejemplos, SMPTE y formatos de puntero de canción DE MES. El **miembro wType** especifica el formato de hora.

La [**función midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) usa la **estructura MMTIME.** Antes de llamar a esta función, debe establecer el **miembro wType** para indicar el formato de hora solicitado. Para ver si se admite el formato de hora solicitado, **compruebe wType** después de la llamada. Si no se admite el formato de hora solicitado, la hora se especifica en un formato de hora alternativo seleccionado por el controlador de dispositivo y el miembro **wType** cambia para indicar el formato de hora seleccionado.

Para obtener más información sobre la **estructura MMTIME,** vea [Temporizadores multimedia](multimedia-timers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 