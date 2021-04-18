---
title: Arrastrar y colocar
description: Arrastrar y colocar hace referencia a las transferencias de datos en las que se usa un mouse u otro dispositivo señalador para especificar el origen de datos y su destino.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704675"
---
# <a name="drag-and-drop"></a><span data-ttu-id="eb8fc-103">Arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="eb8fc-103">Drag and Drop</span></span>

<span data-ttu-id="eb8fc-104">*Arrastrar y colocar* hace referencia a las transferencias de datos en las que se usa un mouse u otro dispositivo señalador para especificar el origen de datos y su destino.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-104">*Drag and drop* refers to data transfers in which a mouse or other pointing device is used to specify both the data source and its destination.</span></span> <span data-ttu-id="eb8fc-105">En una operación típica de arrastrar y colocar, un usuario selecciona el objeto que se va a transferir moviendo el puntero del mouse y manteniendo presionado el botón izquierdo o algún otro botón designado para este fin.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-105">In a typical drag and drop operation, a user selects the object to be transferred by moving the mouse pointer to it and holding down either the left button or some other button designated for this purpose.</span></span> <span data-ttu-id="eb8fc-106">Mientras continúa manteniendo presionado el botón, el usuario inicia la transferencia arrastrando el objeto hasta su destino, que puede ser cualquier contenedor OLE.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-106">While continuing to hold down the button, the user initiates the transfer by dragging the object to its destination, which can be any OLE container.</span></span> <span data-ttu-id="eb8fc-107">Arrastrar y colocar proporciona exactamente la misma funcionalidad que el portapapeles OLE copiar y pegar, pero agrega comentarios visuales y elimina la necesidad de menús.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-107">Drag and drop provides exactly the same functionality as the OLE clipboard copy and paste but adds visual feedback and eliminates the need for menus.</span></span> <span data-ttu-id="eb8fc-108">De hecho, si una aplicación admite la copia y pegado del portapapeles, se necesita poco más para admitir las operaciones de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-108">In fact, if an application supports clipboard copy and paste, little extra is needed to support drag and drop.</span></span>

<span data-ttu-id="eb8fc-109">Durante una operación de arrastrar y colocar de OLE, se usan los siguientes tres fragmentos de código independientes.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-109">During an OLE drag and drop operation, the following three separate pieces of code are used.</span></span>



| <span data-ttu-id="eb8fc-110">Origen de código de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="eb8fc-110">Drag-and-drop code source</span></span>                               | <span data-ttu-id="eb8fc-111">Implementación y uso</span><span class="sxs-lookup"><span data-stu-id="eb8fc-111">Implementation and use</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8fc-112">Interfaz [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)</span><span class="sxs-lookup"><span data-stu-id="eb8fc-112">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interface</span></span><br/> | <span data-ttu-id="eb8fc-113">Implementado por el objeto que contiene los datos arrastrados, a los que se hace referencia como el *origen de arrastre*.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-113">Implemented by the object containing the dragged data, referred to as the *drag source*.</span></span><br/>                                                                                         |
| <span data-ttu-id="eb8fc-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) (interfaz)</span><span class="sxs-lookup"><span data-stu-id="eb8fc-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interface</span></span><br/> | <span data-ttu-id="eb8fc-115">Implementado por el objeto que está pensado para aceptar la eliminación, a la que se hace referencia como *destino de colocación*.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-115">Implemented by the object that is intended to accept the drop, referred to as the *drop target*.</span></span><br/>                                                                                 |
| <span data-ttu-id="eb8fc-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) , función</span><span class="sxs-lookup"><span data-stu-id="eb8fc-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function</span></span><br/>    | <span data-ttu-id="eb8fc-117">Implementado por OLE y se usa para iniciar una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-117">Implemented by OLE and used to initiate a drag and drop operation.</span></span> <span data-ttu-id="eb8fc-118">Una vez que la operación está en curso, facilita la comunicación entre el origen de arrastre y el destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-118">After the operation is in progress, it facilitates communication between the drag source and the drop target.</span></span><br/> |



 

<span data-ttu-id="eb8fc-119">Las interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) se pueden implementar en un contenedor o en una aplicación de objeto.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-119">The [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interfaces can be implemented in either a container or in an object application.</span></span> <span data-ttu-id="eb8fc-120">El rol de origen de arrastre o destino de colocación no se limita a un tipo de aplicación OLE.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-120">The role of drag source or drop target is not limited to any one type of OLE application.</span></span>

<span data-ttu-id="eb8fc-121">La función [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) de OLE implementa un bucle que realiza un seguimiento de los movimientos del mouse y del teclado hasta el momento en que se cancela la acción de arrastrar o se produce una caída.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-121">The OLE function [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implements a loop that tracks mouse and keyboard movement until such time as the drag is canceled or a drop occurs.</span></span> <span data-ttu-id="eb8fc-122">**DoDragDrop** es la función clave en el proceso de arrastrar y colocar, facilitando la comunicación entre el origen de arrastre y el destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-122">**DoDragDrop** is the key function in the drag and drop process, facilitating communication between the drag source and drop target.</span></span>

<span data-ttu-id="eb8fc-123">Durante una operación de arrastrar y colocar, se pueden mostrar tres tipos de comentarios al usuario.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-123">During a drag and drop operation, three types of feedback can be displayed to the user.</span></span>



| <span data-ttu-id="eb8fc-124">Tipo de comentarios</span><span class="sxs-lookup"><span data-stu-id="eb8fc-124">Type of feedback</span></span>            | <span data-ttu-id="eb8fc-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb8fc-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8fc-126">Comentarios de origen</span><span class="sxs-lookup"><span data-stu-id="eb8fc-126">Source feedback</span></span><br/>  | <span data-ttu-id="eb8fc-127">Proporcionado por el origen de arrastre, los comentarios del origen indican que los datos se están arrastrando y no cambian durante el transcurso del arrastre.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-127">Provided by the drag source, the source feedback indicates the data is being dragged and does not change during the course of the drag.</span></span> <span data-ttu-id="eb8fc-128">Normalmente, los datos se resaltan para indicar que se ha seleccionado.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-128">Typically, the data is highlighted to signal it has been selected.</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="eb8fc-129">Comentarios del puntero</span><span class="sxs-lookup"><span data-stu-id="eb8fc-129">Pointer feedback</span></span><br/> | <span data-ttu-id="eb8fc-130">Proporcionado por el origen de arrastre, los comentarios del puntero indican lo que ocurre si se suelta el mouse en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-130">Provided by the drag source, the pointer feedback indicates what happens if the mouse is released at any given moment.</span></span> <span data-ttu-id="eb8fc-131">Los comentarios del puntero cambian continuamente a medida que el usuario mueve el mouse o presiona una tecla modificadora.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-131">Pointer feedback changes continually as the user moves the mouse and/or presses a modifier key.</span></span> <span data-ttu-id="eb8fc-132">Por ejemplo, si el puntero se mueve a una ventana que no puede aceptar una colocación, el puntero cambia al símbolo "no permitido".</span><span class="sxs-lookup"><span data-stu-id="eb8fc-132">For example, if the pointer is moved into a window that cannot accept a drop, the pointer changes to the "not allowed" symbol.</span></span><br/> |
| <span data-ttu-id="eb8fc-133">Comentarios de destino</span><span class="sxs-lookup"><span data-stu-id="eb8fc-133">Target feedback</span></span><br/>  | <span data-ttu-id="eb8fc-134">Proporcionado por el destino de colocación, los comentarios de destino indican dónde debe realizarse la eliminación.</span><span class="sxs-lookup"><span data-stu-id="eb8fc-134">Provided by the drop target, target feedback indicates where the drop is to occur.</span></span><br/>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="eb8fc-135">Para obtener más información, vea [arrastrar responsabilidades del origen](drag-source-responsibilities.md).</span><span class="sxs-lookup"><span data-stu-id="eb8fc-135">For more information, see [Drag Source Responsibilities](drag-source-responsibilities.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb8fc-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb8fc-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb8fc-137">Transferencia de datos</span><span class="sxs-lookup"><span data-stu-id="eb8fc-137">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 





