---
description: La clase de dispositivo tapi/line consta de todos los dispositivos de línea. Puede acceder a estos dispositivos mediante las funciones de línea TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: tapi/line
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56478f43d1055d7bf2a382bc84611360675da97e506812a1806df4beca0aeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760737"
---
# <a name="tapiline"></a>tapi/line

La clase de dispositivo tapi/line consta de todos los dispositivos de línea. Puede acceder a estos dispositivos mediante las funciones de línea TAPI.

La [**función lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) rellena una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo el miembro **dwStringFormat** en el valor STRINGFORMAT BINARY y \_ anexando este miembro adicional.

``` syntax
DWORD dwDeviceI;  // line device identifier
```

El **miembro dwDeviceId** es el identificador del dispositivo de línea asociado al identificador de línea especificado por [**lineGetID.**](/windows/desktop/api/Tapi/nf-tapi-linegetid)

La [**función phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) también rellena una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo **dwStringFormat** en STRINGFORMAT BINARY y \_ anexando este miembro adicional:

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

El **miembro adwDeviceIds** es una matriz que contiene los identificadores de dispositivo de todos los dispositivos de línea asociados al dispositivo de teléfono. Si no hay ningún dispositivo de línea asociado, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) devuelve el valor \_ PHONEERR INVALDEVICECLASS.

 

 



