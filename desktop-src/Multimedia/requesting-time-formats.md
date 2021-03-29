---
title: Solicitar formatos de hora
description: Solicitar formatos de hora
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- Interfaz digital de instrumentos musicales (MIDI), formatos de hora
- MIDI (interfaz digital de instrumentos musicales), formatos de hora
- Servicios MIDI, formatos de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789754"
---
# <a name="requesting-time-formats"></a>Solicitar formatos de hora

Windows usa la estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) para representar la hora en uno o varios formatos diferentes, incluidos los formatos de puntero de milisegundos, ejemplos, SMPTE y MIDI Song. El miembro **wType** especifica el formato de hora.

La función [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) utiliza la estructura **MMTIME** . Antes de llamar a esta función, debe establecer el miembro **wType** para indicar el formato de hora solicitado. Para ver si se admite el formato de hora solicitado, compruebe **wType** después de la llamada. Si no se admite el formato de hora solicitado, la hora se especifica en un formato de hora alternativo seleccionado por el controlador de dispositivo y el miembro **wType** se cambia para indicar el formato de hora seleccionado.

Para obtener más información sobre la estructura **MMTIME** , vea [temporizadores multimedia](multimedia-timers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios MIDI](midi-services.md)
</dt> </dl>

 

 