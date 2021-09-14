---
title: Arrastrar responsabilidades de origen
description: Arrastrar responsabilidades de origen
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242907"
---
# <a name="drag-source-responsibilities"></a>Arrastrar responsabilidades de origen

El origen de arrastre es responsable de las siguientes tareas:

-   Proporcionar un objeto de transferencia de datos para el destino de colocación que expone las interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) [**e IDropSource.**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
-   Generación de comentarios de origen y puntero.
-   Determinar cuándo se ha cancelado la operación de arrastre o se ha producido una operación de colocación.
-   Realizar cualquier acción en los datos originales causados por la operación de eliminación, como eliminar los datos o crear un vínculo a él.

La tarea principal consiste en crear un objeto de transferencia de datos que expone las interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) [**e IDropSource.**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) El origen de arrastre podría incluir o no una copia de los datos seleccionados. Incluirlo no es obligatorio, pero hacerlo ayuda a protegerse contra cambios involuntarios y permite que el código de operaciones del Portapapeles sea idéntico al código de arrastrar y colocar.

Mientras hay una operación de arrastre en curso, el origen de arrastre es responsable de establecer el puntero del mouse y, si procede, de proporcionar comentarios de origen adicionales al usuario. El origen de arrastre no puede proporcionar ningún comentario que haga un seguimiento de la posición del mouse que no sea estableciendo realmente el puntero real (vea la [**función SetCursor).**](/windows/win32/api/winuser/nf-winuser-setcursor) Esta regla debe aplicarse para evitar conflictos con los comentarios proporcionados por el destino de colocación. (Un origen de arrastre también puede ser un destino de colocación. Cuando se coloca sobre sí mismo, el origen o destino puede, por supuesto, proporcionar comentarios de destino para realizar un seguimiento de la posición del mouse. En este caso, sin embargo, es el destino de colocación el que hace el seguimiento del mouse, no el origen). En función de los comentarios que ofrece el destino de colocación, el origen establece un puntero adecuado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arrastrar y colocar](drag-and-drop.md)
</dt> </dl>

 

 