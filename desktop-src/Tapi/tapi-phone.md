---
description: La clase de dispositivo tapi/phone consta de todos los dispositivos de teléfono. Puede acceder a estos dispositivos mediante las funciones de teléfono TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: tapi/phone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b3238fb2e83d4f6e5e565f40b3ab3b124236ae2c89f879cb284d4a5997f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002723"
---
# <a name="tapiphone"></a>tapi/phone

La clase de dispositivo tapi/phone consta de todos los dispositivos de teléfono. Puede acceder a estos dispositivos mediante las funciones de teléfono TAPI.

La [**función phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellena una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo el **miembro dwStringFormat** en el valor STRINGFORMAT BINARY y \_ anexando este miembro adicional:

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

El **miembro dwDeviceId** es el identificador del dispositivo de teléfono asociado al identificador de teléfono especificado por [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).

La [**función lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) también rellena una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo **dwStringFormat** en STRINGFORMAT BINARY y \_ anexando este miembro adicional:

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

El **miembro adwDeviceIds** es una matriz que contiene los identificadores de dispositivo de todos los dispositivos de teléfono asociados al dispositivo de línea determinado. Si no hay ningún dispositivo de teléfono asociado, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) devuelve el valor \_ LINEERR INVALDEVICECLASS.

 

 



