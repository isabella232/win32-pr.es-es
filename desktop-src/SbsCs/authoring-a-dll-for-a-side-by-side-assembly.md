---
description: Al crear sus propios ensamblados en paralelo, siga las instrucciones para crear ensamblados en paralelo.
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: Crear archivos DLL para ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa15f3876c60ce55be00d60d8f417eb0c2cbf6ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277353"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a>Crear archivos DLL para ensamblados en paralelo

Al crear sus propios ensamblados en paralelo, siga las [directrices para crear ensamblados en paralelo](guidelines-for-creating-side-by-side-assemblies.md) y crear cualquier dll que se use en el ensamblado según las siguientes directrices:

-   Los archivos dll deben diseñarse de modo que se puedan ejecutar varias versiones al mismo tiempo y en el mismo proceso sin interferir entre sí. Por ejemplo, muchas aplicaciones hospedan varios complementos, cada uno de los cuales requiere una versión diferente de un componente. El desarrollador debe diseñar y probar el ensamblado en paralelo para asegurarse de que varias versiones del componente funcionan correctamente cuando se ejecutan al mismo tiempo en el mismo proceso.

-   Si tiene previsto proporcionar el componente como componente compartido en sistemas anteriores a Windows XP, debe continuar instalando el componente en estos sistemas como un componente compartido de una sola instancia. En este caso, debe asegurarse de que el componente sea compatible con versiones anteriores.

-   Evalúe el uso de objetos cuando se ejecute más de una versión del ensamblado en el sistema. Determine si las distintas versiones del ensamblado requieren estructuras de datos independientes, como archivos asignados a memoria, canalizaciones con nombre, mensajes y clases de Windows registrados, memoria compartida, semáforos, exclusiones mutuas y controladores de hardware. Todas las estructuras de datos utilizadas en las versiones de ensamblado deben ser compatibles con versiones anteriores. Decida qué estructuras de datos se pueden usar en las versiones y qué estructuras de datos deben ser privadas para una versión. Determine si las estructuras de datos compartidas requieren objetos de sincronización independientes, como semáforos y exclusiones mutuas.

-   Algunos objetos, como las clases de ventana y los átomos, tienen un nombre único para cada proceso. Los objetos como las clases de ventana deben tener versiones para cada ensamblado mediante el manifiesto. Para objetos como átomos, use identificadores específicos de la versión a menos que planee compartir entre versiones. Si usa identificadores específicos de la versión, use el número de versión de cuatro partes.

-   No incluya código de registro automático en ningún archivo DLL. Un archivo DLL de un ensamblado en paralelo no se puede registrar automáticamente.

-   Defina todos los nombres específicos de la versión en el archivo DLL con \# instrucciones de definición. Esto permite cambiar todas las claves del registro de una ubicación. Al liberar una nueva versión del ensamblado, solo tiene que cambiar esta instrucción de \# definición. Por ejemplo:

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   Almacene los datos no persistentes en el directorio temporal.

-   No coloque los datos de usuario en ubicaciones globales. Mantenga los datos de la aplicación separados de los datos del usuario.

-   Asigne a todos los archivos compartidos una versión de archivo que dependa del nombre de la aplicación.

-   Asigne a todos los mensajes y estructuras de datos usados en los procesos una versión para evitar el uso compartido de procesos cruzados involuntariamente.

-   El archivo DLL no debe depender del uso compartido entre versiones que pueden no existir, como las secciones de memoria compartida que no se comparten entre las distintas versiones del ensamblado.

-   Si agrega una nueva funcionalidad que no sigue el contrato de compatibilidad de la interfaz binaria de la DLL original, debe asignar un nuevo CLSID, ProgId y nombre de archivo. Después, es necesario que las versiones futuras del ensamblado en paralelo utilicen este CLSID, ProgId y el nombre de archivo. Esto evita un conflicto cuando una versión de la DLL que no está en paralelo se registra en una versión en paralelo.

-   Si reutiliza el mismo CLSID o ProgId, pruebe a asegurarse de que el ensamblado es compatible con versiones anteriores.

-   Inicialice y establezca la configuración predeterminada para el ensamblado en el código de ensamblado. No guarde los valores predeterminados en el registro.

-   Asignar versiones a todas las estructuras de datos.

-   El archivo DLL debe almacenar el estado del ensamblado en paralelo, tal y como se describe en [creación de almacenamiento de estado para ensamblados en paralelo](authoring-state-storage-for-side-by-side-assemblies.md).

 

 



