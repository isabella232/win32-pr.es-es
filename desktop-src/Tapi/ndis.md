---
description: La clase de dispositivo NDIS se compone de dispositivos que se pueden asociar a los controladores de Media Access Control (MAC) de la especificación de interfaz de controlador de red (NDIS) para admitir las comunicaciones de red. Puede tener acceso a estos dispositivos mediante funciones.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: NDIS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0be1a69f98f9a4ff8cdc2f8ea173b208c0011d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677475"
---
# <a name="ndis"></a>NDIS

La clase de dispositivo NDIS se compone de dispositivos que se pueden asociar a los controladores de Media Access Control (MAC) de la especificación de interfaz de controlador de red (NDIS) para admitir las comunicaciones de red. Puede tener acceso a estos dispositivos mediante funciones.

Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando estos miembros adicionales:

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

El miembro **hDevice** es el identificador que se va a pasar a un equipo Mac, como el equipo Mac asincrónico para las redes de acceso telefónico, para asociar una conexión de red con la conexión de llamada o módem. El miembro **szDeviceType** es una cadena terminada en null que especifica el nombre del dispositivo asociado al identificador.

 

 



