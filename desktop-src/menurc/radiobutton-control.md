---
title: RADIOBUTTON (control)
description: Define un control de botón de radio.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menús de controles RADIOBUTTON y otros recursos
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077751"
---
# <a name="radiobutton-control"></a><span data-ttu-id="82dd3-104">RADIOBUTTON (control)</span><span class="sxs-lookup"><span data-stu-id="82dd3-104">RADIOBUTTON control</span></span>

<span data-ttu-id="82dd3-105">Define un control de botón de radio.</span><span class="sxs-lookup"><span data-stu-id="82dd3-105">Defines a radio-button control.</span></span> <span data-ttu-id="82dd3-106">El control es un círculo pequeño que tiene el texto especificado que se muestra junto a él, normalmente a su derecha.</span><span class="sxs-lookup"><span data-stu-id="82dd3-106">The control is a small circle that has the given text displayed next to it, typically to its right.</span></span> <span data-ttu-id="82dd3-107">El control resalta el círculo y envía un mensaje a su ventana primaria cuando el usuario selecciona el botón.</span><span class="sxs-lookup"><span data-stu-id="82dd3-107">The control highlights the circle and sends a message to its parent window when the user selects the button.</span></span> <span data-ttu-id="82dd3-108">El control quita el resaltado y envía un mensaje cuando se selecciona el botón siguiente.</span><span class="sxs-lookup"><span data-stu-id="82dd3-108">The control removes the highlight and sends a message when the button is next selected.</span></span>

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="82dd3-109"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="82dd3-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="82dd3-110">Estilos del botón de radio, que puede ser una combinación de estilos de clase de botón y los siguientes estilos: **WS \_ TABSTOP**, **WS \_ Disabled** y **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="82dd3-110">Styles for the radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="82dd3-111">Si no especifica un estilo, el estilo predeterminado es `BS_RADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="82dd3-111">If you do not specify a style, the default style is `BS_RADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="82dd3-112">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="82dd3-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="82dd3-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="82dd3-113">Examples</span></span>

<span data-ttu-id="82dd3-114">En el ejemplo siguiente se muestra el uso de la instrucción **RADIOBUTTON** :</span><span class="sxs-lookup"><span data-stu-id="82dd3-114">The following example demonstrates the use of the **RADIOBUTTON** statement:</span></span>

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="82dd3-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="82dd3-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82dd3-116">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="82dd3-116">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="82dd3-117">Botones de radio</span><span class="sxs-lookup"><span data-stu-id="82dd3-117">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 