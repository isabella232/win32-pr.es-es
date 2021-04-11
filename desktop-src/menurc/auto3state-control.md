---
title: Control AUTO3STATE
description: Define una casilla de tres Estados automática.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menús de control de AUTO3STATE y otros recursos
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149232"
---
# <a name="auto3state-control"></a><span data-ttu-id="0c80f-104">Control AUTO3STATE</span><span class="sxs-lookup"><span data-stu-id="0c80f-104">AUTO3STATE control</span></span>

<span data-ttu-id="0c80f-105">Define una casilla de tres Estados automática.</span><span class="sxs-lookup"><span data-stu-id="0c80f-105">Defines an automatic three-state check box.</span></span> <span data-ttu-id="0c80f-106">El control es un cuadro abierto con el texto especificado situado a la derecha del cuadro.</span><span class="sxs-lookup"><span data-stu-id="0c80f-106">The control is an open box with the given text positioned to the right of the box.</span></span> <span data-ttu-id="0c80f-107">Cuando se elige, el cuadro avanza automáticamente entre tres Estados: activado, desactivado y deshabilitado (atenuado).</span><span class="sxs-lookup"><span data-stu-id="0c80f-107">When chosen, the box automatically advances between three states: checked, unchecked, and disabled (grayed).</span></span> <span data-ttu-id="0c80f-108">El control envía un mensaje a su elemento primario cada vez que el usuario elige el control.</span><span class="sxs-lookup"><span data-stu-id="0c80f-108">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0c80f-109"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="0c80f-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0c80f-110">Estilos para el control, que puede ser una combinación del estilo **BS \_ AUTO3STATE** y los siguientes estilos: **WS \_ TABSTOP**, **WS \_ Disabled** y **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="0c80f-110">Styles for the control, which can be a combination of the **BS\_AUTO3STATE** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="0c80f-111">Si no especifica un estilo, el estilo predeterminado es `BS_AUTO3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="0c80f-111">If you do not specify a style, the default style is `BS_AUTO3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="0c80f-112">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0c80f-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0c80f-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c80f-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c80f-114">**Autocheckbox**</span><span class="sxs-lookup"><span data-stu-id="0c80f-114">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="0c80f-115">Casillas</span><span class="sxs-lookup"><span data-stu-id="0c80f-115">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="0c80f-116">**CASILLA**</span><span class="sxs-lookup"><span data-stu-id="0c80f-116">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="0c80f-117">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="0c80f-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="0c80f-118">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="0c80f-118">**STATE3**</span></span>](state3-control.md)
</dt> <dt>

[<span data-ttu-id="0c80f-119">Estilos de ventana</span><span class="sxs-lookup"><span data-stu-id="0c80f-119">Window Styles</span></span>](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 