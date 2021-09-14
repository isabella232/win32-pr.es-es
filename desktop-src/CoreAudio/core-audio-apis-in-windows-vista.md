---
description: API de audio principal
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: API de audio principal
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 2cabb462d13786c874401394fa814484f79b0e3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165113"
---
# <a name="core-audio-apis"></a>API de audio principal

> [!NOTE]
> Para obtener ejemplos de código, consulte [Ejemplos de SDK que usan las API de audio principales.](./sdk-samples-that-use-the-core-audio-apis.md)

En esta documentación se proporciona información sobre las interfaces de programación de aplicaciones (API) de audio principales para la familia Windows de sistemas operativos de Microsoft. Proporciona instrucciones para que los desarrolladores de software sigan el desarrollo de aplicaciones que usan las API de audio principales en Windows Vista. Estas API eran nuevas en Windows Vista y no están disponibles en versiones anteriores de Windows.

Las API de audio principales proporcionan los medios para que las aplicaciones de audio accedan a dispositivos de punto de conexión de audio, como micrófonos y micrófonos. Las API de audio principales sirven como base para las API de audio de nivel superior, como Microsoft DirectSound y las Windows **waveXxx** multimedia. La mayoría de las aplicaciones se comunican con las API de nivel superior, pero es posible que algunas aplicaciones con requisitos especiales deba comunicarse directamente con las API de audio principales.

A partir Windows 7, se han mejorado las API existentes y se han agregado nuevas API para admitir nuevos escenarios. Las API de administración de secuencias y sesiones se han mejorado para que la aplicación ahora pueda enumerar y obtener un control extendido sobre la sesión de audio. Mediante el uso de las nuevas API, la aplicación puede implementar una experiencia de atenuación de flujo personalizada. Las nuevas API relacionadas con el dispositivo proporcionan acceso a las propiedades del controlador de los dispositivos del punto de conexión.

Esta documentación incluye las secciones siguientes.

| Sección                                                                    | Descripción                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Acerca de Windows Core Audio API](about-the-windows-core-audio-apis.md) | Proporciona información general sobre las API Windows de audio principales y describe los conceptos básicos. |
| [Guía de programación](programming-guide.md)                                 | Describe las características clave de las API de audio principales y cómo usarlas.            |
| [Referencia de programación](programming-reference.md)                         | Proporciona información de referencia de C++ para las API de audio principales.                       |

## <a name="related-topics"></a>Temas relacionados

[Tecnologías multimedia para Windows](/previous-versions/bg125389(v=msdn.10))

[Ejemplos de SDK que usan las API de audio principales](./sdk-samples-that-use-the-core-audio-apis.md)