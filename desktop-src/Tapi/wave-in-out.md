---
description: La clase de dispositivo wave/in/out consta de dispositivos de audio dúplex completos.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: wave/in/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f526caf461cbf0bb5c3fb5490cf5e9141d9735e37e10ab632749006135a1cc9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860414"
---
# <a name="waveinout"></a>wave/in/out

La clase de dispositivo wave/in/out consta de dispositivos de audio dúplex completos. Puede acceder a estos dispositivos mediante las funciones wave, que se describen en Platform Software Development Kit (SDK). Los dispositivos de esta clase están asociados a dispositivos de línea que admiten el tipo de medio LINEMEDIAMODE AUTOMATEDVOICE, que se especifica en el miembro \_ **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.

Las [**funciones lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo el miembro **dwStringFormat** en el valor STRINGFORMAT BINARY y anexando \_ dos miembros adicionales:

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

Los **miembros DeviceInId** y **DeviceOutId** son identificadores de un dispositivo de audio cerrado. Estos identificadores se usan en una llamada a la [**función waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir el dispositivo para la salida. Puede usar el identificador de dispositivo resultante para reproducir datos de audio digitalizados en el dispositivo de línea o teléfono.

Para obtener más información sobre las funciones de onda, vea [**Funciones multimedia**](../multimedia/multimedia-functions.md).

 

 
