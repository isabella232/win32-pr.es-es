---
description: La Windows de usuario proporciona a los usuarios acceso a una amplia variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo.
title: Windows Cáscara
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247952"
---
# <a name="windows-shell"></a>Windows Cáscara

La Windows de usuario proporciona a los usuarios acceso a una amplia variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo. Los objetos más numerosos y familiares son las carpetas y los archivos que residen en unidades de disco del equipo. También hay una serie de objetos virtuales que permiten al usuario realizar tareas como enviar archivos a impresoras remotas o acceder a la papelera de reciclaje. El Shell organiza estos objetos en un espacio de nombres jerárquico y proporciona a los usuarios y las aplicaciones una manera coherente y eficaz de acceder a los objetos y administrarlos.

## <a name="shell-development-scenarios"></a>Escenarios de desarrollo de Shell

Los siguientes escenarios de desarrollo están relacionados con el desarrollo de aplicaciones:

-   Extender el shell, que consiste en crear un origen de datos (frente al consumo del modelo de datos de Shell)
-   Implementación de un subconjunto de las tareas del origen de datos de Shell
-   Compatibilidad con bibliotecas y vistas de elementos en Windows Explorer
-   Uso del cuadro de diálogo de archivo común
-   Implementación de Panel de control elementos
-   Administración de notificaciones

Los siguientes escenarios de desarrollo están relacionados con la propiedad del formato de archivo:

-   Implementación de un subconjunto de las tareas del origen de datos de Shell
-   Implementar cualquier controlador
-   Compatibilidad con la búsqueda de escritorio

Los siguientes escenarios de desarrollo están relacionados con la propiedad del almacenamiento de datos:

-   Compatibilidad con la búsqueda de escritorio y OpenSearch
-   Implementación de un subconjunto de las tareas de origen de datos de Shell (carpetas virtuales)
-   Compatibilidad de bibliotecas en Windows Explorer

El siguiente escenario de desarrollo está relacionado con la compatibilidad con dispositivos:

-   Ejecución automática y reproducción automática

## <a name="windows-shell-sdk-documentation"></a>Windows Documentación del SDK de Shell

Esta documentación se divide en tres secciones principales:

-   La [Guía del desarrollador de Shell](intro.md) proporciona material conceptual sobre cómo funciona shell y cómo usar la API del shell en la aplicación.
-   En [la sección Referencia del](shell-reference-bumper.md) shell se documenta la programación de elementos que son las distintas API de Shell.
-   [Ejemplos de shell](samples-entry.md) proporciona vínculos a ejemplos de código relacionados.

En la tabla siguiente se proporciona un esquema de la sección Referencia del shell. A menos que se indique lo contrario, todos los elementos de programación se documentan en C++ no administrado.



| Sección                                                               | Descripción                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Clases de shell](classes.md)                                          | En esta sección se describe la selección Windows clases de Shell.                                                                 |
| [Shell Interfaces](interfaces.md)                                    | En esta sección se describen Windows interfaces del Modelo de objetos componentes (COM) de Shell.                                    |
| [Funciones de shell](functions.md)                                      | En esta sección se describen las Windows Shell.                                                                  |
| [Funciones de devolución de llamada de shell](callbacks.md)                             | En esta sección se describen las plantillas de Windows de devolución de llamada de Shell.                                               |
| [Constantes de shell, enumeraciones y marcas](consts-enums-flags.md)    | En esta sección se describen las Windows, enumeraciones y marcas de Shell usadas en las API de Shell.                  |
| [Funciones de utilidad ligera de Shell](shlwapi.md)                    | En esta sección se describen las Windows de utilidad ligera de Shell proporcionadas en Shlwapi.dll.                      |
| [Shell Macros](macros.md)                                            | En esta sección se describen las macros de Windows Shell.                                                             |
| [Mensajes y notificaciones de shell](messages.md)                      | En esta sección se describen los mensajes y las notificaciones enviados por los elementos de Windows Shell.                         |
| [Objetos de shell para scripting y Microsoft Visual Basic](objects.md) | En esta sección se describen los Windows implementados por shell para su uso en scripting y Microsoft Visual Basic. |
| [Objetos de shell para C++](objects-cpp.md)                              | En esta sección se describen los objetos Windows C++ implementados por el shell.                                             |
| [Esquemas de shell](schemas.md)                                          | En esta sección se describen los esquemas de biblioteca, propiedad y manifiesto de transferencia usados por Windows Shell.                   |
| [Estructuras de shell](structures.md)                                    | En esta sección se describen las Windows shell usadas en las API de Shell.                                          |



 

 

 



