---
title: Control PUSHBUTTON (menús y otros recursos)
description: Define un control de botón de reenvío. El control es un rectángulo de esquinas redondas que contiene el texto especificado. El texto se centra en el control. El control envía un mensaje a su elemento primario cada vez que el usuario elige el control.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menús de control de PULSAdores y otros recursos
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358972"
---
# <a name="pushbutton-control"></a><span data-ttu-id="144a9-107">Control PUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="144a9-107">PUSHBUTTON control</span></span>

<span data-ttu-id="144a9-108">Define un control de botón de reenvío.</span><span class="sxs-lookup"><span data-stu-id="144a9-108">Defines a push-button control.</span></span> <span data-ttu-id="144a9-109">El control es un rectángulo de esquinas redondas que contiene el texto especificado.</span><span class="sxs-lookup"><span data-stu-id="144a9-109">The control is a round-cornered rectangle containing the given text.</span></span> <span data-ttu-id="144a9-110">El texto se centra en el control.</span><span class="sxs-lookup"><span data-stu-id="144a9-110">The text is centered in the control.</span></span> <span data-ttu-id="144a9-111">El control envía un mensaje a su elemento primario cada vez que el usuario elige el control.</span><span class="sxs-lookup"><span data-stu-id="144a9-111">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="144a9-112"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="144a9-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="144a9-113">Estilos para el Pushbutton, que puede ser una combinación del estilo **de \_ pulsador de BS** y los siguientes estilos: **WS \_ TABSTOP**, **WS \_ Disabled** y **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="144a9-113">Styles for the pushbutton, which can be a combination of the **BS\_PUSHBUTTON** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="144a9-114">Si no especifica un estilo, el estilo predeterminado es `BS_PUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="144a9-114">If you do not specify a style, the default style is `BS_PUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="144a9-115">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="144a9-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="144a9-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="144a9-116">Examples</span></span>

<span data-ttu-id="144a9-117">En el siguiente ejemplo se muestra el uso de la instrucción **PUSHBUTTON** :</span><span class="sxs-lookup"><span data-stu-id="144a9-117">The following example demonstrates the use of the **PUSHBUTTON** statement:</span></span>

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a><span data-ttu-id="144a9-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="144a9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="144a9-119">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="144a9-119">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="144a9-120">Botones de reenvío</span><span class="sxs-lookup"><span data-stu-id="144a9-120">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 