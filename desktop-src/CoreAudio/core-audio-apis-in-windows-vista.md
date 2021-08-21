---
description: API de audio principales
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: API de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 69c0c83700dabd3aa0298bcd6474b95c4c38bdf933c9867a4c639edee1e43379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077649"
---
# <a name="core-audio-apis"></a>API de audio principales

> [!NOTE]
> Para obtener ejemplos de código, consulte [Ejemplos de SDK que usan las API de audio principales.](./sdk-samples-that-use-the-core-audio-apis.md)

En esta documentación se proporciona información sobre las interfaces de programación de aplicaciones (API) de audio principales para la familia de sistemas operativos Windows Microsoft. Proporciona instrucciones para que los desarrolladores de software sigan el desarrollo de aplicaciones que usan las API de audio principales en Windows Vista. Estas API eran nuevas en Windows Vista y no están disponibles en versiones anteriores de Windows.

Las API de audio principales proporcionan los medios para que las aplicaciones de audio accedan a dispositivos de punto de conexión de audio, como auriculares y micrófonos. Las API de audio básicas sirven como base para las API de audio de nivel superior, como Microsoft Direct Sound y las Windows **waveXxx** multimedia. La mayoría de las aplicaciones se comunican con las API de nivel superior, pero es posible que algunas aplicaciones con requisitos especiales deba comunicarse directamente con las API de audio principales.

A partir Windows 7, se han mejorado las API existentes y se han agregado nuevas API para admitir nuevos escenarios. Las API de administración de secuencias y sesiones se han mejorado para que la aplicación ahora pueda enumerar y obtener un mayor control sobre la sesión de audio. Mediante el uso de las nuevas API, la aplicación puede implementar una experiencia de atenuación de secuencia personalizada. Las nuevas API relacionadas con el dispositivo proporcionan acceso a las propiedades del controlador de los dispositivos de punto de conexión.

Esta documentación incluye las secciones siguientes.

| Sección                                                                    | Descripción                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Acerca de Windows Core Audio API](about-the-windows-core-audio-apis.md) | Proporciona información general sobre las API de audio Windows core y describe los conceptos básicos. |
| [Guía de programación](programming-guide.md)                                 | Describe las características clave de las API de audio principales y cómo usarlas.            |
| [Referencia de programación](programming-reference.md)                         | Proporciona información de referencia de C++ para las API de audio principales.                       |

## <a name="related-topics"></a>Temas relacionados

[Tecnologías multimedia para Windows](/previous-versions/bg125389(v=msdn.10))

[Ejemplos de SDK que usan las API de audio principales](./sdk-samples-that-use-the-core-audio-apis.md)