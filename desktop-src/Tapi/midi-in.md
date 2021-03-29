---
description: La clase de dispositivo MIDI/in consta de secuenciadores MIDI que se usan para la entrada. Puede acceder a estos dispositivos mediante las funciones MIDI, que se describen en el kit de desarrollo de software (SDK) de la plataforma.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808305"
---
# <a name="midiin"></a>MIDI/in

La clase de dispositivo MIDI/in consta de secuenciadores MIDI que se usan para la entrada. Puede acceder a estos dispositivos mediante las funciones MIDI, que se describen en el kit de desarrollo de software (SDK) de la plataforma.

Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

El miembro **DeviceId** es el identificador de un dispositivo MIDI cerrado. Este identificador se usa en una llamada a la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) para abrir el dispositivo para la entrada. Puede usar el identificador de dispositivo resultante para grabar datos MIDI desde el dispositivo de línea o teléfono.

Para obtener más información acerca de las funciones MIDI, consulte [**funciones multimedia**](../multimedia/multimedia-functions.md).

 

 
