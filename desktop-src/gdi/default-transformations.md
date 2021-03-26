---
description: Cada vez que una aplicación crea un controlador de dominio y comienza inmediatamente a llamar a funciones de dibujo o de salida de GDI, aprovecha el espacio de página predeterminado para el espacio de dispositivo y el espacio de dispositivo a las transformaciones del área de cliente.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Transformaciones predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5f13c764a92c005fad36c9f2599b99a654284f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985003"
---
# <a name="default-transformations"></a><span data-ttu-id="14c12-103">Transformaciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="14c12-103">Default Transformations</span></span>

<span data-ttu-id="14c12-104">Cada vez que una aplicación crea un controlador de dominio y comienza inmediatamente a llamar a funciones de dibujo o de salida de GDI, aprovecha el espacio de página predeterminado para el espacio de dispositivo y el espacio de dispositivo a las transformaciones del área de cliente.</span><span class="sxs-lookup"><span data-stu-id="14c12-104">Whenever an application creates a DC and immediately begins calling GDI drawing or output functions, it takes advantage of the default page-space to device-space, and device-space to client-area transformations.</span></span> <span data-ttu-id="14c12-105">No se puede realizar una transformación de espacio de página universal hasta que la aplicación llama primero a la función [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) para establecer el modo en GM \_ Advanced y, a continuación, llama a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .</span><span class="sxs-lookup"><span data-stu-id="14c12-105">A world-to-page space transformation cannot happen until the application first calls the [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) function to set the mode to GM\_ADVANCED and then calls the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function.</span></span>

<span data-ttu-id="14c12-106">El uso de \_ texto mm (el espacio de página predeterminado para la transformación del espacio de dispositivo) da como resultado una asignación de uno a uno, es decir, un punto determinado en el espacio de la página se asigna al mismo punto en el espacio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14c12-106">Use of MM\_TEXT (the default page-space to device-space transformation) results in a one-to-one mapping; that is, a given point in page space maps to the same point in device space.</span></span> <span data-ttu-id="14c12-107">Como se mencionó anteriormente, esta transformación no se especifica mediante una matriz.</span><span class="sxs-lookup"><span data-stu-id="14c12-107">As previously mentioned, this transformation is not specified by a matrix.</span></span> <span data-ttu-id="14c12-108">En su lugar, se obtiene dividiendo el ancho de la ventanilla por el ancho de la ventana y el alto de la ventanilla por el alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="14c12-108">Instead, it is obtained by dividing the width of the viewport by the width of the window and the height of the viewport by the height of the window.</span></span> <span data-ttu-id="14c12-109">En el caso predeterminado, las dimensiones de la ventanilla son de 1 píxel por 1 píxel y las dimensiones de la ventana son una unidad de 1 página por unidad de página.</span><span class="sxs-lookup"><span data-stu-id="14c12-109">In the default case, the viewport dimensions are 1-pixel by 1-pixel and the window dimensions are 1-page unit by 1-page unit.</span></span>

<span data-ttu-id="14c12-110">La transformación espacio de dispositivo en dispositivo físico (área de cliente, escritorio o impresora) siempre da como resultado una asignación uno a uno; es decir, una unidad en el espacio del dispositivo siempre es equivalente a una unidad en el área cliente, en el escritorio o en una página.</span><span class="sxs-lookup"><span data-stu-id="14c12-110">The device-space to physical-device (client area, desktop, or printer paper) transformation always results in a one-to-one mapping; that is, one unit in device space is always equivalent to one unit in the client area, on the desktop, or on a page.</span></span> <span data-ttu-id="14c12-111">El único propósito de esta transformación es la traducción; garantiza que la salida aparece correctamente en la ventana de una aplicación, independientemente de dónde se mueva esa ventana en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="14c12-111">The sole purpose of this transformation is translation; it ensures that output appears correctly in an application's window no matter where that window is moved on the desktop.</span></span>

<span data-ttu-id="14c12-112">El aspecto único del texto MM \_ es la orientación del eje y en el espacio de la página.</span><span class="sxs-lookup"><span data-stu-id="14c12-112">The one unique aspect of MM\_TEXT is the orientation of the y-axis in page space.</span></span> <span data-ttu-id="14c12-113">En \_ el texto mm, el eje y positivo se extiende hacia abajo y el eje y negativo se extiende hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="14c12-113">In MM\_TEXT, the positive y-axis extends downward and the negative y-axis extends upward.</span></span>

 

 



