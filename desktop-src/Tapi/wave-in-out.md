---
description: La clase de dispositivo de onda/salida consta de dispositivos de audio dúplex completo.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: Wave/in/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678055"
---
# <a name="waveinout"></a>Wave/in/out

La clase de dispositivo de onda/salida consta de dispositivos de audio dúplex completo. Puede acceder a estos dispositivos mediante las funciones de onda, que se describen en el kit de desarrollo de software (SDK) de la plataforma. Los dispositivos de esta clase están asociados a los dispositivos de línea que admiten el \_ tipo de medio LINEMEDIAMODE AUTOMATEDVOICE, que se especifica en el miembro **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.

Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando dos miembros adicionales:

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

Los miembros **DeviceInId** y **DeviceOutId** son identificadores de un dispositivo de audio cerrado. Estos identificadores se usan en una llamada a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir el dispositivo para la salida. Puede usar el identificador de dispositivo resultante para reproducir datos de audio digitalizados en el dispositivo de línea o teléfono.

Para obtener más información sobre las funciones de onda, consulte [**funciones multimedia**](../multimedia/multimedia-functions.md).

 

 
