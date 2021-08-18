---
title: API UpdateOrchestrator
description: UpdateOrchestrator programa las actualizaciones automáticas de software con el impacto en el usuario en mente.
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: 6460446397af168a4098a7203179d5587d4dcd9a3cea813991648a5083d07334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966132"
---
# <a name="updateorchestrator-api"></a>UpdateOrchestrator API

**UpdateOrchestrator programa** las actualizaciones de software automáticas con el impacto en el usuario en mente. Esta API permite programar la descarga e instalación automáticas, junto con sus requisitos, para ejecutar actualizaciones en un momento óptimo que minimice el impacto presente del usuario. Estas características benefician especialmente a los sistemas de menor rendimiento con recursos informáticos limitados o más lentos.

Windows 19H1 incluye una solución de primera generación para los casos de uso de actualizaciones automáticas de software que adoptaron las actualizaciones del sistema operativo y las actualizaciones de aplicaciones de la Tienda, y expone una versión inicial de "acceso limitado" de esta API para un conjunto selecto de actualizadores de aplicaciones de "modo de usuario", como se describe a continuación.

## <a name="features"></a>Características

- Registra dinámicamente los actualizadores de software
 
- Invoca los actualizadores de software registrados en momentos óptimos, como durante la ausencia del usuario, para actualizar "aplicaciones en modo de usuario".
    - Incluye la capacidad de "mantenerse activo" en la alimentación de ca para reducir aún más el impacto en la salida del usuario.

- Opera en un modelo de confianza que solo invoca actualizadores de software registrados de terceros de confianza.
    - Existen riesgos considerables al exponer UpdateOrchestrator a todos y cada uno de los llamadores, como la actualización del firmware del BIOS o los controladores cuando un usuario no está presente.  UpdateOrchestrator incluye un modelo de confianza para mitigar estos riesgos.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

> [!IMPORTANT]
> UpdateOrchestrator API es actualmente una [característica de acceso limitado.](/uwp/api/windows.applicationmodel.limitedaccessfeatures) Esta API estará disponible públicamente en una versión futura.

Use UpdateOrchestrator API si ya tiene actualizadores de software en segundo plano para aplicaciones de "modo de usuario" de Win32, como el actualizador de Adobe para Acrobat Reader o Valve's Steam. Esta interfaz no es necesaria para las aplicaciones para UWP o store, ya Microsoft Store aprovecha esta funcionalidad para las actualizaciones de software.

Para proporcionar la mejor experiencia del cliente, esta versión de API inicial está en el ámbito de un conjunto selecto de actualizadores registrados que cumplen los criterios siguientes:

- Actualizaciones solo para aplicaciones de "modo de usuario"
- No implicar bios, firmware, dispositivo o controladores de software
    - La actualización de bios, firmware o controladores de dispositivo o software que no han pasado un criterio de calidad común supone un riesgo considerable, especialmente cuando un usuario no está presente. 
- Participar en el uso de esta API implica poder dar fe de todo el contenido descargado e instalado por los actualizadores de software en segundo plano en los sistemas de usuarios a través de auditorías. 

Esta API se puede modificar significativamente antes de la versión pública.   Mientras updateOrchestrator API está en desarrollo, esta versión inicial como característica de acceso limitado es solo para los actualizadores que cumplen los criterios anteriores en este momento.

Nuestro objetivo es mejorar la funcionalidad de esta API y reducir el impacto de varios actualizadores de software automáticos en Windows. Agradecemos su opinión a través de esta [**breve**](https://aka.ms/UOAPISurvey) encuesta para ayudarnos a comprender cómo UpdateOrchestrator API puede satisfacer mejor las necesidades de los desarrolladores.

