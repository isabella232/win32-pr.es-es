---
description: Un Windows ensamblado en paralelo se describe mediante manifiestos.
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: Acerca de los ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e190e6428f2e366af45a4f0961ad6ea6fb3561fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271799"
---
# <a name="about-side-by-side-assemblies"></a>Acerca de los ensamblados en paralelo

Un Windows ensamblado en paralelo se describe mediante [manifiestos](manifests.md). Un ensamblado en paralelo contiene una colección de recursos (un grupo de archivos DLL, clases Windows, servidores COM, bibliotecas de tipos o interfaces) que siempre se proporcionan a las aplicaciones juntas. Se describen en el manifiesto del ensamblado.

Normalmente, un ensamblado en paralelo es un único archivo DLL. Por ejemplo, el ensamblado COMCTL32 de Microsoft es un único archivo DLL con un manifiesto, mientras que el ensamblado Microsoft Visual C++ bibliotecas en tiempo de ejecución del sistema de desarrollo de Microsoft Visual C++ contiene varios archivos. Los manifiestos [*contienen metadatos*](m-sbscs-gly.md) que describen ensamblados en paralelo y dependencias de ensamblado en paralelo.

El sistema operativo usa los ensamblados en paralelo como unidades fundamentales de nomenclatura, enlace, control de versiones, implementación y configuración. Cada ensamblado en paralelo tiene una identidad única. Uno de los atributos de la identidad del ensamblado es su versión. Para obtener más información, vea [Versiones de ensamblado.](assembly-versions.md)

A partir Windows XP, las aplicaciones que ejecutan al mismo tiempo pueden usar varias versiones de ensamblados en paralelo. El cargador usa los manifiestos y el número de versión del ensamblado para determinar el enlace correcto de las versiones de ensamblado a las aplicaciones. Los ensamblados y manifiestos en paralelo funcionan con las aplicaciones y el administrador en paralelo, como se muestra en la ilustración siguiente.

![representación del ensamblado en paralelo típico](images/sxsman.png)

En el ejemplo anterior, tanto Comctl32.DLL versión 6.0 como Comctl32.DLL versión 5.0 están en la caché de ensamblados en paralelo y están disponibles para las aplicaciones. Cuando una aplicación llama a para cargar el archivo DLL, el administrador en paralelo determina si la aplicación tiene una dependencia de versión descrita en un manifiesto. Si no hay ningún manifiesto pertinente, el sistema carga la versión predeterminada del ensamblado. Para Windows XP, la versión 5.0 de Comctl32.DLL es el valor predeterminado del sistema. Si el administrador en paralelo encuentra una dependencia de la versión 6.0 indicada en un manifiesto, esa versión se carga para ejecutarse con la aplicación.

Microsoft está haciendo que varios ensamblados clave del sistema estén disponibles como ensamblados en paralelo. Para obtener más información, vea Ensamblados en paralelo [de Microsoft admitidos.](supported-microsoft-side-by-side-assemblies.md) Los desarrolladores de aplicaciones también pueden crear sus propios ensamblados en paralelo. Para obtener más información, vea Directrices para crear [ensamblados en paralelo.](guidelines-for-creating-side-by-side-assemblies.md) En muchos casos, es posible actualizar las aplicaciones existentes para usar ensamblados en paralelo sin tener que cambiar el código de la aplicación.

Se recomienda a los desarrolladores usar ensamblados [](isolated-applications.md)en paralelo para crear aplicaciones aisladas y actualizar las aplicaciones existentes en aplicaciones aisladas por los siguientes motivos:

-   Los ensamblados en paralelo reducen la posibilidad de conflictos de versión de DLL.
-   El uso compartido de ensamblados en paralelo permite que varias versiones de ensamblados COM o Windows se ejecuten al mismo tiempo.
-   Las aplicaciones y los administradores pueden actualizar la configuración de ensamblados de forma [global](publisher-configuration.md) o por [aplicación](per-application-configuration.md) después de la implementación. Por ejemplo, una aplicación se puede actualizar para usar un ensamblado en paralelo que incluya una actualización sin tener que volver a instalar la aplicación.

 

 



