---
description: Interoperabilidad con las API de audio heredadas
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilidad con las API de audio heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000719"
---
# <a name="interoperability-with-legacy-audio-apis"></a>Interoperabilidad con las API de audio heredadas

Muchas aplicaciones existentes usan las API de audio heredadas como DirectSound, DirectShow y las funciones multimedia de Windows. Con solo modificaciones menores, estas aplicaciones se pueden aumentar para hacer uso de [roles de dispositivo](device-roles.md), [controles de volumen de sesión](session-volume-controls.md)y otras características de las API de audio principales en Windows Vista.

Como se describe en [componentes de audio de modo de usuario](user-mode-audio-components.md), las API de audio principales sirven como base para la creación de las API de audio de nivel superior. En Windows Vista, los dispositivos de audio a los que las aplicaciones acceden a través de las API de audio heredadas como DirectSound y las funciones **waveOutXxx** y **waveInXxx** de Windows Media son, de hecho, [dispositivos de punto de conexión](audio-endpoint-devices.md) de audio implementados por las API de audio principales. Debido a las limitaciones inherentes en las interfaces de las API de audio heredadas, una aplicación puede acceder a algunas de las funcionalidades de los dispositivos de punto de conexión de audio, pero no a ellas, a través de estas interfaces. En las secciones siguientes se describen técnicas para mejorar las aplicaciones existentes mediante el acceso a funciones adicionales de los dispositivos de punto de conexión de audio directamente a través de las API de audio principales. Estas mejoras normalmente solo requieren pequeños cambios en el código de aplicación existente.

En las secciones siguientes se describe cómo incorporar características de las API de audio principales en aplicaciones existentes que usan las API de audio heredadas:

-   [Roles de dispositivo para aplicaciones DirectSound](device-roles-for-directsound-applications.md)
-   [Roles de dispositivo para aplicaciones de DirectShow](device-roles-for-directshow-applications.md)
-   [Roles de dispositivo para aplicaciones multimedia heredadas de Windows](device-roles-for-legacy-windows-multimedia-applications.md)
-   [Eventos de audio para aplicaciones de audio heredadas](audio-events-for-legacy-audio-applications.md)
-   [Sonidos de notificación para aplicaciones de audio heredadas](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Roles de dispositivo](device-roles.md)
</dt> </dl>

 

 



