---
description: API de audio principales
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: API de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 83488233240121ba2edcfd677484df67a452e479
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105660109"
---
# <a name="core-audio-apis"></a>API de audio principales

> [!NOTE]
> Para ver ejemplos de código, consulte [ejemplos de SDK que usan las API de audio principales](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis).

En esta documentación se proporciona información sobre las interfaces de programación de aplicaciones (API) de audio principales para la familia de sistemas operativos Microsoft Windows. Proporciona directrices para que los desarrolladores de software sigan el desarrollo de aplicaciones que usan las API de audio principales en Windows Vista. Estas API eran nuevas en Windows Vista y no están disponibles en versiones anteriores de Windows.

Las API de audio principales proporcionan los medios para que las aplicaciones de audio accedan a dispositivos de punto de conexión de audio, como auriculares y micrófonos. Las API de audio principales sirven como base para las API de audio de nivel superior, como Microsoft DirectSound y las funciones de **waveXxx** multimedia de Windows. La mayoría de las aplicaciones se comunican con las API de nivel superior, pero es posible que algunas aplicaciones con requisitos especiales deban comunicarse directamente con las API de audio principales.

A partir de Windows 7, las API existentes se han mejorado y se han agregado nuevas API para admitir nuevos escenarios. Las API de administración de transmisiones y sesiones se han mejorado para que la aplicación pueda enumerar y obtener el control extendido de la sesión de audio. Mediante el uso de las nuevas API, la aplicación puede implementar una experiencia de atenuación de secuencia personalizada. Las nuevas API relacionadas con el dispositivo proporcionan acceso a las propiedades del controlador de los dispositivos de punto de conexión.

En esta documentación se incluyen las siguientes secciones.

| Sección                                                                    | Descripción                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Acerca de las API de audio de Windows Core](about-the-windows-core-audio-apis.md) | Proporciona información general sobre las API de audio de Windows Core y describe los conceptos básicos. |
| [Guía de programación](programming-guide.md)                                 | Describe las características clave de las API de audio principales y cómo usarlas.            |
| [Referencia de programación](programming-reference.md)                         | Proporciona información de referencia de C++ para las API de audio principales.                       |

## <a name="related-topics"></a>Temas relacionados

[Tecnologías multimedia para Windows](/previous-versions/bg125389(v=msdn.10))

[Ejemplos de SDK que usan las API de audio principales](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis)
