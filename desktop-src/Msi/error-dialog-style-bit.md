---
description: Si se establece este bit, el cuadro de diálogo es un cuadro de diálogo de error.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit de estilo del cuadro de diálogo de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652483"
---
# <a name="error-dialog-style-bit"></a><span data-ttu-id="5834c-103">Bit de estilo del cuadro de diálogo de error</span><span class="sxs-lookup"><span data-stu-id="5834c-103">Error Dialog Style Bit</span></span>

<span data-ttu-id="5834c-104">Si se establece este bit, el cuadro de diálogo es un cuadro de diálogo de error.</span><span class="sxs-lookup"><span data-stu-id="5834c-104">If this bit is set, the dialog box is an error dialog.</span></span>

<span data-ttu-id="5834c-105">Puede haber más de un cuadro de diálogo con este estilo.</span><span class="sxs-lookup"><span data-stu-id="5834c-105">There can be more than one dialog with this style.</span></span> <span data-ttu-id="5834c-106">La propiedad **ErrorDialog** determina qué cuadro de diálogo se usa como cuadro de diálogo de error.</span><span class="sxs-lookup"><span data-stu-id="5834c-106">The **ErrorDialog** property determines which dialog is used as an error dialog.</span></span> <span data-ttu-id="5834c-107">El cuadro de diálogo seleccionado solo puede ser uno de los que tienen este bit de estilo establecido.</span><span class="sxs-lookup"><span data-stu-id="5834c-107">The selected dialog can be only one of those that have this style bit set.</span></span> <span data-ttu-id="5834c-108">El cuadro de diálogo de error debe tener un control de texto estático denominado ErrorText.</span><span class="sxs-lookup"><span data-stu-id="5834c-108">The error dialog must have a static text control named ErrorText.</span></span> <span data-ttu-id="5834c-109">Este control recibe el texto del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="5834c-109">This control receives the text of the error message.</span></span> <span data-ttu-id="5834c-110">El cuadro de diálogo también debe tener los siete botones de reenvío correspondientes a los posibles valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="5834c-110">The dialog should also have the seven push buttons corresponding to the possible return values.</span></span> <span data-ttu-id="5834c-111">El mensaje de error determina cuál de estos botones se muestra realmente.</span><span class="sxs-lookup"><span data-stu-id="5834c-111">The error message determines which of these buttons are actually displayed.</span></span> <span data-ttu-id="5834c-112">Los botones mostrados se reorganizan de modo que se distribuyan uniformemente en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5834c-112">The displayed buttons are rearranged so they are evenly distributed on the dialog.</span></span> <span data-ttu-id="5834c-113">Esta reorganización cambia la coordenada X de los botones, pero no las otras tres coordenadas.</span><span class="sxs-lookup"><span data-stu-id="5834c-113">This rearrangement changes the X coordinate of the buttons, but not the other three coordinates.</span></span> <span data-ttu-id="5834c-114">Por lo tanto, es aconsejable que no se cree ningún otro control en la misma región horizontal del cuadro de diálogo que los botones.</span><span class="sxs-lookup"><span data-stu-id="5834c-114">Therefore it is advisable that no other control should be authored in the same horizontal region of the dialog as the buttons.</span></span> <span data-ttu-id="5834c-115">Si el mensaje de error no especifica ningún botón, se muestra el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="5834c-115">If the error message specifies no button, the **OK** button is displayed.</span></span> <span data-ttu-id="5834c-116">El botón **predeterminado** , el primer control activo y los valores del botón **Cancelar** se omiten en un cuadro de diálogo de error.</span><span class="sxs-lookup"><span data-stu-id="5834c-116">The **Default** button, First active control and **Cancel** button values are ignored for an error dialog.</span></span> <span data-ttu-id="5834c-117">El botón **predeterminado** definido en el mensaje de error se asignará a los tres valores.</span><span class="sxs-lookup"><span data-stu-id="5834c-117">The **Default** button defined in the error message will be assigned to all three values.</span></span> <span data-ttu-id="5834c-118">El efecto de insertar estos botones debe definirse en la [tabla ControlEvent,](controlevent-table.md) como para todos los demás botones.</span><span class="sxs-lookup"><span data-stu-id="5834c-118">The effect of pushing these buttons have to be defined in the [ControlEvent table](controlevent-table.md) just like for all other buttons.</span></span> <span data-ttu-id="5834c-119">El título del cuadro de diálogo se crea de forma similar a otros cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5834c-119">The title of the dialog is authored in a way similar to other dialogs.</span></span> <span data-ttu-id="5834c-120">Se puede sobrescribir con el mensaje de error si especifica un texto de encabezado después de la lista de botones.</span><span class="sxs-lookup"><span data-stu-id="5834c-120">It can get overwritten by the error message if it specifies a header text after the button list.</span></span>

## <a name="value"></a><span data-ttu-id="5834c-121">Value</span><span class="sxs-lookup"><span data-stu-id="5834c-121">Value</span></span>



| <span data-ttu-id="5834c-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="5834c-122">Decimal</span></span> | <span data-ttu-id="5834c-123">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="5834c-123">Hexadecimal</span></span> | <span data-ttu-id="5834c-124">Constante</span><span class="sxs-lookup"><span data-stu-id="5834c-124">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="5834c-125">65536</span><span class="sxs-lookup"><span data-stu-id="5834c-125">65536</span></span>   | <span data-ttu-id="5834c-126">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5834c-126">0x00010000</span></span>  | <span data-ttu-id="5834c-127">**msidbDialogAttributesError**</span><span class="sxs-lookup"><span data-stu-id="5834c-127">**msidbDialogAttributesError**</span></span> |



 

 

 



