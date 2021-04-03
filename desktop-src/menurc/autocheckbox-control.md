---
title: Autocheckbox (control)
description: Define un control de casilla automática.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menús de control autocheckbox y otros recursos
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790318"
---
# <a name="autocheckbox-control"></a><span data-ttu-id="fdb19-104">Autocheckbox (control)</span><span class="sxs-lookup"><span data-stu-id="fdb19-104">AUTOCHECKBOX control</span></span>

<span data-ttu-id="fdb19-105">Define un control de casilla automática.</span><span class="sxs-lookup"><span data-stu-id="fdb19-105">Defines an automatic check box control.</span></span> <span data-ttu-id="fdb19-106">El control es un rectángulo pequeño (casilla) con el texto especificado que aparece junto a él (normalmente, a la derecha).</span><span class="sxs-lookup"><span data-stu-id="fdb19-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="fdb19-107">Cuando el usuario elige el control, el control resalta el rectángulo y envía un mensaje a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="fdb19-107">When the user chooses the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="fdb19-108">La instrucción **autocheckbox** solo se puede usar en el cuerpo de un [**cuadro de diálogo**](dialog-resource.md) o una instrucción [**DIALOGEX**](dialogex-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="fdb19-108">The **AUTOCHECKBOX** statement can only be used in the body of a [**DIALOG**](dialog-resource.md) or [**DIALOGEX**](dialogex-resource.md) statement.</span></span>

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="fdb19-109"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="fdb19-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="fdb19-110">Estilos del control.</span><span class="sxs-lookup"><span data-stu-id="fdb19-110">Styles of the control.</span></span> <span data-ttu-id="fdb19-111">Este valor puede ser una combinación del estilo de clase de botón **BS \_ autocheckbox** y los estilos **WS \_ TABSTOP** y **WS \_ Group** .</span><span class="sxs-lookup"><span data-stu-id="fdb19-111">This value can be a combination of the button class style **BS\_AUTOCHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="fdb19-112">Si no especifica un estilo, el estilo predeterminado es `BS_AUTOCHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="fdb19-112">If you do not specify a style, the default style is `BS_AUTOCHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="fdb19-113">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fdb19-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fdb19-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdb19-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb19-115">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="fdb19-115">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="fdb19-116">Estilos de botón</span><span class="sxs-lookup"><span data-stu-id="fdb19-116">Button Styles</span></span>](../controls/button-styles.md)
</dt> <dt>

[<span data-ttu-id="fdb19-117">**CASILLA**</span><span class="sxs-lookup"><span data-stu-id="fdb19-117">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="fdb19-118">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="fdb19-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="fdb19-119">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="fdb19-119">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 