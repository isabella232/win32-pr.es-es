---
description: Interoperabilidad con las API de audio heredadas
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilidad con las API de audio heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f894c20785ebd49e50765ad67ba19056f5439bd5ab8c8fc7e0bcfbdd05fe04ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875435"
---
# <a name="interoperability-with-legacy-audio-apis"></a>Interoperabilidad con las API de audio heredadas

Muchas aplicaciones existentes usan API de audio heredadas, como Direct Sound, DirectShow y las Windows multimedia. Con solo modificaciones menores, estas aplicaciones se pueden aumentar para hacer uso de [roles](device-roles.md)de [dispositivo,](session-volume-controls.md)controles de volumen de sesión y otras características de las API de audio principales de Windows Vista.

Como se describe en Componentes de [audio](user-mode-audio-components.md)en modo de usuario, las API de audio básicas sirven como base sobre la que se construyen las API de audio de nivel superior. En Windows Vista, los dispositivos de audio a los que las aplicaciones acceden a través de API de audio heredadas como Direct Sound y las funciones **Windows media waveOutXxx** y **waveInXxx** son, de hecho, dispositivos de punto de conexión de [audio](audio-endpoint-devices.md) implementados por las API de audio principales. Debido a las limitaciones inherentes en las interfaces de las API de audio heredadas, una aplicación puede acceder a algunas de las funcionalidades de los dispositivos de punto de conexión de audio a través de estas interfaces, pero no todas. En las secciones siguientes se describen técnicas para mejorar las aplicaciones existentes mediante el acceso a funcionalidades adicionales de dispositivos de punto de conexión de audio directamente a través de las API de audio principales. Estas mejoras normalmente solo requieren cambios menores en el código de aplicación existente.

En las secciones siguientes se describe cómo incorporar características de las API de audio principales en aplicaciones existentes que usan API de audio heredadas:

-   [Roles de dispositivo para aplicaciones Direct Sound](device-roles-for-directsound-applications.md)
-   [Roles de dispositivo para DirectShow aplicaciones](device-roles-for-directshow-applications.md)
-   [Roles de dispositivo para aplicaciones Windows multimedia heredadas](device-roles-for-legacy-windows-multimedia-applications.md)
-   [Eventos de audio para aplicaciones de audio heredadas](audio-events-for-legacy-audio-applications.md)
-   [Sonidos de notificación para aplicaciones de audio heredadas](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Roles de dispositivo](device-roles.md)
</dt> </dl>

 

 



