---
title: Consideraciones de programación (Programador de tareas)
description: Al desarrollar aplicaciones que usan el Programador de tareas 1,0, tenga en cuenta los siguientes problemas de programación. La aplicación debe asegurarse de que el servicio de Programador de tareas se está ejecutando antes de intentar realizar llamadas mediante la API de Programador de tareas. Al recuperar cadenas, asegúrese de llamar a CoTaskMemFree para liberar cada cadena una vez que ya no se necesite. Al recuperar matrices de cadenas, asegúrese de liberar primero cada cadena de la matriz y, a continuación, liberar la propia matriz. Al crear o modificar un elemento de trabajo, incluidos los desencadenadores asociados a un elemento de trabajo, asegúrese de llamar a IPersistFile Save para guardar el elemento de trabajo en el disco. Después de usar cualquiera de las interfaces proporcionadas por la API de Programador de tareas, asegúrese de llamar a la versión IUnknown para liberar la interfaz. IUnknown es compatible con cada objeto de Programador de tareas.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- Inicio Programador de tareas
- consideraciones de programación Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676533"
---
# <a name="programming-considerations-task-scheduler"></a>Consideraciones de programación (Programador de tareas)

Al desarrollar aplicaciones que usan el Programador de tareas 1,0, tenga en cuenta los siguientes problemas de programación.

-   La aplicación debe asegurarse de que el servicio de Programador de tareas se está ejecutando antes de intentar realizar llamadas mediante la API de Programador de tareas.
-   Al recuperar cadenas, asegúrese de llamar a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar cada cadena una vez que ya no se necesite. Al recuperar matrices de cadenas, asegúrese de liberar primero cada cadena de la matriz y, a continuación, liberar la propia matriz.
-   Al crear o modificar un elemento de trabajo, incluidos los desencadenadores asociados a un elemento de trabajo, asegúrese de llamar a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el elemento de trabajo en el disco.
-   Después de usar cualquiera de las interfaces proporcionadas por el Programador de tareas API, asegúrese de llamar a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar la interfaz. [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) es compatible con cada objeto de programador de tareas.

La sección uso de la documentación Programador de tareas proporciona numerosos ejemplos que siguen estas instrucciones. En la tabla siguiente se proporcionan saltos a algunos de estos ejemplos.

| Para obtener un ejemplo de         | Vea                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| Liberar cadenas         | [Recuperar ejemplos de propiedades de elementos de trabajo](retrieving-work-item-property-examples.md)       |
| Guardar elementos de trabajo en el disco | [Configuración de ejemplos de propiedades de elementos de trabajo](setting-work-item-property-examples.md)             |
| Liberar interfaces      | [Crear una tarea mediante el ejemplo NewWorkItem](creating-a-task-using-newworkitem-example.md) |



 

 

 
