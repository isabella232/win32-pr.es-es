---
description: Al crear sus propios ensamblados en paralelo, siga las instrucciones para crear ensamblados en paralelo.
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: Creación de archivos DLL para ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa15f3876c60ce55be00d60d8f417eb0c2cbf6ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271716"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a>Creación de archivos DLL para ensamblados en paralelo

Al crear sus propios ensamblados en [](guidelines-for-creating-side-by-side-assemblies.md) paralelo, siga las instrucciones para crear ensamblados en paralelo y cree los archivos DLL que se usan en el ensamblado según las instrucciones siguientes:

-   Los archivos DLL deben diseñarse para que se puedan ejecutar varias versiones al mismo tiempo y en el mismo proceso sin interferir entre sí. Por ejemplo, muchas aplicaciones hospedan varios complementos que requieren una versión diferente de un componente. El desarrollador debe diseñar y probar el ensamblado en paralelo para asegurarse de que varias versiones del componente funcionan correctamente cuando se ejecutan al mismo tiempo en el mismo proceso.

-   Si tiene previsto proporcionar el componente como un componente compartido en sistemas anteriores a Windows XP, debe seguir instalando el componente en estos sistemas como un componente compartido de instancia única. En este caso, debe asegurarse de que el componente es compatible con versiones anteriores.

-   Evalúe el uso de objetos cuando se ejecuta más de una versión del ensamblado en el sistema. Determine si las distintas versiones del ensamblado requieren estructuras de datos independientes, como archivos asignados a memoria, canalizaciones con nombre, clases y mensajes Windows registrados, memoria compartida, semáforos, exclusiones mutuas y controladores de hardware. Todas las estructuras de datos usadas en las versiones de ensamblado deben ser compatibles con versiones anteriores. Decida qué estructuras de datos se pueden usar entre versiones y qué estructuras de datos deben ser privadas para una versión. Determine si las estructuras de datos compartidos requieren objetos de sincronización independientes, como semáforos y exclusiones mutuas.

-   Algunos objetos, como las clases de ventana y los atomes, tienen un nombre único para cada proceso. Los objetos como las clases de ventana deben tener versiones para cada ensamblado mediante el manifiesto. Para objetos como Atoms, use identificadores específicos de la versión a menos que planee compartir entre versiones. Si usa identificadores específicos de la versión, use el número de control de versiones de cuatro partes.

-   No incluya código de registro propio en ningún archivo DLL. Un archivo DLL en un ensamblado en paralelo no puede registrarse por sí mismo.

-   Defina todos los nombres específicos de la versión del archivo DLL con \# instrucciones define. Esto permite cambiar todas las claves del Registro desde una ubicación. Cuando se publica una nueva versión del ensamblado, solo es necesario cambiar esta \# instrucción de definición. Por ejemplo:

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   Almacene los datos no persistentes en el directorio Temp.

-   No coloque los datos de usuario en ubicaciones globales. Mantenga los datos de la aplicación separados de los datos de usuario.

-   Asigne a todos los archivos compartidos una versión de archivo que dependa del nombre de la aplicación.

-   Asigne todos los mensajes y estructuras de datos que se usan en los procesos de una versión para evitar el uso compartido involuntario entre procesos.

-   El archivo DLL no debe depender del uso compartido entre versiones que pueden no existir, como las secciones de memoria compartida que no se comparten entre distintas versiones del ensamblado.

-   Si agrega una nueva funcionalidad que no sigue el contrato de compatibilidad de interfaz binaria del archivo DLL original, debe asignar un nuevo CLSID, ProgId y un nombre de archivo. A continuación, se requieren versiones futuras del ensamblado en paralelo para usar este CLSID, ProgId y el nombre de archivo. Esto evita un conflicto cuando se registra una versión del archivo DLL que no está en paralelo a través de una versión en paralelo.

-   Si reutiliza el mismo CLSID o ProgId, pruebe para asegurarse de que el ensamblado es compatible con versiones anteriores.

-   Inicialice y establezca la configuración predeterminada del ensamblado en el código del ensamblado. No guarde la configuración predeterminada en el Registro.

-   Asigne versiones a todas las estructuras de datos.

-   El archivo DLL debe almacenar el estado del ensamblado en paralelo como se describe en [Authoring State Storage for Side-by-Side Assemblies](authoring-state-storage-for-side-by-side-assemblies.md).

 

 



