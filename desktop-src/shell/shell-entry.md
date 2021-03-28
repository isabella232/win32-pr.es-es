---
description: La interfaz de usuario de Windows proporciona a los usuarios acceso a una gran variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo.
title: Shell de Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985611"
---
# <a name="windows-shell"></a>Shell de Windows

La interfaz de usuario de Windows proporciona a los usuarios acceso a una gran variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo. El más conocido de estos objetos son las carpetas y los archivos que residen en las unidades de disco del equipo. También hay una serie de objetos virtuales que permiten al usuario realizar tareas como el envío de archivos a las impresoras remotas o el acceso a la papelera de reciclaje. El shell organiza estos objetos en un espacio de nombres jerárquico y proporciona a los usuarios y las aplicaciones una manera coherente y eficaz de obtener acceso a los objetos y administrarlos.

## <a name="shell-development-scenarios"></a>Escenarios de desarrollo de Shell

Los siguientes escenarios de desarrollo se relacionan con el desarrollo de aplicaciones:

-   Extender el Shell, que consiste en crear un origen de datos (en lugar de consumir el modelo de datos de Shell)
-   Implementar un subconjunto de las tareas de origen de datos de Shell
-   Compatibilidad con bibliotecas y vistas de elementos en el explorador de Windows
-   Usar el cuadro de diálogo archivo común
-   Implementar elementos del panel de control
-   Administración de notificaciones

Los siguientes escenarios de desarrollo se refieren a la propiedad del formato de archivo:

-   Implementar un subconjunto de las tareas de origen de datos de Shell
-   Implementar cualquier controlador
-   Compatibilidad con la búsqueda en el escritorio

Los siguientes escenarios de desarrollo se refieren a la propiedad del almacenamiento de datos:

-   Compatibilidad con la búsqueda de escritorio y OpenSearch
-   Implementar un subconjunto de las tareas de origen de datos de Shell (carpetas virtuales)
-   Bibliotecas auxiliares en el explorador de Windows

El siguiente escenario de desarrollo está relacionado con la compatibilidad de dispositivos:

-   Ejecución automática y reproducción automática

## <a name="windows-shell-sdk-documentation"></a>Documentación del SDK de Windows Shell

Esta documentación se divide en tres secciones principales:

-   La [Guía del desarrollador de Shell](intro.md) proporciona material conceptual sobre cómo funciona el Shell y cómo usar la API del shell en la aplicación.
-   La sección de [Referencia del shell](shell-reference-bumper.md) documenta los elementos de programación que componen las distintas API de Shell.
-   [Ejemplos de Shell](samples-entry.md) proporciona vínculos a ejemplos de código relacionados.

En la tabla siguiente se proporciona un esquema de la sección de referencia de Shell. A menos que se indique lo contrario, todos los elementos de programación están documentados en C++ no administrado.



| Sección                                                               | Descripción                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Clases de Shell](classes.md)                                          | En esta sección se describen las clases de Shell de Windows.                                                                 |
| [Interfaces de Shell](interfaces.md)                                    | En esta sección se describen las interfaces del modelo de objetos componentes (COM) del shell de Windows.                                    |
| [Funciones de Shell](functions.md)                                      | En esta sección se describen las funciones del shell de Windows.                                                                  |
| [Funciones de devolución de llamada de Shell](callbacks.md)                             | En esta sección se describen las plantillas de funciones de devolución de llamada del shell de Windows.                                               |
| [Constantes, enumeraciones y marcas de Shell](consts-enums-flags.md)    | En esta sección se describen las constantes, enumeraciones y marcas del shell de Windows que se usan en las API de Shell.                  |
| [Funciones de la utilidad ligera de Shell](shlwapi.md)                    | En esta sección se describen las funciones de utilidad ligera de Shell de Windows proporcionadas en Shlwapi.dll.                      |
| [Macros de Shell](macros.md)                                            | En esta sección se describen las macros de la utilidad Shell de Windows.                                                             |
| [Notificaciones y mensajes de Shell](messages.md)                      | En esta sección se describen los mensajes y las notificaciones enviados por elementos del shell de Windows.                         |
| [Objetos de Shell para scripting y Microsoft Visual Basic](objects.md) | En esta sección se describen los objetos de Windows implementados por el shell para su uso en scripting y Microsoft Visual Basic. |
| [Objetos de Shell para C++](objects-cpp.md)                              | En esta sección se describen los objetos de Windows de C++ implementados por el shell.                                             |
| [Esquemas de Shell](schemas.md)                                          | En esta sección se describen los esquemas de manifiesto de biblioteca, propiedad y transferencia utilizados por el shell de Windows.                   |
| [Estructuras de Shell](structures.md)                                    | En esta sección se describen las estructuras de Shell de Windows que se usan en las API de Shell.                                          |



 

 

 



