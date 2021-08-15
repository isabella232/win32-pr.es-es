---
description: La clase de dispositivo wave/out consta de dispositivos de audio para la salida de audio de onda de bajo nivel.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: wave/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3e8a82b8345e8f50e1ad18f527c82f4ece241e03c0ea7cd083dd2d2ae79282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760180"
---
# <a name="waveout"></a>wave/out

La clase de dispositivo wave/out consta de dispositivos de audio para la salida de audio de onda de bajo nivel. Puede acceder a estos dispositivos mediante las funciones wave, que se describen en Platform Software Development Kit (SDK). Los dispositivos de esta clase están asociados a dispositivos de línea que admiten el tipo de medio LINEMEDIAMODE AUTOMATEDVOICE, que se especifica en el miembro \_ **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.

Las [**funciones lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo el **miembro dwStringFormat** en el valor STRINGFORMAT BINARY y \_ anexando este miembro adicional:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

El **miembro DeviceId** es el identificador de un dispositivo de audio cerrado. Este identificador se usa en una llamada a la [**función waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir el dispositivo para la salida. Puede usar el identificador de dispositivo resultante para reproducir datos de audio digitalizados en el dispositivo de línea o teléfono.

Aunque también existe una clase de dispositivo "wave" para dispositivos de audio de onda de bajo nivel, siempre debe usar la clase de dispositivo wave/out para la salida de onda de bajo nivel.

Para obtener más información sobre las funciones de onda, vea [**Funciones multimedia.**](../multimedia/multimedia-functions.md)

 

 
