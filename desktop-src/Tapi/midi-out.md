---
description: La clase de dispositivo midi/out consta de secuenciadores MIDI que se usan para la salida. Puede acceder a estos dispositivos mediante las funciones DE MIDI, que se describen en Platform Software Development Kit (SDK).
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: midi/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c0199cc7918ab9aeacb3210b6f98d5ff03fc3bca90624bee00d864727ae0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518618"
---
# <a name="midiout"></a>midi/out

La clase de dispositivo midi/out consta de secuenciadores MIDI que se usan para la salida. Puede acceder a estos dispositivos mediante las funciones DE MIDI, que se describen en Platform Software Development Kit (SDK).

Las [**funciones lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo el **miembro dwStringFormat** en el valor STRINGFORMAT BINARY y \_ anexando este miembro adicional:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

El **miembro DeviceId** es el identificador de un dispositivo MIDI cerrado. Este identificador se usa en una llamada a la [**función midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) para abrir el dispositivo para la salida. Puede usar el identificador de dispositivo resultante para reproducir datos DE MIDI en el dispositivo de línea o teléfono.

Para obtener más información sobre las funciones de MIDI, vea [**Funciones multimedia**](../multimedia/multimedia-functions.md).

 

 
