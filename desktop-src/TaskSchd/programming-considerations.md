---
title: Consideraciones de programación (Programador de tareas)
description: Al desarrollar aplicaciones que usan el Programador de tareas 1.0, tenga en cuenta los siguientes problemas de programación. La aplicación debe asegurarse de que Programador de tareas servicio se está ejecutando antes de intentar realizar cualquier llamada mediante Programador de tareas API. Al recuperar cadenas, asegúrese de llamar a CoTaskMemFree para liberar cada cadena después de que ya no sea necesaria. Al recuperar matrices de cadenas, asegúrese de liberar primero cada cadena de la matriz y, a continuación, liberar la propia matriz. Al crear o modificar un elemento de trabajo, incluidos los desencadenadores asociados a un elemento de trabajo, asegúrese de llamar a IPersistFile Save para guardar el elemento de trabajo en el disco. Después de usar cualquiera de las interfaces proporcionadas por Programador de tareas API, asegúrese de llamar a IUnknown Release para liberar la interfaz. IUnknown es compatible con cada Programador de tareas objeto.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- a partir Programador de tareas
- consideraciones de programación Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173017"
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
| Liberación de interfaces      | [Crear una tarea mediante el ejemplo NewWorkItem](creating-a-task-using-newworkitem-example.md) |



 

 

 
