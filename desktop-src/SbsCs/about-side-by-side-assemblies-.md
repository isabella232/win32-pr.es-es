---
description: Un ensamblado en paralelo de Windows se describe mediante manifiestos.
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: Acerca de los ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e190e6428f2e366af45a4f0961ad6ea6fb3561fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001860"
---
# <a name="about-side-by-side-assemblies"></a>Acerca de los ensamblados en paralelo

Un ensamblado en paralelo de Windows se describe mediante [manifiestos](manifests.md). Un ensamblado simultáneo contiene una colección de recursos (un grupo de archivos dll, clases de Windows, servidores COM, bibliotecas de tipos o interfaces) que siempre se proporcionan a las aplicaciones. Se describen en el manifiesto del ensamblado.

Normalmente, un ensamblado simultáneo es un solo archivo DLL. Por ejemplo, el ensamblado de COMCTL32 de Microsoft es un único archivo DLL con un manifiesto, mientras que el ensamblado de bibliotecas en tiempo de ejecución del sistema de desarrollo de Microsoft Visual C++ contiene varios archivos. Los manifiestos contienen [*metadatos*](m-sbscs-gly.md) que describen los ensamblados en paralelo y las dependencias de ensamblado en paralelo.

El sistema operativo utiliza ensamblados en paralelo como unidades fundamentales de nomenclatura, enlace, control de versiones, implementación y configuración. Cada ensamblado simultáneo tiene una identidad única. Uno de los atributos de la identidad del ensamblado es su versión. Para obtener más información, vea [versiones de ensamblado](assembly-versions.md).

A partir de Windows XP, las aplicaciones que se ejecutan al mismo tiempo pueden usar varias versiones de ensamblados en paralelo. El cargador usa los manifiestos y el número de versión del ensamblado para determinar el enlace correcto de las versiones de ensamblado a las aplicaciones. Los ensamblados en paralelo y los manifiestos funcionan con aplicaciones y el administrador en paralelo, tal y como se muestra en la ilustración siguiente.

![representación del ensamblado en paralelo típico](images/sxsman.png)

En el ejemplo anterior, Comctl32.DLL versión 6,0 y Comctl32.DLL versión 5,0 se encuentran en la caché de ensamblados en paralelo y están disponibles para las aplicaciones. Cuando una aplicación llama a para cargar el archivo DLL, el administrador en paralelo determina si la aplicación tiene una dependencia de versión descrita en un manifiesto. Si no hay ningún manifiesto relevante, el sistema carga la versión predeterminada del ensamblado. En Windows XP, la versión 5,0 de Comctl32.DLL es el valor predeterminado del sistema. Si el administrador en paralelo encuentra una dependencia de la versión 6,0 indicada en un manifiesto, esa versión se carga para ejecutarse con la aplicación.

Varios ensamblados del sistema de claves están disponibles en Microsoft como ensamblados en paralelo. Para obtener más información, consulte [ensamblados en paralelo de Microsoft compatibles](supported-microsoft-side-by-side-assemblies.md). Los desarrolladores de aplicaciones también pueden crear sus propios ensamblados en paralelo. Para obtener más información, vea [instrucciones para crear ensamblados en paralelo](guidelines-for-creating-side-by-side-assemblies.md). En muchos casos, es posible actualizar las aplicaciones existentes para usar ensamblados en paralelo sin tener que cambiar el código de la aplicación.

Se recomienda que los desarrolladores usen ensamblados en paralelo para crear [aplicaciones aisladas](isolated-applications.md)y para actualizar las aplicaciones existentes en aplicaciones aisladas por las siguientes razones:

-   Los ensamblados en paralelo reducen la posibilidad de conflictos de versión de DLL.
-   El uso compartido de ensamblados en paralelo permite que se ejecuten varias versiones de ensamblados COM o Windows al mismo tiempo.
-   Las aplicaciones y los administradores pueden actualizar la configuración del ensamblado en función de la configuración [global](publisher-configuration.md) o [por aplicación](per-application-configuration.md) después de la implementación. Por ejemplo, una aplicación se puede actualizar para utilizar un ensamblado en paralelo que incluye una actualización sin tener que volver a instalar la aplicación.

 

 



