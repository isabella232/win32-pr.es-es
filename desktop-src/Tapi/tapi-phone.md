---
description: La clase de dispositivo TAPI/teléfono se compone de todos los dispositivos telefónicos. Puede tener acceso a estos dispositivos mediante las funciones de teléfono de TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI/teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002444"
---
# <a name="tapiphone"></a>TAPI/teléfono

La clase de dispositivo TAPI/teléfono se compone de todos los dispositivos telefónicos. Puede tener acceso a estos dispositivos mediante las funciones de teléfono de TAPI.

La función [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

El miembro **dwDeviceId** es el identificador del dispositivo telefónico asociado al identificador de teléfono proporcionado por [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).

La función [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) también rellena una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo **DWSTRINGFORMAT** en \_ el binario STRINGFORMAT y anexando este miembro adicional:

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

El miembro **adwDeviceIds** es una matriz que contiene los identificadores de dispositivos de todos los dispositivos telefónicos asociados con el dispositivo de línea especificado. Si no hay ningún dispositivo telefónico asociado, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) devuelve el \_ valor INVALDEVICECLASS de LINEERR.

 

 



