---
title: Obtener la hora del sistema
description: Obtener la hora del sistema
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- temporizadores multimedia, hora del sistema
- temporizadores, hora del sistema
- hora del sistema
- timeGetTime función)
- timeGetSystemTime función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487571"
---
# <a name="obtaining-the-system-time"></a>Obtener la hora del sistema

Normalmente, antes de que una aplicación empiece a usar los servicios de temporizador multimedia, recupera la *hora actual del sistema*. La hora del sistema es el tiempo, en milisegundos, transcurrido desde que se inició el sistema operativo Microsoft Windows. Puede usar la función [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) o [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) para recuperar la hora del sistema. Estas dos funciones son muy similares: **timeGetTime** devuelve la hora del sistema y **timeGetSystemTime** rellena una estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) con la hora del sistema.

 

 