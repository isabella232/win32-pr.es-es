---
title: Consideraciones de programación (Programador de tareas)
description: Al desarrollar aplicaciones que usan el Programador de tareas 1.0, tenga en cuenta los siguientes problemas de programación. La aplicación debe asegurarse de que Programador de tareas servicio se está ejecutando antes de intentar realizar cualquier llamada mediante Programador de tareas API. Al recuperar cadenas, asegúrese de llamar a CoTaskMemFree para liberar cada cadena después de que ya no sea necesaria. Al recuperar matrices de cadenas, asegúrese de liberar primero cada cadena de la matriz y, a continuación, liberar la propia matriz. Al crear o modificar un elemento de trabajo, incluidos los desencadenadores asociados a un elemento de trabajo, asegúrese de llamar a IPersistFile Save para guardar el elemento de trabajo en el disco. Después de usar cualquiera de las interfaces proporcionadas por Programador de tareas API, asegúrese de llamar a IUnknown Release para liberar la interfaz. IUnknown es compatible con cada Programador de tareas objeto.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- a partir de Programador de tareas
- consideraciones de programación Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa04e5987ea375dfdfc535b0d4d27b21621d2d9678bd69ea15819c8f90bffee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943638"
---
# <a name="programming-considerations-task-scheduler"></a>Consideraciones de programación (Programador de tareas)

Al desarrollar aplicaciones que usan el Programador de tareas 1.0, tenga en cuenta los siguientes problemas de programación.

-   La aplicación debe asegurarse de que Programador de tareas servicio se está ejecutando antes de intentar realizar cualquier llamada mediante Programador de tareas API.
-   Al recuperar cadenas, asegúrese de llamar a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar cada cadena después de que ya no sea necesaria. Al recuperar matrices de cadenas, asegúrese de liberar primero cada cadena de la matriz y, a continuación, liberar la propia matriz.
-   Al crear o modificar un elemento de trabajo, incluidos los desencadenadores asociados a un elemento de trabajo, asegúrese de llamar a [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para guardar el elemento de trabajo en el disco.
-   Después de usar cualquiera de las interfaces proporcionadas por la API Programador de tareas, asegúrese de llamar a [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar la interfaz. [**IUnknown es**](/windows/win32/api/unknwn/nn-unknwn-iunknown) compatible con cada Programador de tareas objeto.

La sección Uso de la documentación Programador de tareas proporciona numerosos ejemplos que siguen estas directrices. En la tabla siguiente se proporcionan saltos a algunos de estos ejemplos.

| Para obtener un ejemplo de         | Vea                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| Liberar cadenas         | [Recuperación de ejemplos de propiedades de elementos de trabajo](retrieving-work-item-property-examples.md)       |
| Guardar elementos de trabajo en el disco | [Establecer ejemplos de propiedades de elemento de trabajo](setting-work-item-property-examples.md)             |
| Liberar interfaces      | [Crear una tarea mediante el ejemplo NewWorkItem](creating-a-task-using-newworkitem-example.md) |



 

 

 
