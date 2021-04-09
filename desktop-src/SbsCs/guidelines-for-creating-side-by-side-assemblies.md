---
description: Las instrucciones siguientes explican cómo crear sus propios ensamblados en paralelo COM o Win32.
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: Instrucciones para crear ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8e8fd2bd31a65477b44d3afcf2156d5160a72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154102"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>Instrucciones para crear ensamblados en paralelo

Las instrucciones siguientes explican cómo crear sus propios ensamblados en paralelo COM o Win32. Es posible que no tenga que crear sus propios ensamblados en paralelo si la funcionalidad necesaria la proporciona uno de los [ensamblados en paralelo de Microsoft admitidos](supported-microsoft-side-by-side-assemblies.md). En este caso, use los ensamblados proporcionados por Microsoft y siga los procedimientos para usar ensamblados en paralelo en el [uso de aplicaciones aisladas y ensamblados en paralelo](using-isolated-applications-and-side-by-side-assemblies.md).

En primer lugar, considere si el componente hace que un candidato adecuado para un ensamblado en paralelo. Para obtener más información, vea [¿debe proporcionar un componente compartido como ensamblado simultáneo?](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md)

Para crear un ensamblado en paralelo, siga estas instrucciones:

-   Decida qué recursos incluir en el ensamblado. Tenga en cuenta que un ensamblado está compuesto de uno o varios archivos que siempre se proporcionan a las aplicaciones y a los clientes juntos. El ensamblado actúa como la unidad fundamental utilizada para la nomenclatura, el enlace, el control de versiones, la implementación y la [configuración predeterminada](default-configuration.md). Como norma general, si no está seguro de si dos recursos pertenecen al mismo ensamblado, se recomienda que se cree para entrar en ensamblados independientes. Normalmente, un ensamblado simultáneo consta de un solo archivo DLL.
-   Cree un [manifiesto](manifests.md) del ensamblado para el ensamblado. El manifiesto debe describir el objeto COM o las bibliotecas de tipos en el ensamblado. Para obtener más información sobre lo que se debe crear en un manifiesto del ensamblado, vea [manifiestos de ensamblado](assembly-manifests.md).
-   Evalúe el uso de objetos cuando se ejecute más de una versión del ensamblado en el sistema. Determine si las distintas versiones del ensamblado requieren estructuras de datos independientes, como archivos asignados a memoria, canalizaciones con nombre, mensajes y clases de Windows registrados, memoria compartida, semáforos, exclusiones mutuas y controladores de hardware. Todas las estructuras de datos utilizadas en las versiones de ensamblado deben ser versiones compatibles con versiones anteriores. Decida qué estructuras de datos se pueden usar en las versiones y qué estructuras de datos deben ser privadas para una versión. Determine si las estructuras de datos compartidas requieren objetos de sincronización independientes como semáforos y exclusiones mutuas.
-   Cree el archivo DLL para que funcione bien como un ensamblado en paralelo; para ello, siga las instrucciones de [creación de un archivo DLL para un ensamblado en paralelo](authoring-a-dll-for-a-side-by-side-assembly.md).
-   Cree un conjunto de archivos de encabezado y funciones auxiliares para proporcionar una manera sencilla de crear una versión de las claves del registro que contenga el estado del ensamblado. Los ensamblados normalmente guardan su configuración de estado en las claves del registro. La configuración del registro se debe escribir en cada versión para aislar varias versiones de ensamblado que se pueden ejecutar al mismo tiempo. Diseñe el ensamblado y el archivo DLL en paralelo para almacenar y controlar correctamente el estado del ensamblado durante los escenarios de uso compartido en paralelo. Siga las instrucciones de [creación de almacenamiento de estado para ensamblados en paralelo](authoring-state-storage-for-side-by-side-assemblies.md).
-   Los desarrolladores de aplicaciones que usan [ensamblados privados](/windows/desktop/Msi/private-assemblies) deben proteger el directorio de la aplicación. Si la aplicación se instala mediante el [Windows Installer](../msi/windows-installer-portal.md), el directorio de la aplicación se puede proteger mediante la tabla LockPermissions. Normalmente, el sistema recibe acceso de lectura, escritura y ejecución a los ensamblados privados. a todos los demás procesos solo se les proporciona acceso de ejecución y de lectura.
-   Pruebe el ensamblado mediante escenarios con el uso compartido en paralelo para asegurarse de que es un ensamblado en paralelo válido. La instalación correcta del ensamblado no es suficiente para garantizar que funcionará según lo previsto.
-   Adopte un método para numerar las actualizaciones del ensamblado. Cada ensamblado está asociado a un número de versión de cuatro partes. De izquierda a derecha, los elementos principal, secundario, de compilación y de revisión se separan por puntos. Cambiar el número principal o secundario de un ensamblado para una versión que no es compatible con versiones anteriores. Cambie solo los elementos de compilación y revisión para los cambios compatibles con versiones anteriores en el ensamblado. Por ejemplo, un desarrollador puede adoptar un método de numeración en el que todos los 1.0.0. \* los números de versión hacen referencia a las versiones de actualización de la versión 1.0.0.0 del ensamblado.

 

 
