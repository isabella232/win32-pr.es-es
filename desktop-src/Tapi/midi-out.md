---
description: La clase de dispositivo MIDI/Out consta de secuenciadores MIDI que se utilizan para la salida. Puede acceder a estos dispositivos mediante las funciones MIDI, que se describen en el kit de desarrollo de software (SDK) de la plataforma.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: MIDI/salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275175"
---
# <a name="midiout"></a>MIDI/salida

La clase de dispositivo MIDI/Out consta de secuenciadores MIDI que se utilizan para la salida. Puede acceder a estos dispositivos mediante las funciones MIDI, que se describen en el kit de desarrollo de software (SDK) de la plataforma.

Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

El miembro **DeviceId** es el identificador de un dispositivo MIDI cerrado. Este identificador se usa en una llamada a la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) para abrir el dispositivo para la salida. Puede usar el identificador de dispositivo resultante para reproducir datos MIDI en el dispositivo de línea o teléfono.

Para obtener más información acerca de las funciones MIDI, consulte [**funciones multimedia**](../multimedia/multimedia-functions.md).

 

 
