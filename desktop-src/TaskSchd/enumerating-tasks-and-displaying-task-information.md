---
title: Enumerar tareas y mostrar información de tareas
description: Para mostrar información sobre una tarea, como el nombre de la tarea, el estado o la última vez que se ejecutó la tarea, se enumeran las tareas en ejecución o las tareas de una carpeta de tareas y se muestra la información deseada.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- enumeración de tareas Programador de tareas
- Programador de tareas ejemplos Programador de tareas , enumeración de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068667"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a>Enumerar tareas y mostrar información de tareas

Para mostrar información sobre una tarea, como el nombre de la tarea, el estado o la última vez que se ejecutó la tarea, se enumeran las tareas en ejecución o las tareas de una carpeta de tareas y se muestra la información deseada.

## <a name="accessing-properties-of-registered-tasks"></a>Acceso a las propiedades de las tareas registradas

Para mostrar el valor de propiedad de una tarea registrada, debe conectarse al servicio Programador de tareas y, a continuación, obtener una instancia de la carpeta de tareas que contiene las tareas de las que desea obtener información. A continuación, se obtiene una colección de todas las tareas registradas en la carpeta de tareas. A continuación, se enumera a través de cada tarea registrada y se obtiene y muestra un valor de propiedad para cada tarea.

## <a name="accessing-properties-of-running-tasks"></a>Acceso a las propiedades de las tareas en ejecución

Para mostrar el valor de propiedad de una tarea en ejecución, debe conectarse al servicio Programador de tareas y, a continuación, obtener una colección de todas las tareas en ejecución (incluidas o excluidas las tareas ocultas). A continuación, enumera a través de cada tarea en ejecución y obtiene y muestra un valor de propiedad para cada tarea.

## <a name="example"></a>Ejemplo

En los ejemplos siguientes se enumeran las tareas y se muestra el nombre y el estado de las tareas:

-   [Mostrar nombres y estados de tareas (scripting)](displaying-task-names-and-state--scripting-.md)
-   [Mostrar los nombres y el estado de las tareas (C++)](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




