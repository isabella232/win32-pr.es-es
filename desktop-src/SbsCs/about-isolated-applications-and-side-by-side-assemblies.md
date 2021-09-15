---
description: Las aplicaciones aisladas y los ensamblados en paralelo proporcionan una solución que reduce los conflictos de control de versiones de DLL. Permiten a las aplicaciones compartir ensamblados de forma segura. Para obtener más información, vea Ensamblados compartidos.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: Acerca de las aplicaciones aisladas y los ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9099ca2e41d61c84e2952661b33ca008651f8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271807"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>Acerca de las aplicaciones aisladas y los ensamblados en paralelo

[Las aplicaciones aisladas](isolated-applications.md) [y los ensamblados](about-side-by-side-assemblies-.md) en paralelo proporcionan una solución que reduce los conflictos de control de [*versiones de DLL.*](d-sbscs-gly.md) Permiten a las aplicaciones compartir ensamblados de forma segura. Para obtener más información, vea [Ensamblados compartidos](/windows/desktop/Msi/shared-assemblies).

Un ensamblado es una unidad fundamental para asignar nombres, enlazar, control de versiones, implementar o configurar un bloque de código de programación. Las aplicaciones con funcionalidad común pueden ejecutar bloques compartidos de código de programación que se conocen como módulos o ensamblados de código. Estos ensamblados de código se pueden colocar en archivos DLL o ensamblados COM. La infraestructura para el uso compartido seguro de ensamblados se conoce como uso compartido de ensamblados en paralelo.

[Los ensamblados en](about-side-by-side-assemblies-.md) paralelo son ensamblados de código descritos por manifiestos y [creados](manifests.md) para que varias versiones se puedan ejecutar al mismo tiempo sin conflictos entre sí. Cuando los desarrolladores escriben manifiestos y escriben aplicaciones para usar el uso compartido de ensamblados en [paralelo,](side-by-side-assembly-sharing.md)se pueden ejecutar varias versiones de ensamblado en el sistema y cada aplicación puede especificar qué versión de ensamblado debe usar.

Un ensamblado [*en paralelo típico es*](s-sbscs-gly.md) un único archivo DLL con un único manifiesto. Los ensamblados en paralelo almacenan la información sobre el enlace y la activación COM, tradicionalmente guardados en el Registro, en manifiestos. En algunos casos, los publicadores de ensamblados, desarrolladores de aplicaciones o administradores pueden cambiar las versiones del ensamblado especificadas en los manifiestos, de forma global o por aplicación. Para obtener más información, vea [configuración predeterminada,](default-configuration.md) [configuración del publicador](publisher-configuration.md)y [configuración por aplicación.](per-application-configuration.md)

Los desarrolladores pueden usar los ensamblados en paralelo proporcionados por Microsoft u otros publicadores de ensamblados en paralelo en sus aplicaciones. Por ejemplo, los desarrolladores pueden obtener la funcionalidad de los controles comunes actualizados, como la temas, diseñando sus aplicaciones para usar el ensamblado en paralelo que contiene Comctl32.dll 6.0. Para obtener la lista de ensamblados y manifiestos en paralelo que se envían con Windows XP, vea Ensamblados en paralelo de [Microsoft admitidos.](supported-microsoft-side-by-side-assemblies.md) Los desarrolladores también pueden crear sus propios ensamblados en paralelo. Para obtener más información, vea [Directrices para crear](guidelines-for-creating-side-by-side-assemblies.md)ensamblados en paralelo.

 

 
