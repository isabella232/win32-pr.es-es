---
title: Enumerar tareas y mostrar información de tareas
description: La visualización de información sobre una tarea, como el nombre de la tarea, el estado o la última vez que se ejecutó la tarea, se realiza enumerando mediante tareas en ejecución o en una carpeta de tareas y mostrando la información deseada.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- enumeración de tareas Programador de tareas
- Programador de tareas ejemplos Programador de tareas , enumeración de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4859122218ead4d18c1f9e83de0f55ce9373306cd2762e5608cf4d1841019b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002453"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a>Enumerar tareas y mostrar información de tareas

La visualización de información sobre una tarea, como el nombre de la tarea, el estado o la última vez que se ejecutó la tarea, se realiza enumerando mediante tareas en ejecución o en una carpeta de tareas y mostrando la información deseada.

## <a name="accessing-properties-of-registered-tasks"></a>Acceso a las propiedades de las tareas registradas

Para mostrar el valor de propiedad de una tarea registrada, debe conectarse al servicio Programador de tareas y, a continuación, obtener una instancia de la carpeta de tareas que contiene las tareas sobre las que desea obtener información. A continuación, obtiene una colección de todas las tareas registradas en la carpeta de tareas. A continuación, se enumera a través de cada tarea registrada y se obtiene y muestra un valor de propiedad para cada tarea.

## <a name="accessing-properties-of-running-tasks"></a>Acceso a las propiedades de las tareas en ejecución

Para mostrar el valor de propiedad de una tarea en ejecución, debe conectarse al servicio Programador de tareas y, a continuación, obtener una colección de todas las tareas en ejecución (incluidas o excluidas las tareas ocultas). A continuación, se enumera a través de cada tarea en ejecución y se obtiene y muestra un valor de propiedad para cada tarea.

## <a name="example"></a>Ejemplo

En los ejemplos siguientes se enumeran las tareas y se muestra el nombre y el estado de las tareas:

-   [Mostrar nombres y estados de tareas (scripting)](displaying-task-names-and-state--scripting-.md)
-   [Mostrar los nombres y el estado de las tareas (C++)](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




