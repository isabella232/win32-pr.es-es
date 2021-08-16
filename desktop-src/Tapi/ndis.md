---
description: La clase de dispositivo ndis consta de dispositivos que se pueden asociar con controladores de control de acceso multimedia (MAC) de especificación de interfaz de controlador de red (NDIS) para admitir las comunicaciones de red. Puede acceder a estos dispositivos mediante funciones.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: Ndis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dda773591a3e3766a77b00925b9c15eacc5f45188900b12d6b9744c52f238ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761344"
---
# <a name="ndis"></a>Ndis

La clase de dispositivo ndis consta de dispositivos que se pueden asociar con controladores de control de acceso multimedia (MAC) de especificación de interfaz de controlador de red (NDIS) para admitir las comunicaciones de red. Puede acceder a estos dispositivos mediante funciones.

Las [**funciones lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo el **miembro dwStringFormat** en el valor STRINGFORMAT BINARY y anexando estos miembros \_ adicionales:

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

El **miembro hDevice** es el identificador que se pasa a un EQUIPO MAC, como el MAC asincrónico para redes de acceso telefónico, para asociar una conexión de red a la conexión de llamada o módem. El **miembro szDeviceType** es una cadena terminada en NULL que especifica el nombre del dispositivo asociado al identificador.

 

 



