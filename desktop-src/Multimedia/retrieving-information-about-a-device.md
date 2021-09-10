---
title: Recuperar información sobre un dispositivo
description: Recuperar información sobre un dispositivo
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- MCI_GETDEVCAPS comando
- MCI_STATUS comando
- MCI_INFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371695"
---
# <a name="retrieving-information-about-a-device"></a>Recuperar información sobre un dispositivo

Cada dispositivo responde a los comandos [**capability**](capability.md) [**(MCI \_ GETDEVCAPS),**](mci-getdevcaps.md) [**status**](status.md) [**(MCI \_ STATUS)**](mci-status.md)e [**info**](info.md) [**(MCI \_ INFO).**](mci-info.md) Estos comandos obtienen información sobre el dispositivo. Por ejemplo, el comando siguiente devuelve "true" si un **dispositivo cdaudio** puede expulsar el disco:


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Las marcas enumeradas para los comandos obligatorios y básicos proporcionan una cantidad mínima de información sobre un dispositivo. Muchos dispositivos complementan los comandos necesarios y básicos con marcas extendidas para proporcionar información adicional sobre el dispositivo.

 

 




