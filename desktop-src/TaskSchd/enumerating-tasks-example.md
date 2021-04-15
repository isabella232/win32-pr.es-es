---
title: Ejemplo de enumeración de tareas
description: Para enumerar las tareas, debe llamar a la enumeración ITaskScheduler para crear un objeto de enumeración. A continuación, use la interfaz IEnumWorkItems del objeto de enumeración para enumerar las tareas de la carpeta tareas programadas.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676447"
---
# <a name="enumerating-tasks-example"></a>Ejemplo de enumeración de tareas

Para enumerar las tareas, debe llamar a [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) para crear un [*objeto de enumeración*](e.md). A continuación, use la interfaz [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) del objeto de enumeración para enumerar las tareas de la carpeta tareas programadas.

En el procedimiento siguiente se describe cómo enumerar las tareas en la carpeta tareas programadas.

**Para enumerar las tareas de la carpeta tareas programadas**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) para obtener un objeto de enumeración.
3.  Llame a [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) para recuperar las tareas. (En este ejemplo se intenta recuperar cinco tareas con cada llamada).
4.  Procesa las tareas devueltas. (Este ejemplo simplemente imprime el nombre de cada tarea en la pantalla.
5.  Libere recursos. Llame a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria usada para los nombres.



| Para obtener un ejemplo de código de                                                         | Vea                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Enumerar todas las tareas de la carpeta tareas programadas del equipo local | [Ejemplo de código de C/C++: enumerar tareas](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 