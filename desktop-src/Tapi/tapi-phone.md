---
description: La clase de dispositivo tapi/phone consta de todos los dispositivos de teléfono. Puede acceder a estos dispositivos mediante las funciones de teléfono TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: tapi/phone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476313"
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

 

 



