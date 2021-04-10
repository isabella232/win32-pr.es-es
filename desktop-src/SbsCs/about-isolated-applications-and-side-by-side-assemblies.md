---
description: Las aplicaciones aisladas y los ensamblados en paralelo proporcionan una solución que reduce los conflictos de control de versiones de los archivos DLL. Permiten a las aplicaciones compartir ensamblados de forma segura. Para obtener más información, vea ensamblados compartidos.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: Acerca de las aplicaciones aisladas y los ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9099ca2e41d61c84e2952661b33ca008651f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156456"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>Acerca de las aplicaciones aisladas y los ensamblados en paralelo

[Las aplicaciones aisladas](isolated-applications.md) y los [ensamblados en paralelo](about-side-by-side-assemblies-.md) proporcionan una solución que reduce los conflictos de control de versiones de los [*archivos dll*](d-sbscs-gly.md). Permiten a las aplicaciones compartir ensamblados de forma segura. Para obtener más información, vea [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies).

Un ensamblado es una unidad fundamental para la nomenclatura, el enlace, el control de versiones, la implementación o la configuración de un bloque de código de programación. Las aplicaciones con funcionalidad común pueden ejecutar bloques compartidos de código de programación a los que se hace referencia como módulos o ensamblados de código. Estos ensamblados de código se pueden colocar en archivos dll o ensamblados COM. La infraestructura para el uso compartido seguro de ensamblados se conoce como uso compartido de ensamblados en paralelo.

Los [ensamblados en paralelo](about-side-by-side-assemblies-.md) son los ensamblados de código descritos por los [manifiestos](manifests.md) y creados para que varias versiones se puedan ejecutar al mismo tiempo sin entrar en conflicto entre sí. Cuando los desarrolladores crean manifiestos y escriben aplicaciones para usar el [uso compartido de ensamblados en paralelo](side-by-side-assembly-sharing.md), se pueden ejecutar varias versiones de ensamblado en el sistema y cada aplicación puede especificar la versión de ensamblado que debe usar.

Un [*ensamblado en paralelo*](s-sbscs-gly.md) típico es un único archivo dll con un solo manifiesto. Los ensamblados en paralelo almacenan la información sobre el enlace y la activación COM, que tradicionalmente se guarda en el registro, en los manifiestos. En algunos casos, las versiones del ensamblado especificado en los manifiestos se pueden cambiar, de forma global o por aplicación, por publicadores de ensamblados, desarrolladores de aplicaciones o administradores. Para obtener más información, vea [configuración predeterminada](default-configuration.md), [configuración del publicador](publisher-configuration.md)y [configuración por aplicación](per-application-configuration.md).

Los desarrolladores pueden usar los ensamblados en paralelo proporcionados por Microsoft, u otros publicadores de ensamblados en paralelo, en sus aplicaciones. Por ejemplo, los desarrolladores pueden obtener la funcionalidad de los controles comunes actualizados, como los de los mismos, diseñando sus aplicaciones para usar el ensamblado en paralelo que contiene Comctl32.dll 6,0. Para obtener la lista de ensamblados en paralelo y manifiestos que se incluyen con Windows XP, consulte [ensamblados en paralelo de Microsoft compatibles](supported-microsoft-side-by-side-assemblies.md). Los desarrolladores también pueden crear sus propios ensamblados en paralelo. Para obtener más información, vea [instrucciones para crear ensamblados en paralelo](guidelines-for-creating-side-by-side-assemblies.md).

 

 
