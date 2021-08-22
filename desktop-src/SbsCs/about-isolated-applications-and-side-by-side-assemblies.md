---
description: Las aplicaciones aisladas y los ensamblados en paralelo proporcionan una solución que reduce los conflictos de control de versiones de DLL. Permiten a las aplicaciones compartir ensamblados de forma segura. Para obtener más información, vea Ensamblados compartidos.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: Acerca de las aplicaciones aisladas y los ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ab72689173d4e8942d10dfc62259091574634227c3f4d252b0d87853ec9be7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142668"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>Acerca de las aplicaciones aisladas y los ensamblados en paralelo

[Las aplicaciones aisladas](isolated-applications.md) [y los ensamblados](about-side-by-side-assemblies-.md) en paralelo proporcionan una solución que reduce los conflictos de control de [*versiones de DLL.*](d-sbscs-gly.md) Permiten a las aplicaciones compartir ensamblados de forma segura. Para obtener más información, vea [Ensamblados compartidos.](/windows/desktop/Msi/shared-assemblies)

Un ensamblado es una unidad fundamental para asignar nombres, enlazar, control de versiones, implementar o configurar un bloque de código de programación. Las aplicaciones con funcionalidad común pueden ejecutar bloques compartidos de código de programación que se conocen como módulos o ensamblados de código. Estos ensamblados de código se pueden colocar en archivos DLL o ensamblados COM. La infraestructura para el uso compartido seguro de ensamblados se conoce como uso compartido de ensamblados en paralelo.

[Los ensamblados en](about-side-by-side-assemblies-.md) paralelo son ensamblados de código descritos por manifiestos y [creados](manifests.md) para que varias versiones se puedan ejecutar al mismo tiempo sin conflictos entre sí. Cuando los desarrolladores escriben manifiestos y escriben aplicaciones para usar el uso compartido de ensamblados en [paralelo,](side-by-side-assembly-sharing.md)se pueden ejecutar varias versiones de ensamblado en el sistema y cada aplicación puede especificar qué versión de ensamblado debe usar.

Un ensamblado [*en paralelo típico es*](s-sbscs-gly.md) un único archivo DLL con un único manifiesto. Los ensamblados en paralelo almacenan la información sobre el enlace y la activación COM, tradicionalmente guardados en el Registro, en manifiestos. En algunos casos, los publicadores de ensamblados, desarrolladores de aplicaciones o administradores pueden cambiar las versiones del ensamblado especificadas en los manifiestos, de forma global o por aplicación. Para obtener más información, [vea configuración predeterminada,](default-configuration.md) [configuración del publicador](publisher-configuration.md)y [configuración por aplicación.](per-application-configuration.md)

Los desarrolladores pueden usar los ensamblados en paralelo proporcionados por Microsoft u otros publicadores de ensamblados en paralelo en sus aplicaciones. Por ejemplo, los desarrolladores pueden obtener la funcionalidad de los controles comunes actualizados, como temas, diseñando sus aplicaciones para usar el ensamblado en paralelo que contiene Comctl32.dll 6.0. Para obtener la lista de ensamblados y manifiestos en paralelo que se envían con Windows XP, vea Supported [Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md). Los desarrolladores también pueden crear sus propios ensamblados en paralelo. Para obtener más información, vea Directrices para crear [ensamblados en paralelo.](guidelines-for-creating-side-by-side-assemblies.md)

 

 
