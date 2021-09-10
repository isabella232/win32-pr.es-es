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
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372428"
---
# <a name="obtaining-the-system-time"></a>Obtener la hora del sistema

Normalmente, antes de que una aplicación comience a usar los servicios de temporizador multimedia, recupera la hora *actual del sistema*. La hora del sistema es la hora, en milisegundos, desde que se Windows sistema operativo de Microsoft. Puede usar la función [**timeGetTime o**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) para recuperar la hora del sistema. Estas dos funciones son muy similares: **timeGetTime** devuelve la hora del sistema y **timeGetSystemTime** rellena una estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) con la hora del sistema.

 

 