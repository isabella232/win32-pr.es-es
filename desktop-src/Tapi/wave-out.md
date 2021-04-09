---
description: La clase de dispositivo de onda/salida consta de dispositivos de audio para la salida de audio de onda de bajo nivel.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: onda/salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975a3308b6f0b29e130ad07534494e1cb1d991a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913805"
---
# <a name="waveout"></a>onda/salida

La clase de dispositivo de onda/salida consta de dispositivos de audio para la salida de audio de onda de bajo nivel. Puede acceder a estos dispositivos mediante las funciones de onda, que se describen en el kit de desarrollo de software (SDK) de la plataforma. Los dispositivos de esta clase están asociados a los dispositivos de línea que admiten el \_ tipo de medio LINEMEDIAMODE AUTOMATEDVOICE, que se especifica en el miembro **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.

Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

El miembro **DeviceId** es el identificador de un dispositivo de audio cerrado. Este identificador se usa en una llamada a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir el dispositivo para la salida. Puede usar el identificador de dispositivo resultante para reproducir datos de audio digitalizados en el dispositivo de línea o teléfono.

Aunque también existe una clase de dispositivo "Wave" para dispositivos de audio de onda de bajo nivel, siempre debe usar la clase de dispositivo de onda/salida para la salida de onda de bajo nivel.

Para obtener más información sobre las funciones de onda, consulte [**funciones multimedia**](../multimedia/multimedia-functions.md).

 

 
