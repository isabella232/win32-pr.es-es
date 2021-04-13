---
title: Métodos IPaper
description: Proporciona objetos de copapeles controlados principalmente por su interfaz IPaper nativa.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269317"
---
# <a name="ipaper-methods"></a><span data-ttu-id="25b9e-104">Métodos IPaper</span><span class="sxs-lookup"><span data-stu-id="25b9e-104">IPaper Methods</span></span>

<span data-ttu-id="25b9e-105">**StoServe** proporciona objetos de copapeles controlados principalmente por su interfaz **IPaper** nativa.</span><span class="sxs-lookup"><span data-stu-id="25b9e-105">**StoServe** provides COPaper objects that are controlled primarily by their native **IPaper** interface.</span></span>

<span data-ttu-id="25b9e-106">En la tabla siguiente se enumeran los métodos de **IPaper** de IPaper. H en el directorio del mismo nivel \\ .</span><span class="sxs-lookup"><span data-stu-id="25b9e-106">The following table lists **IPaper** methods from IPAPER.H in the sibling \\INC directory.</span></span>



| <span data-ttu-id="25b9e-107">Método</span><span class="sxs-lookup"><span data-stu-id="25b9e-107">Method</span></span>    | <span data-ttu-id="25b9e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="25b9e-108">Description</span></span>                                                         |
|-----------|---------------------------------------------------------------------|
| <span data-ttu-id="25b9e-109">InitPaper</span><span class="sxs-lookup"><span data-stu-id="25b9e-109">InitPaper</span></span> | <span data-ttu-id="25b9e-110">Inicializa el objeto paper y crea una matriz de datos de tinta.</span><span class="sxs-lookup"><span data-stu-id="25b9e-110">Initializes paper object and create ink data array.</span></span>                 |
| <span data-ttu-id="25b9e-111">Lock</span><span class="sxs-lookup"><span data-stu-id="25b9e-111">Lock</span></span>      | <span data-ttu-id="25b9e-112">Proporciona al cliente control del papel y bloquea a otros clientes.</span><span class="sxs-lookup"><span data-stu-id="25b9e-112">Gives client control of the paper and locks out other clients.</span></span>      |
| <span data-ttu-id="25b9e-113">Desbloquear</span><span class="sxs-lookup"><span data-stu-id="25b9e-113">Unlock</span></span>    | <span data-ttu-id="25b9e-114">Abandona el control de la documentación del cliente.</span><span class="sxs-lookup"><span data-stu-id="25b9e-114">Relinquishes client control of the paper.</span></span>                           |
| <span data-ttu-id="25b9e-115">Cargar</span><span class="sxs-lookup"><span data-stu-id="25b9e-115">Load</span></span>      | <span data-ttu-id="25b9e-116">Carga el contenido de papel del archivo compuesto del cliente y notifica a los receptores.</span><span class="sxs-lookup"><span data-stu-id="25b9e-116">Loads paper content from client's compound file and notifies sinks.</span></span> |
| <span data-ttu-id="25b9e-117">Guardar</span><span class="sxs-lookup"><span data-stu-id="25b9e-117">Save</span></span>      | <span data-ttu-id="25b9e-118">Guarda el contenido del papel en el archivo compuesto del cliente.</span><span class="sxs-lookup"><span data-stu-id="25b9e-118">Saves paper content to client's compound file.</span></span>                      |
| <span data-ttu-id="25b9e-119">InkStart</span><span class="sxs-lookup"><span data-stu-id="25b9e-119">InkStart</span></span>  | <span data-ttu-id="25b9e-120">Inicia el dibujo de la tinta de color en la superficie del papel.</span><span class="sxs-lookup"><span data-stu-id="25b9e-120">Starts color ink drawing to the paper surface.</span></span>                      |
| <span data-ttu-id="25b9e-121">InkDraw</span><span class="sxs-lookup"><span data-stu-id="25b9e-121">InkDraw</span></span>   | <span data-ttu-id="25b9e-122">Coloca los puntos de datos de tinta en la superficie electrónica del papel.</span><span class="sxs-lookup"><span data-stu-id="25b9e-122">Puts ink data points on the electronic paper surface.</span></span>               |
| <span data-ttu-id="25b9e-123">InkStop</span><span class="sxs-lookup"><span data-stu-id="25b9e-123">InkStop</span></span>   | <span data-ttu-id="25b9e-124">Detiene el dibujo de la tinta en la superficie del papel.</span><span class="sxs-lookup"><span data-stu-id="25b9e-124">Stops ink drawing to the paper surface.</span></span>                             |
| <span data-ttu-id="25b9e-125">Borrar</span><span class="sxs-lookup"><span data-stu-id="25b9e-125">Erase</span></span>     | <span data-ttu-id="25b9e-126">Borre el contenido del papel actual y notifique a los receptores.</span><span class="sxs-lookup"><span data-stu-id="25b9e-126">Erase the current paper content and notifies sinks.</span></span>                 |
| <span data-ttu-id="25b9e-127">Cambiar de tamaño</span><span class="sxs-lookup"><span data-stu-id="25b9e-127">Resize</span></span>    | <span data-ttu-id="25b9e-128">Cambia el tamaño del rectángulo del papel del dibujo y notifica a los receptores.</span><span class="sxs-lookup"><span data-stu-id="25b9e-128">Resizes the drawing paper rectangle size and notifies sinks.</span></span>        |
| <span data-ttu-id="25b9e-129">Volver a dibujar</span><span class="sxs-lookup"><span data-stu-id="25b9e-129">Redraw</span></span>    | <span data-ttu-id="25b9e-130">Vuelve a dibujar el contenido del objeto de papel y notifica a los receptores.</span><span class="sxs-lookup"><span data-stu-id="25b9e-130">Redraws contents of paper object and notifies sinks.</span></span>                |



 

<span data-ttu-id="25b9e-131">Los métodos de interés para este ejemplo de código en archivos compuestos son cargar, [**Guardar**](ipaper--save.md)y [**volver**](ipaper--load.md)a [**dibujar**](ipaper--redraw.md).</span><span class="sxs-lookup"><span data-stu-id="25b9e-131">Methods of interest for this code sample on compound files are [**Load**](ipaper--load.md), [**Save**](ipaper--save.md), and [**Redraw**](ipaper--redraw.md).</span></span>

<span data-ttu-id="25b9e-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) son métodos usados por los clientes para el copapel del comando para grabar secuencias de dibujo de tinta.</span><span class="sxs-lookup"><span data-stu-id="25b9e-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) are methods used by clients to command COPaper to record ink drawing sequences.</span></span> <span data-ttu-id="25b9e-133">Normalmente, el cliente responderá a un \_ mensaje de LBUTTONDOWN de WM como el inicio de una secuencia de dibujo de tinta mediante una llamada a **InkStart** en el copaper.</span><span class="sxs-lookup"><span data-stu-id="25b9e-133">The client will typically respond to a WM\_LBUTTONDOWN message as the start of an ink drawing sequence by calling **InkStart** on COPaper.</span></span> <span data-ttu-id="25b9e-134">A medida que el usuario mueve el mouse o el lápiz para dibujar mientras mantiene presionado el botón primario, el cliente responderá a los mensajes de la MOUSEMOVE de WM repetidos \_ con las llamadas correspondientes a **InkDraw**.</span><span class="sxs-lookup"><span data-stu-id="25b9e-134">As the user moves the mouse or pen to draw while holding down the left button, the client will respond to repeated WM\_MOUSEMOVE messages with corresponding calls to **InkDraw**.</span></span> <span data-ttu-id="25b9e-135">Cuando el usuario suelta el botón primario del mouse, el cliente responde a un mensaje de WM \_ LBUTTONUP con una llamada a **InkStop**, que marca el final de la secuencia de dibujo de la tinta.</span><span class="sxs-lookup"><span data-stu-id="25b9e-135">When the user releases the left mouse button, the client will respond to a WM\_LBUTTONUP message with a call to **InkStop**, which marks the end of the ink drawing sequence.</span></span>

<span data-ttu-id="25b9e-136">[**InkStart**](inkstart-method.md) indica al copaper la posición inicial de la secuencia de dibujo en coordenadas de la ventana del cliente.</span><span class="sxs-lookup"><span data-stu-id="25b9e-136">[**InkStart**](inkstart-method.md) tells COPaper the start position for the drawing sequence in client window coordinates.</span></span> <span data-ttu-id="25b9e-137">También pasa el color y el ancho de la tinta seleccionados actualmente.</span><span class="sxs-lookup"><span data-stu-id="25b9e-137">It also passes the currently selected ink color and width.</span></span> <span data-ttu-id="25b9e-138">El cliente mantiene estas selecciones; El copapel simplemente los registra cuando se realiza la llamada a **InkStart** .</span><span class="sxs-lookup"><span data-stu-id="25b9e-138">The client maintains these selections; COPaper merely records them when the **InkStart** call is made.</span></span> <span data-ttu-id="25b9e-139">Se llama a [**InkDraw**](inkdraw-method.md) varias veces para indicar a los copapeles la sucesión de coordenadas de la ventana que representan el movimiento del dibujo del mouse o del lápiz.</span><span class="sxs-lookup"><span data-stu-id="25b9e-139">[**InkDraw**](inkdraw-method.md) is called repeatedly to tell COPaper the succession of window coordinates that represent the drawing motion of the mouse or pen.</span></span> <span data-ttu-id="25b9e-140">[**InkStop**](cguipaper-methods.md) indica al copaper que marque el final de una secuencia de dibujo.</span><span class="sxs-lookup"><span data-stu-id="25b9e-140">[**InkStop**](cguipaper-methods.md) instructs COPaper to mark the end of a drawing sequence.</span></span>

 

 




