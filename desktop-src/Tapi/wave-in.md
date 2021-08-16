---
description: La clase de dispositivo wave/in consta de dispositivos de audio para la entrada de audio de onda de bajo nivel.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24cc80d41f402abf1886e063563f272abf7992768dd62f03e64b327a7e199360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002533"
---
# <a name="wavein"></a>wave/in

La clase de dispositivo wave/in consta de dispositivos de audio para la entrada de audio de onda de bajo nivel. Puede acceder a estos dispositivos mediante las funciones wave, que se describen en Platform Software Development Kit (SDK). Los dispositivos de esta clase están asociados a dispositivos de línea que admiten el tipo de medio LINEMEDIAMODE AUTOMATEDVOICE, que se especifica en el miembro \_ **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.

Las [**funciones lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo el **miembro dwStringFormat** en el valor STRINGFORMAT BINARY y \_ anexando este miembro adicional:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

El **miembro DeviceId** es el identificador de un dispositivo de audio cerrado. Este identificador se usa en una llamada a la [**función waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir el dispositivo para la entrada. Puede usar el identificador de dispositivo resultante para grabar datos de audio digitalizados desde la línea o el dispositivo de teléfono.

Aunque también existe una clase de dispositivo "wave" para dispositivos de audio de onda de bajo nivel, siempre debe usar la clase de dispositivo wave/in para la entrada de onda de bajo nivel.

Para obtener más información sobre las funciones de onda, vea [**Funciones multimedia.**](../multimedia/multimedia-functions.md)

 

 
