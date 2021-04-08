---
title: Recuperación de información acerca de un dispositivo
description: Recuperación de información acerca de un dispositivo
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- Comando MCI_GETDEVCAPS
- Comando MCI_STATUS
- Comando MCI_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994550"
---
# <a name="retrieving-information-about-a-device"></a>Recuperación de información acerca de un dispositivo

Cada dispositivo responde a los comandos [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**MCI \_ status**](mci-status.md)) y [**info**](info.md) ([**MCI \_ info**](mci-info.md)). Estos comandos obtienen información sobre el dispositivo. Por ejemplo, el siguiente comando devuelve "true" Si un dispositivo **cdaudio** puede expulsar el disco:


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Las marcas enumeradas para los comandos necesarios y básicos proporcionan una cantidad mínima de información sobre un dispositivo. Muchos dispositivos complementan los comandos necesarios y básicos con marcas extendidas para proporcionar información adicional sobre el dispositivo.

 

 




