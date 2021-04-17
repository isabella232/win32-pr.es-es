---
title: CHECKBOX (control del compilador de recursos)
description: Define un control de casilla.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menús de control de casilla y otros recursos
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704945"
---
# <a name="checkbox-control"></a><span data-ttu-id="f6735-104">CHECKBOX (control)</span><span class="sxs-lookup"><span data-stu-id="f6735-104">CHECKBOX control</span></span>

<span data-ttu-id="f6735-105">Define un control de casilla.</span><span class="sxs-lookup"><span data-stu-id="f6735-105">Defines a check box control.</span></span> <span data-ttu-id="f6735-106">El control es un rectángulo pequeño (casilla) con el texto especificado que aparece junto a él (normalmente, a la derecha).</span><span class="sxs-lookup"><span data-stu-id="f6735-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="f6735-107">Cuando el usuario selecciona el control, el control resalta el rectángulo y envía un mensaje a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="f6735-107">When the user selects the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="f6735-108">La instrucción **CheckBox** , que solo se puede utilizar en una instrucción [**DIALOGEX**](dialogex-resource.md) , define el texto, el identificador, las dimensiones y los atributos del control.</span><span class="sxs-lookup"><span data-stu-id="f6735-108">The **CHECKBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="f6735-109"><span id="text"></span><span id="TEXT"></span>*negrita*</span><span class="sxs-lookup"><span data-stu-id="f6735-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="f6735-110">Texto que se va a mostrar a la derecha del control.</span><span class="sxs-lookup"><span data-stu-id="f6735-110">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="f6735-111"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="f6735-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="f6735-112">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="f6735-112">Control styles.</span></span> <span data-ttu-id="f6735-113">Este valor puede ser una combinación de la **\_ casilla** de estilo de clase de botón BS y los estilos de **WS \_ TABSTOP** y de **\_ grupo de WS** .</span><span class="sxs-lookup"><span data-stu-id="f6735-113">This value can be a combination of the button class style **BS\_CHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="f6735-114">Si no especifica un estilo, el estilo predeterminado es `BS_CHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="f6735-114">If you do not specify a style, the default style is `BS_CHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="f6735-115">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f6735-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f6735-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f6735-116">Examples</span></span>

<span data-ttu-id="f6735-117">En este ejemplo se define un control de casilla con la etiqueta Italic:</span><span class="sxs-lookup"><span data-stu-id="f6735-117">This example defines a check-box control that is labeled Italic:</span></span>

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="f6735-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6735-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6735-119">**Autocheckbox**</span><span class="sxs-lookup"><span data-stu-id="f6735-119">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="f6735-120">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="f6735-120">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="f6735-121">Casillas</span><span class="sxs-lookup"><span data-stu-id="f6735-121">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="f6735-122">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="f6735-122">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="f6735-123">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="f6735-123">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 