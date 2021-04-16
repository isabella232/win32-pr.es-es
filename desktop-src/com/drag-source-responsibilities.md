---
title: Arrastrar responsabilidades de origen
description: Arrastrar responsabilidades de origen
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695764"
---
# <a name="drag-source-responsibilities"></a>Arrastrar responsabilidades de origen

El origen de arrastre es responsable de las siguientes tareas:

-   Proporcionar un objeto de transferencia de datos para el destino de colocación que expone las interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .
-   Generación de comentarios de puntero y de origen.
-   Determinar cuándo se ha cancelado la operación de arrastre o se ha producido una operación de colocar.
-   Realizar cualquier acción en los datos originales causados por la operación de colocar, como eliminar los datos o crear un vínculo a él.

La tarea principal es la creación de un objeto de transferencia de datos que expone las interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) . El origen de arrastre puede incluir o no una copia de los datos seleccionados. La inclusión no es obligatoria, pero esto ayuda a protegerse contra cambios involuntarios y permite que el código de operaciones del portapapeles sea idéntico al código de arrastrar y colocar.

Mientras una operación de arrastre está en curso, el origen de arrastre es responsable de establecer el puntero del mouse y, si es necesario, para proporcionar comentarios sobre el origen adicional al usuario. El origen de arrastre no puede proporcionar ningún comentario que realice un seguimiento de la posición del mouse que no sea estableciendo realmente el puntero real (vea la función [**setCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) ). Esta regla se debe aplicar para evitar conflictos con los comentarios proporcionados por el destino de colocación. (Un origen de arrastre también puede ser un destino de colocación. Al colocarse en sí mismo, el origen o el destino pueden, por supuesto, proporcionar comentarios de destino para realizar el seguimiento de la posición del mouse. Sin embargo, en este caso, se trata del destino de colocación que realiza el seguimiento del mouse, no del origen). En función de los comentarios que ofrece el destino de colocación, el origen establece un puntero adecuado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arrastrar y colocar](drag-and-drop.md)
</dt> </dl>

 

 