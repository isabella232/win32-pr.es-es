---
title: Usar controles TrackBar
description: En esta sección se proporcionan detalles y ejemplos de implementación de los controles TrackBar.
ms.assetid: 28078f3e-a3d1-4bb5-96c6-2191ff9f8d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d667a495dce918bdcfcf0391638eef8a3c6e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775558"
---
# <a name="using-trackbar-controls"></a><span data-ttu-id="e383a-103">Usar controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="e383a-103">Using Trackbar Controls</span></span>

<span data-ttu-id="e383a-104">En esta sección se proporcionan detalles y ejemplos de implementación de los controles TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e383a-104">This section provides implementation details and examples for Trackbar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e383a-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e383a-105">In this section</span></span>



| <span data-ttu-id="e383a-106">Tema</span><span class="sxs-lookup"><span data-stu-id="e383a-106">Topic</span></span>                                                                                                  | <span data-ttu-id="e383a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e383a-107">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e383a-108">Cómo crear un TrackBar</span><span class="sxs-lookup"><span data-stu-id="e383a-108">How to Create a Trackbar</span></span>](create-a-trackbar.md)<br/>                                           | <span data-ttu-id="e383a-109">Cuando se crea la barra de inicio, se inicializan su intervalo y su intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="e383a-109">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="e383a-110">También se establece el tamaño de página en este momento.</span><span class="sxs-lookup"><span data-stu-id="e383a-110">The page size is also set at this time.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="e383a-111">Cómo procesar mensajes de notificación de TrackBar</span><span class="sxs-lookup"><span data-stu-id="e383a-111">How to Process Trackbar Notification Messages</span></span>](process-trackbar-notification-messages.md)<br/> | <span data-ttu-id="e383a-112">Trackbars notifique a su ventana primaria de las acciones del usuario mediante el envío de un mensaje primario a [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="e383a-112">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="e383a-113">Cómo limitar el movimiento del control deslizante</span><span class="sxs-lookup"><span data-stu-id="e383a-113">How to Limit Slider Movement</span></span>](limit-slider-movement.md)<br/>                                   | <span data-ttu-id="e383a-114">Tal y como se describe en [acerca de los controles TrackBar](trackbar-controls.md), es posible establecer una parte del intervalo de la barra de control como un intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="e383a-114">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="e383a-115">Un propósito de un intervalo de selección puede ser limitar el movimiento del control deslizante, haciendo que algunas partes de los límites del intervalo completo estén desactivadas.</span><span class="sxs-lookup"><span data-stu-id="e383a-115">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span> <br/> |
| [<span data-ttu-id="e383a-116">Cómo usar las ventanas de amigos</span><span class="sxs-lookup"><span data-stu-id="e383a-116">How to Use Buddy Windows</span></span>](use-buddy-windows.md)<br/>                                           | <span data-ttu-id="e383a-117">Al establecer otros controles como ventanas de amigos para una barra de control, puede colocar automáticamente esos controles en los extremos de la barra de control como etiquetas.</span><span class="sxs-lookup"><span data-stu-id="e383a-117">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span><br/>                                                                                                                          |



 

 

 





