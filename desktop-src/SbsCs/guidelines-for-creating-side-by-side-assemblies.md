---
description: En las siguientes instrucciones se describe cómo crear sus propios ensamblados COM o Win32 en paralelo.
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: Directrices para crear ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19054f0c48f74a373f0ce502cb6b52374db5ded00fcde3c284fad2609ba21e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885255"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>Directrices para crear ensamblados en paralelo

En las siguientes instrucciones se describe cómo crear sus propios ensamblados COM o Win32 en paralelo. Es posible que no tenga que crear sus propios ensamblados en paralelo si la funcionalidad necesaria la proporciona uno de los ensamblados de Microsoft en [paralelo admitidos.](supported-microsoft-side-by-side-assemblies.md) En este caso, use los ensamblados proporcionados por Microsoft y siga los procedimientos para usar ensamblados en paralelo en Uso de aplicaciones aisladas y ensamblados [en paralelo.](using-isolated-applications-and-side-by-side-assemblies.md)

En primer lugar, considere si el componente es un candidato adecuado para un ensamblado en paralelo. Para obtener más información, [vea Should you provide a shared component as a side-by-side assembly?](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md) (¿Debe proporcionar un componente compartido como ensamblado en paralelo?)

Para crear un ensamblado en paralelo, siga estas instrucciones:

-   Decida qué recursos incluir en el ensamblado. Tenga en cuenta que un ensamblado consta de uno o varios archivos que siempre se proporcionan a las aplicaciones y los clientes juntos. El ensamblado actúa como la unidad fundamental utilizada para la nomenclatura, el enlace, el control de versiones, la implementación y [la configuración predeterminada.](default-configuration.md) Como regla general, cuando no está seguro de si dos recursos pertenecen al mismo ensamblado, se recomienda que se creen para ir a ensamblados independientes. Normalmente, un ensamblado en paralelo consta de un único archivo DLL.
-   Cree un manifiesto [de ensamblado](manifests.md) para el ensamblado. El manifiesto debe describir el objeto COM o las bibliotecas de tipos del ensamblado. Para obtener más información sobre lo que se debe crear en un manifiesto de ensamblado, vea [manifiestos de ensamblado](assembly-manifests.md).
-   Evalúe el uso de objetos cuando se ejecuta más de una versión del ensamblado en el sistema. Determine si las distintas versiones del ensamblado requieren estructuras de datos independientes, como archivos asignados a memoria, canalizaciones con nombre, clases y mensajes Windows registrados, memoria compartida, semáforos, exclusiones mutuas y controladores de hardware. Todas las estructuras de datos usadas en las versiones de ensamblado deben ser versiones compatibles con versiones anteriores. Decida qué estructuras de datos se pueden usar entre versiones y qué estructuras de datos deben ser privadas para una versión. Determine si las estructuras de datos compartidos requieren objetos de sincronización independientes, como semáforos y exclusiones mutuas.
-   Cree el archivo DLL para que funcione bien como un ensamblado en paralelo siguiendo las directrices de Creación de un archivo DLL para un ensamblado en [paralelo.](authoring-a-dll-for-a-side-by-side-assembly.md)
-   Cree un conjunto de archivos de encabezado y funciones auxiliares para proporcionar una manera sencilla de crear versiones de las claves del Registro que contienen el estado del ensamblado. Los ensamblados normalmente guardarán su configuración de estado en las claves del Registro. La configuración del Registro debe escribirse en una versión individual para aislar varias versiones de ensamblado que se pueden ejecutar al mismo tiempo. Diseñe el ensamblado en paralelo y el archivo DLL para almacenar y controlar correctamente el estado del ensamblado durante los escenarios de uso compartido en paralelo. Siga las instrucciones de [Authoring State Storage for Side-by-Side Assemblies](authoring-state-storage-for-side-by-side-assemblies.md).
-   Los desarrolladores de aplicaciones que [usan ensamblados privados deben](/windows/desktop/Msi/private-assemblies) proteger el directorio de la aplicación. Si la aplicación se instala mediante el instalador de Windows [,](../msi/windows-installer-portal.md)el directorio de la aplicación se puede proteger mediante la tabla LockPermissions. Normalmente, el sistema tiene acceso de lectura, escritura y ejecución a ensamblados privados. a todos los demás procesos solo se les proporciona acceso de ejecución y lectura.
-   Pruebe el ensamblado mediante escenarios con uso compartido en paralelo para asegurarse de que es un ensamblado en paralelo válido. La instalación correcta del ensamblado no es suficiente para garantizar que funcionará según lo previsto.
-   Adopte un método para numerar las actualizaciones del ensamblado. Cada ensamblado está asociado a un número de versión de cuatro partes. De izquierda a derecha, las partes principal, secundaria, de compilación y de revisión están separadas por puntos. Cambie el número principal o menor de un ensamblado para una versión incompatible con versiones anteriores. Cambie solo los elementos de compilación y revisión para los cambios compatibles con versiones anteriores del ensamblado. Por ejemplo, un desarrollador podría adoptar un método de numeración en el que todas las 1.0.0. \* Los números de versión hacen referencia a las versiones de actualización a la versión de ensamblado 1.0.0.0.

 

 
