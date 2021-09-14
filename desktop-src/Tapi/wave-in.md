---
description: La clase de dispositivo wave/in consta de dispositivos de audio para entrada de audio de onda de bajo nivel.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068688"
---
# <a name="wavein"></a>wave/in

La clase de dispositivo wave/in consta de dispositivos de audio para entrada de audio de onda de bajo nivel. Puede acceder a estos dispositivos mediante las funciones wave, que se describen en Platform Software Development Kit (SDK). Los dispositivos de esta clase están asociados a dispositivos de línea que admiten el tipo de medio LINEMEDIAMODE AUTOMATEDVOICE, que se especifica en el miembro \_ **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.

Las [**funciones lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo el **miembro dwStringFormat** en el valor STRINGFORMAT BINARY y \_ anexando este miembro adicional:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

El **miembro DeviceId** es el identificador de un dispositivo de audio cerrado. Este identificador se usa en una llamada a la [**función waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir el dispositivo para la entrada. Puede usar el identificador de dispositivo resultante para grabar datos de audio digitalizados desde la línea o el dispositivo de teléfono.

Aunque también existe una clase de dispositivo "wave" para dispositivos de audio de onda de bajo nivel, siempre debe usar la clase de dispositivo wave/in para la entrada de onda de bajo nivel.

Para obtener más información sobre las funciones de onda, vea [**Funciones multimedia**](../multimedia/multimedia-functions.md).

 

 
