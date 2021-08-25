---
title: Obtener la hora del sistema
description: Obtener la hora del sistema
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- temporizadores multimedia, hora del sistema
- temporizadores, hora del sistema
- hora del sistema
- función timeGetTime
- función timeGetSystemTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45460078776732234510d7308bd1e8f490e3871334bdf950bcedd77943b430e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806475"
---
# <a name="obtaining-the-system-time"></a>Obtener la hora del sistema

Normalmente, antes de que una aplicación comience a usar los servicios de temporizador multimedia, recupera la hora *actual del sistema*. La hora del sistema es la hora, en milisegundos, desde que se inició Windows sistema operativo de Microsoft. Puede usar la función [**timeGetTime o**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) para recuperar la hora del sistema. Estas dos funciones son muy similares: **timeGetTime** devuelve la hora del sistema y **timeGetSystemTime** rellena una estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) con la hora del sistema.

 

 