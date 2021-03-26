---
title: API UpdateOrchestrator
description: UpdateOrchestrator programa las actualizaciones de software automáticas teniendo en cuenta el impacto de los usuarios.
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: a172cccdc56d2c645bb4e7d048066ca34aea07ba
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "103913913"
---
# <a name="updateorchestrator-api"></a>API de UpdateOrchestrator

**UpdateOrchestrator** programa las actualizaciones de software automáticas teniendo en cuenta el impacto de los usuarios. Esta API le permite programar la descarga e instalación automáticas, junto con sus requisitos para ejecutar actualizaciones en un momento óptimo, lo que minimiza el impacto presente por el usuario. Estas características benefician especialmente a sistemas de rendimiento inferiores con recursos informáticos limitados o lentos.

Windows 19H1 incluye una solución de primera generación para los casos de uso de actualizaciones de software automáticas que fueron adoptados por las actualizaciones del sistema operativo y las actualizaciones de aplicaciones de la tienda, y expone una versión inicial de "acceso limitado" de esta API para un conjunto seleccionado de aplicaciones de "modo de usuario" como se describe a continuación.

## <a name="features"></a>Características

- Registra dinámicamente los actualizadores de software
 
- Invoca a los actualizadores de software registrados durante las horas óptimas, como por ejemplo, durante la ausencia del usuario, para actualizar las "aplicaciones en modo de usuario".
    - Incluye la capacidad de "mantenerse activo" sobre la alimentación de CA para reducir aún más el impacto de los usuarios.

- Funciona en un modelo de confianza que solo invoca los actualizadores de software registrados de terceros de confianza.
    - La exposición de UpdateOrchestrator a cualquiera de los autores de llamadas, como la actualización del firmware o los controladores de BIOS, es importante cuando un usuario no está presente.  UpdateOrchestrator incluye un modelo de confianza para mitigar estos riesgos.

## <a name="developer-audience"></a>Audiencia de los desarrolladores

> [!IMPORTANT]
> La API de UpdateOrchestrator es actualmente una [característica de acceso limitado](/uwp/api/windows.applicationmodel.limitedaccessfeatures). Esta API estará disponible públicamente en una versión futura.

Use la API de UpdateOrchestrator si ya dispone de actualizadores de software en segundo plano para aplicaciones de "modo de usuario" de Win32 como el actualizador de Adobe para Acrobat Reader o la secuencia de la válvula. Esta interfaz no es necesaria para las aplicaciones de UWP o Store, ya que el Microsoft Store ya aprovecha esta funcionalidad para las actualizaciones de software.

Para proporcionar la mejor experiencia de cliente, esta versión inicial de la API tiene como ámbito un conjunto seleccionado de actualizadores registrados que cumplen los siguientes criterios:

- Actualizaciones solo para aplicaciones de ' modo de usuario '
- No implique controladores de BIOS/firmware/dispositivo o software
    - La actualización del BIOS, el firmware o los controladores de dispositivo o software que no han superado los criterios de calidad comunes suponen un riesgo sustancial, especialmente cuando un usuario no está presente. 
- Al participar en el uso de esta API, se puede realizar una comprobación de todo el contenido descargado e instalado por los actualizadores de software en segundo plano de los sistemas de los usuarios a través de auditorías. 

Esta API se puede modificar significativamente antes de la versión pública.   Mientras que la API de UpdateOrchestrator está en desarrollo, esta versión inicial como característica de acceso limitado solo es para los actualizadores que cumplen los criterios anteriores en este momento.

Nuestro objetivo es mejorar la funcionalidad de esta API y reducir el impacto de varios actualizadores de software automáticos en Windows. Agradecemos su entrada a través de esta [**breve encuesta**](https://aka.ms/UOAPISurvey) para ayudarnos a comprender cómo UpdateOrchestrator API puede atender mejor sus necesidades de desarrollo.

