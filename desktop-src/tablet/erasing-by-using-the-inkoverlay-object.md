---
description: El objeto InkOverlay se puede adjuntar a un control de ventana y se usa para habilitar la capacidad básica de entrada de lápiz.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Borrar mediante el objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf85926f3566340cbde0d3202f3485e7c54cccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810087"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a><span data-ttu-id="01c31-103">Borrar mediante el objeto InkOverlay</span><span class="sxs-lookup"><span data-stu-id="01c31-103">Erasing by Using the InkOverlay Object</span></span>

<span data-ttu-id="01c31-104">El objeto [**InkOverlay**](inkoverlay-class.md) se puede adjuntar a un control de ventana y se usa para habilitar la capacidad básica de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="01c31-104">The [**InkOverlay**](inkoverlay-class.md) object can be attached to a window control and is used to enable basic ink capability.</span></span> <span data-ttu-id="01c31-105">Puede usar el objeto **InkOverlay** para borrar la entrada de lápiz; para ello, establezca la propiedad [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) en **Delete**.</span><span class="sxs-lookup"><span data-stu-id="01c31-105">You can use the **InkOverlay** object to erase ink by setting the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) property equal to **Delete**.</span></span> <span data-ttu-id="01c31-106">Después, puede establecer la propiedad [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) en los miembros de **trazo** o **punto** de [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span><span class="sxs-lookup"><span data-stu-id="01c31-106">You can then set the [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) property to either the **Stroke** or **Point** members of [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span></span> <span data-ttu-id="01c31-107">Al establecer la propiedad **EraserMode** en **Stroke** , se borran los trazos completos.</span><span class="sxs-lookup"><span data-stu-id="01c31-107">Setting the **EraserMode** property to **Stroke** erases entire strokes.</span></span> <span data-ttu-id="01c31-108">Al establecer la propiedad **EraserMode** en **Point** , se borra la tinta que pasa el cursor.</span><span class="sxs-lookup"><span data-stu-id="01c31-108">Setting the **EraserMode** property to **Point** erases the ink that the cursor passes over.</span></span>

 

 



