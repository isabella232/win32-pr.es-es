---
description: Información general sobre cómo asignar un nombre a una ventana de forma adecuada y establecer el título de la ventana para Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Asignar un nombre adecuado a una ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659931"
---
# <a name="naming-a-window-appropriately"></a><span data-ttu-id="cd9eb-103">Asignar un nombre adecuado a una ventana</span><span class="sxs-lookup"><span data-stu-id="cd9eb-103">Naming a Window Appropriately</span></span>

<span data-ttu-id="cd9eb-104">Asigne a cada ventana un título descriptivo, incluso si la ventana o su título es invisible.</span><span class="sxs-lookup"><span data-stu-id="cd9eb-104">Assign every window a user-friendly caption, even if the window or its caption is invisible.</span></span> <span data-ttu-id="cd9eb-105">Esto permite que la funcionalidad de voz identifique la ventana y la jerarquía de ventanas.</span><span class="sxs-lookup"><span data-stu-id="cd9eb-105">This allows the speech functionality to identify the window and the window hierarchy.</span></span> <span data-ttu-id="cd9eb-106">Esta recomendación se aplica a todas las ventanas: ventanas de nivel superior con fotogramas visibles; ventanas secundarias, como las paletas flotantes; controles personalizados; barras los paneles y dentro de una ventana, cuando se implementan como ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="cd9eb-106">This recommendation applies to all windows: top-level windows with visible frames; child windows, such as floating palettes; custom controls; toolbars; and panes within a window, when implemented as child windows.</span></span>

<span data-ttu-id="cd9eb-107">Hay tres maneras de establecer el título de la ventana:</span><span class="sxs-lookup"><span data-stu-id="cd9eb-107">There are three ways to set the window caption:</span></span>

-   <span data-ttu-id="cd9eb-108">Establezca la cadena en el script de recursos cuando llame a [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o a funciones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cd9eb-108">Set the string in your resource script when calling [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or related functions.</span></span>
-   <span data-ttu-id="cd9eb-109">Llame a la función [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="cd9eb-109">Call the [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) function.</span></span>
-   <span data-ttu-id="cd9eb-110">Defina el nombre de los controles en los cuadros de diálogo mediante las técnicas descritas en [nombrar controles en los cuadros de diálogo](naming-controls-in-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="cd9eb-110">Define the name of controls in dialog boxes by using the techniques described in [Naming Controls in Dialog Boxes](naming-controls-in-dialog-boxes.md).</span></span> <span data-ttu-id="cd9eb-111">Este es el único método para etiquetar un control de edición, ya que el establecimiento de la etiqueta intrínseca Controls cambia el contenido de los controles.</span><span class="sxs-lookup"><span data-stu-id="cd9eb-111">This is the only method for labeling an edit control, because setting the controls intrinsic label changes the controls contents.</span></span>

<span data-ttu-id="cd9eb-112">Puede consultar el título mediante Microsoft Active Accessibility o el mensaje de GETTEXT de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="cd9eb-112">You can query the caption by using either Microsoft Active Accessibility or the WM\_GETTEXT message.</span></span>

<span data-ttu-id="cd9eb-113">Para obtener más información sobre cómo consultar el título mediante Active Accessibility, vea la sección [accesibilidad](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="cd9eb-113">For more information about querying the caption by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
