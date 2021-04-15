---
title: Novedades (controles de Windows)
description: En este tema se describen las diferencias entre la compatibilidad con temas y estilos visuales entre Windows 8 y versiones anteriores de Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488711"
---
# <a name="whats-new-windows-controls"></a>Novedades (controles de Windows)

En este tema se describen las diferencias entre la compatibilidad con temas y estilos visuales entre Windows 8 y versiones anteriores de Windows.

## <a name="through-windows-7"></a>A través de Windows 7

A través de Windows 7, los estilos visuales están activados de forma predeterminada, pero el usuario puede desactivarlos seleccionando el tema clásico de Windows o desactivando el servicio de temas. Cuando los estilos visuales están desactivados, todas las interfaces de usuario obtienen el aspecto clásico y la mayoría de las API de estilos visuales no están disponibles. El modo de estilos visuales desactivado se ha mantenido a través de Windows 7 para admitir los diversos temas de contraste alto, así como el tema clásico de Windows. Si desea admitir tanto estilos visuales como temas de contraste alto en la misma aplicación, normalmente necesitará mantener dos rutas de acceso de código independientes para la representación de controles.

## <a name="windows-8-and-later"></a>Windows 8 y versiones posteriores

En Windows 8, los estilos visuales no se pueden desactivar a través de la página **Personalización** de la **configuración del equipo** o desactivando el servicio temas. El modo clásico de Windows ya no existe y se ha modificado el modo de contraste alto para trabajar con estilos visuales. Debido a estos cambios, las aplicaciones destinadas solo a Windows 8 ya no necesitan dos rutas de acceso de código independientes para admitir los estilos visuales y los temas de contraste alto.

Los estilos visuales de Windows 8 incluyen compatibilidad con versiones anteriores del modo de Windows clásico. Cualquier código de representación de la interfaz de usuario que funcione en versiones anteriores continuará funcionando en Windows 8 sin modificaciones.

En Windows 8, si desea que la aplicación admita los temas de contraste alto basados en estilos visuales, debe incluir el GUID de Windows 8 en la sección de compatibilidad del manifiesto de aplicación. De lo contrario, el sistema supone que la aplicación está diseñada para una versión anterior y representa el área cliente mediante la simulación de los temas de contraste alto de Windows clásico. Para obtener más información, consulte [compatibilidad con temas de contraste alto](supporting-high-contrast-themes.md).

Como en versiones anteriores, Windows 8 es compatible con la versión 5 y la versión 6 de los controles comunes, siendo la versión 5 la predeterminada. Dado que solo la versión 6 admite estilos visuales, debe especificar la versión 6 en el manifiesto de aplicación si desea que los estilos visuales se apliquen a los controles comunes en el área cliente de la aplicación. Para obtener más información, vea [habilitar estilos visuales](cookbook-overview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar los estilos visuales](cookbook-overview.md)
</dt> <dt>

[Compatibilidad con temas de contraste alto](supporting-high-contrast-themes.md)
</dt> <dt>

[Estilos visuales](themes-overview.md)
</dt> <dt>

[Información general sobre los estilos visuales](visual-styles-overview.md)
</dt> </dl>

 

 




