---
title: Novedades (Windows controles)
description: En este tema se describen las diferencias en la compatibilidad con temas y estilos visuales entre Windows 8 versiones anteriores de Windows .
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7801eea011aabb05663cc2e29f18e0dd58edc9fddc4f32014fcffb96c559cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957554"
---
# <a name="whats-new-windows-controls"></a>Novedades (Windows controles)

En este tema se describen las diferencias en la compatibilidad con temas y estilos visuales entre Windows 8 versiones anteriores de Windows .

## <a name="through-windows-7"></a>Hasta Windows 7

A Windows 7 Windows, los estilos visuales están encendidos de forma predeterminada, pero el usuario puede desactivarlos seleccionando un tema clásico o desactivando el servicio Temas. Cuando los estilos visuales están desactivados, toda la interfaz de usuario obtiene el aspecto clásico y la mayoría de las API de estilos visuales no están disponibles. Los estilos visuales desactivados se han conservado Windows 7 para admitir los distintos temas de contraste alto, así como Windows tema clásico. Si desea admitir estilos visuales y temas de contraste alto en la misma aplicación, normalmente debe mantener dos rutas de acceso de código independientes para representar controles.

## <a name="windows-8-and-later"></a>Windows 8 y versiones posteriores

En Windows 8, los estilos visuales no se pueden desactivar a través de la página **Personalización** de **pc Configuración** o desactivando el servicio Temas. Windows El modo clásico ya no existe y el modo de contraste alto se ha modificado para que funcione con estilos visuales. Debido a estos cambios, las aplicaciones que tienen como destino Windows 8 ya no necesitan dos rutas de acceso de código independientes para admitir estilos visuales y temas de contraste alto.

Los estilos visuales de Windows 8 compatibilidad con versiones anteriores para Windows de tema clásico. Cualquier código de representación de la interfaz de usuario que funcione en versiones anteriores seguirá funcionando en Windows 8 sin modificaciones.

En Windows 8, si desea que la aplicación admita los temas de contraste alto basados en estilos visuales, debe incluir el GUID de Windows 8 en la sección de compatibilidad del manifiesto de aplicación. De lo contrario, el sistema asume que la aplicación está diseñada para una versión anterior y representa el área de cliente simulando Windows temas clásicos de contraste alto. Para obtener más información, [vea Supporting contraste alto Themes](supporting-high-contrast-themes.md).

Al igual que en versiones anteriores, Windows 8 admite tanto la versión 5 como la versión 6 de los controles comunes, siendo la versión 5 la predeterminada. Dado que solo la versión 6 admite estilos visuales, debe especificar la versión 6 en el manifiesto de aplicación si desea que los estilos visuales se apliquen a los controles comunes del área de cliente de la aplicación. Para obtener más información, vea [Habilitar estilos visuales.](cookbook-overview.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar los estilos visuales](cookbook-overview.md)
</dt> <dt>

[Compatibilidad con contraste alto temas](supporting-high-contrast-themes.md)
</dt> <dt>

[Estilos visuales](themes-overview.md)
</dt> <dt>

[Información general sobre los estilos visuales](visual-styles-overview.md)
</dt> </dl>

 

 




