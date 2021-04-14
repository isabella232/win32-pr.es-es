---
title: Símbolos
description: En esta sección se describen las intercalaciones que parpadean en líneas, bloques o mapas de bits en el área de cliente de una ventana.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- recursos, insumos
- insumos, acerca de
- líneas intermitentes
- bloques en parpadeo
- parpadeo de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104424095"
---
# <a name="carets"></a><span data-ttu-id="3263a-108">Símbolos</span><span class="sxs-lookup"><span data-stu-id="3263a-108">Carets</span></span>

<span data-ttu-id="3263a-109">Un *símbolo de intercalación* es una línea, un bloque o un mapa de bits intermitentes en el área de cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="3263a-109">A *caret* is a blinking line, block, or bitmap in the client area of a window.</span></span> <span data-ttu-id="3263a-110">El símbolo de intercalación suele indicar el lugar en el que se insertará el texto o los gráficos.</span><span class="sxs-lookup"><span data-stu-id="3263a-110">The caret typically indicates the place at which text or graphics will be inserted.</span></span>

<span data-ttu-id="3263a-111">En la ilustración siguiente se muestran algunas variaciones comunes en la apariencia del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="3263a-111">The following illustration shows some common variations in the appearance of the caret.</span></span>

![Muestra 5 formas diferentes que puede aparecer un símbolo de intercalación.](images/cscrt-01.png)

<span data-ttu-id="3263a-113">Las aplicaciones pueden crear un símbolo de intercalación, cambiar su tiempo de intermitencia y mostrar, ocultar o reubicar el símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="3263a-113">Applications can create a caret, change its blink time, and display, hide, or relocate the caret.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="3263a-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3263a-114">In This Section</span></span>



| <span data-ttu-id="3263a-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="3263a-115">Name</span></span>                                   | <span data-ttu-id="3263a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3263a-116">Description</span></span>                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="3263a-117">Acerca de las intercalaciones</span><span class="sxs-lookup"><span data-stu-id="3263a-117">About Carets</span></span>](about-carets.md)       | <span data-ttu-id="3263a-118">Describe las intercalaciones.</span><span class="sxs-lookup"><span data-stu-id="3263a-118">Discusses carets.</span></span><br/>                                              |
| [<span data-ttu-id="3263a-119">Usar las intercalaciones</span><span class="sxs-lookup"><span data-stu-id="3263a-119">Using Carets</span></span>](using-carets.md)       | <span data-ttu-id="3263a-120">Ejemplos de código que muestran cómo realizar tareas relacionadas con las intercalaciones.</span><span class="sxs-lookup"><span data-stu-id="3263a-120">Code samples that show how to perform tasks related to carets.</span></span><br/> |
| [<span data-ttu-id="3263a-121">Referencia de símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="3263a-121">Caret Reference</span></span>](caret-reference.md) | <span data-ttu-id="3263a-122">Contiene la referencia de la API.</span><span class="sxs-lookup"><span data-stu-id="3263a-122">Contains the API reference.</span></span><br/>                                    |



 

### <a name="caret-functions"></a><span data-ttu-id="3263a-123">Funciones de símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="3263a-123">Caret Functions</span></span>



| <span data-ttu-id="3263a-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="3263a-124">Name</span></span>                                           | <span data-ttu-id="3263a-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="3263a-125">Description</span></span>                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3263a-126">**CreateCaret**</span><span class="sxs-lookup"><span data-stu-id="3263a-126">**CreateCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | <span data-ttu-id="3263a-127">Crea una nueva forma para el símbolo de intercalación del sistema y asigna la propiedad del símbolo de intercalación a la ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="3263a-127">Creates a new shape for the system caret and assigns ownership of the caret to the specified window.</span></span> <span data-ttu-id="3263a-128">La forma del símbolo de intercalación puede ser una línea, un bloque o un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="3263a-128">The caret shape can be a line, a block, or a bitmap.</span></span> <br/>                                                                                         |
| [<span data-ttu-id="3263a-129">**DestroyCaret**</span><span class="sxs-lookup"><span data-stu-id="3263a-129">**DestroyCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | <span data-ttu-id="3263a-130">Destruye la forma actual del símbolo de intercalación, libera el símbolo de intercalación de la ventana y quita el símbolo de intercalación de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="3263a-130">Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.</span></span> <br/>                                                                                                                                       |
| [<span data-ttu-id="3263a-131">**GetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="3263a-131">**GetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | <span data-ttu-id="3263a-132">Recupera el tiempo necesario para invertir los píxeles del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="3263a-132">Retrieves the time required to invert the caret's pixels.</span></span> <span data-ttu-id="3263a-133">El usuario puede establecer este valor.</span><span class="sxs-lookup"><span data-stu-id="3263a-133">The user can set this value.</span></span> <br/>                                                                                                                                                            |
| [<span data-ttu-id="3263a-134">**GetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="3263a-134">**GetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | <span data-ttu-id="3263a-135">Copia la posición del símbolo de intercalación en la estructura de [**puntos**](/previous-versions//dd162805(v=vs.85)) especificada.</span><span class="sxs-lookup"><span data-stu-id="3263a-135">Copies the caret's position to the specified [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <br/>                                                                                                                                                                    |
| [<span data-ttu-id="3263a-136">**HideCaret**</span><span class="sxs-lookup"><span data-stu-id="3263a-136">**HideCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | <span data-ttu-id="3263a-137">Quita el símbolo de intercalación de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="3263a-137">Removes the caret from the screen.</span></span> <span data-ttu-id="3263a-138">Ocultar un símbolo de intercalación no destruye su forma actual ni invalida el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="3263a-138">Hiding a caret does not destroy its current shape or invalidate the insertion point.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="3263a-139">**SetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="3263a-139">**SetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | <span data-ttu-id="3263a-140">Establece el tiempo de parpadeo del símbolo de intercalación en el número de milisegundos especificado.</span><span class="sxs-lookup"><span data-stu-id="3263a-140">Sets the caret blink time to the specified number of milliseconds.</span></span> <span data-ttu-id="3263a-141">El tiempo de intermitencia es el tiempo transcurrido, en milisegundos, necesario para invertir los píxeles del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="3263a-141">The blink time is the elapsed time, in milliseconds, required to invert the caret's pixels.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="3263a-142">**SetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="3263a-142">**SetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | <span data-ttu-id="3263a-143">Mueve el símbolo de intercalación a las coordenadas especificadas.</span><span class="sxs-lookup"><span data-stu-id="3263a-143">Moves the caret to the specified coordinates.</span></span> <span data-ttu-id="3263a-144">Si la ventana que posee el símbolo de intercalación se creó con el estilo de clase **CS \_ OWNDC** , las coordenadas especificadas están sujetas al modo de asignación del contexto de dispositivo asociado a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="3263a-144">If the window that owns the caret was created with the **CS\_OWNDC** class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.</span></span> <br/> |
| [<span data-ttu-id="3263a-145">**ShowCaret**</span><span class="sxs-lookup"><span data-stu-id="3263a-145">**ShowCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | <span data-ttu-id="3263a-146">Hace que el símbolo de intercalación esté visible en la pantalla en la posición actual del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="3263a-146">Makes the caret visible on the screen at the caret's current position.</span></span> <span data-ttu-id="3263a-147">Cuando el símbolo de intercalación se vuelve visible, comienza a parpadear automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3263a-147">When the caret becomes visible, it begins flashing automatically.</span></span> <br/>                                                                                                          |



 

 

