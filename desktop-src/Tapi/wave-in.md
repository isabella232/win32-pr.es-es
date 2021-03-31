---
description: La clase de dispositivo de entrada y salida consta de dispositivos de audio para entradas de audio de onda de bajo nivel.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: onda/en
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278556"
---
# <a name="wavein"></a>onda/en

La clase de dispositivo de entrada y salida consta de dispositivos de audio para entradas de audio de onda de bajo nivel. Puede acceder a estos dispositivos mediante las funciones de onda, que se describen en el kit de desarrollo de software (SDK) de la plataforma. Los dispositivos de esta clase están asociados a los dispositivos de línea que admiten el \_ tipo de medio LINEMEDIAMODE AUTOMATEDVOICE, que se especifica en el miembro **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.

Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

El miembro **DeviceId** es el identificador de un dispositivo de audio cerrado. Este identificador se usa en una llamada a la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir el dispositivo para la entrada. Puede usar el identificador de dispositivo resultante para grabar datos de audio digitalizados desde el dispositivo de línea o teléfono.

Aunque también existe una clase de dispositivo "Wave" para dispositivos de audio de onda de bajo nivel, siempre debe usar la clase de dispositivo de onda/entrada para la entrada de onda de bajo nivel.

Para obtener más información sobre las funciones de onda, consulte [**funciones multimedia**](../multimedia/multimedia-functions.md).

 

 
