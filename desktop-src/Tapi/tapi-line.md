---
description: La clase de dispositivo TAPI/línea consta de todos los dispositivos de línea. Puede tener acceso a estos dispositivos con las funciones de línea TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928cfa6144e9a701d6462519d2aa9d590a54a511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678234"
---
# <a name="tapiline"></a>TAPI/línea

La clase de dispositivo TAPI/línea consta de todos los dispositivos de línea. Puede tener acceso a estos dispositivos con las funciones de línea TAPI.

La función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional.

``` syntax
DWORD dwDeviceI;  // line device identifier
```

El miembro **dwDeviceId** es el identificador del dispositivo de línea asociado al identificador de línea proporcionado por [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

La función [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) también rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo **DWSTRINGFORMAT** en \_ el binario STRINGFORMAT y anexando este miembro adicional:

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

El miembro **adwDeviceIds** es una matriz que contiene los identificadores de dispositivos de todos los dispositivos de línea asociados al dispositivo telefónico. Si no hay dispositivos de línea asociados, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) devuelve el valor de INVALDEVICECLASS de PHONEERR \_ .

 

 



