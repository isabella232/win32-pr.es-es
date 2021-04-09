---
title: SCROLLBAR (control)
description: Define un control de barra de desplazamiento.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menús de control SCROLLBAR y otros recursos
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149271"
---
# <a name="scrollbar-control"></a><span data-ttu-id="489e0-104">SCROLLBAR (control)</span><span class="sxs-lookup"><span data-stu-id="489e0-104">SCROLLBAR control</span></span>

<span data-ttu-id="489e0-105">Define un control de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="489e0-105">Defines a scroll-bar control.</span></span> <span data-ttu-id="489e0-106">El control es un rectángulo que contiene un cuadro de desplazamiento y tiene flechas de dirección en ambos extremos.</span><span class="sxs-lookup"><span data-stu-id="489e0-106">The control is a rectangle that contains a scroll box and has direction arrows at both ends.</span></span> <span data-ttu-id="489e0-107">El control de barra de desplazamiento envía un mensaje de notificación a su elemento primario cada vez que el usuario hace clic con el mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="489e0-107">The scroll-bar control sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="489e0-108">El elemento primario es responsable de actualizar la posición del cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="489e0-108">The parent is responsible for updating the scroll-box position.</span></span> <span data-ttu-id="489e0-109">Los controles de barra de desplazamiento se pueden colocar en cualquier parte de una ventana y usarse siempre que sea necesario para proporcionar la entrada de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="489e0-109">Scroll-bar controls can be positioned anywhere in a window and used whenever needed to provide scrolling input.</span></span>

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="489e0-110"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="489e0-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="489e0-111">Cero o una combinación de los siguientes estilos: **WS \_ TABSTOP**, **WS \_ Group** y **WS \_ deshabilitados**.</span><span class="sxs-lookup"><span data-stu-id="489e0-111">Zero or a combination of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="489e0-112">Además de estos estilos, el parámetro *Style* puede contener una combinación (o ninguno) de los estilos de clase ScrollBar.</span><span class="sxs-lookup"><span data-stu-id="489e0-112">In addition to these styles, the *style* parameter may contain a combination (or none) of the SCROLLBAR-class styles.</span></span>

<span data-ttu-id="489e0-113">Si no especifica un estilo, el estilo predeterminado es **SBS \_ horizontal**.</span><span class="sxs-lookup"><span data-stu-id="489e0-113">If you do not specify a style, the default style is **SBS\_HORZ**.</span></span>

</dd> </dl>

<span data-ttu-id="489e0-114">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="489e0-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span> <span data-ttu-id="489e0-115">Tenga en cuenta que no puede especificar texto para este control.</span><span class="sxs-lookup"><span data-stu-id="489e0-115">Note that you cannot specify text for this control.</span></span>

## <a name="examples"></a><span data-ttu-id="489e0-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="489e0-116">Examples</span></span>

<span data-ttu-id="489e0-117">En el ejemplo siguiente se muestra el uso de la instrucción **ScrollBar** :</span><span class="sxs-lookup"><span data-stu-id="489e0-117">The following example demonstrates the use of the **SCROLLBAR** statement:</span></span>

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a><span data-ttu-id="489e0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="489e0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489e0-119">Barras de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="489e0-119">Scroll Bars</span></span>](../controls/about-scroll-bars.md)
</dt> </dl>

 

 