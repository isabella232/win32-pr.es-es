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
# <a name="drag-source-responsibilities"></a><span data-ttu-id="a46a5-103">Arrastrar responsabilidades de origen</span><span class="sxs-lookup"><span data-stu-id="a46a5-103">Drag Source Responsibilities</span></span>

<span data-ttu-id="a46a5-104">El origen de arrastre es responsable de las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="a46a5-104">The drag source is responsible for the following tasks:</span></span>

-   <span data-ttu-id="a46a5-105">Proporcionar un objeto de transferencia de datos para el destino de colocación que expone las interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="a46a5-105">Providing a data-transfer object for the drop target that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span>
-   <span data-ttu-id="a46a5-106">Generación de comentarios de puntero y de origen.</span><span class="sxs-lookup"><span data-stu-id="a46a5-106">Generating pointer and source feedback.</span></span>
-   <span data-ttu-id="a46a5-107">Determinar cuándo se ha cancelado la operación de arrastre o se ha producido una operación de colocar.</span><span class="sxs-lookup"><span data-stu-id="a46a5-107">Determining when the drag operation has been canceled or a drop operation has occurred.</span></span>
-   <span data-ttu-id="a46a5-108">Realizar cualquier acción en los datos originales causados por la operación de colocar, como eliminar los datos o crear un vínculo a él.</span><span class="sxs-lookup"><span data-stu-id="a46a5-108">Performing any action on the original data caused by the drop operation, such as deleting the data or creating a link to it.</span></span>

<span data-ttu-id="a46a5-109">La tarea principal es la creación de un objeto de transferencia de datos que expone las interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="a46a5-109">The main task is creating a data-transfer object that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span> <span data-ttu-id="a46a5-110">El origen de arrastre puede incluir o no una copia de los datos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="a46a5-110">The drag source might or might not include a copy of the selected data.</span></span> <span data-ttu-id="a46a5-111">La inclusión no es obligatoria, pero esto ayuda a protegerse contra cambios involuntarios y permite que el código de operaciones del portapapeles sea idéntico al código de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="a46a5-111">Including it is not mandatory, but doing so helps protect against inadvertent changes and allows the Clipboard operations code to be identical to the drag and drop code.</span></span>

<span data-ttu-id="a46a5-112">Mientras una operación de arrastre está en curso, el origen de arrastre es responsable de establecer el puntero del mouse y, si es necesario, para proporcionar comentarios sobre el origen adicional al usuario.</span><span class="sxs-lookup"><span data-stu-id="a46a5-112">While a drag operation is in progress, the drag source is responsible for setting the mouse pointer and, if appropriate, for providing additional source feedback to the user.</span></span> <span data-ttu-id="a46a5-113">El origen de arrastre no puede proporcionar ningún comentario que realice un seguimiento de la posición del mouse que no sea estableciendo realmente el puntero real (vea la función [**setCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) ).</span><span class="sxs-lookup"><span data-stu-id="a46a5-113">The drag source cannot provide any feedback that tracks the mouse position other than by actually setting the real pointer (see the [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) function).</span></span> <span data-ttu-id="a46a5-114">Esta regla se debe aplicar para evitar conflictos con los comentarios proporcionados por el destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="a46a5-114">This rule must be enforced to avoid conflicts with the feedback provided by the drop target.</span></span> <span data-ttu-id="a46a5-115">(Un origen de arrastre también puede ser un destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="a46a5-115">(A drag source can also be a drop target.</span></span> <span data-ttu-id="a46a5-116">Al colocarse en sí mismo, el origen o el destino pueden, por supuesto, proporcionar comentarios de destino para realizar el seguimiento de la posición del mouse.</span><span class="sxs-lookup"><span data-stu-id="a46a5-116">When dropping on itself, the source/target can, of course, provide target feedback to track the mouse position.</span></span> <span data-ttu-id="a46a5-117">Sin embargo, en este caso, se trata del destino de colocación que realiza el seguimiento del mouse, no del origen). En función de los comentarios que ofrece el destino de colocación, el origen establece un puntero adecuado.</span><span class="sxs-lookup"><span data-stu-id="a46a5-117">In this case, however, it is the drop target tracking the mouse, not the source.) Based on the feedback offered by the drop target, the source sets an appropriate pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a46a5-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a46a5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a46a5-119">Arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="a46a5-119">Drag and Drop</span></span>](drag-and-drop.md)
</dt> </dl>

 

 