---
description: La clase de dispositivo TAPI/terminal consta de los dispositivos telefónicos asociados a cada terminal en una línea o el terminal en cada línea asociada a un dispositivo de teléfono. Puede tener acceso a estos dispositivos mediante las funciones dispositivo de línea TAPI o dispositivo de teléfono.
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: TAPI/terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce64da984f766e8ca3c0c47f1b60db6e9d7d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678168"
---
# <a name="tapiterminal"></a>TAPI/terminal

La clase de dispositivo TAPI/terminal consta de los dispositivos telefónicos asociados a cada terminal en una línea o el terminal en cada línea asociada a un dispositivo de teléfono. Puede tener acceso a estos dispositivos mediante las funciones dispositivo de [línea](line-device-functions.md) TAPI o [dispositivo de teléfono](phone-device-functions.md).

La función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

El miembro **adwDeviceId** es una matriz de identificadores de dispositivo de teléfono. Hay un elemento de matriz para cada terminal especificado por el miembro **dwNumTerminals** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea especificado. Cada elemento especifica el identificador del dispositivo telefónico asociado al terminal correspondiente en la línea. Si no hay ningún dispositivo de teléfono asociado a un terminal, el elemento se establece en – 1 (0xFFFFFFFF).

La función [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

El miembro **adwTerminalID** es una matriz de identificadores de terminal. Hay un elemento de matriz para cada identificador de dispositivo de línea especificado por la función [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) . Cada elemento de la matriz contiene el identificador de terminal asociado al dispositivo telefónico para el dispositivo de línea especificado. Si no hay ningún dispositivo de teléfono, el elemento se establece en – 1 (0xFFFFFFFF). Los identificadores de terminal van en el valor de cero a uno menos que el número especificado por el miembro **dwNumTerminals** en la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .

 

 



