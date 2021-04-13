---
title: Control COMBOBOX (menús y otros recursos)
description: Define un control de cuadro combinado (un cuadro combinado).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menús de control COMBOBOX y otros recursos
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420606"
---
# <a name="combobox-control"></a><span data-ttu-id="70e95-104">COMBOBOX (control)</span><span class="sxs-lookup"><span data-stu-id="70e95-104">COMBOBOX control</span></span>

<span data-ttu-id="70e95-105">Define un control de cuadro combinado (un cuadro combinado).</span><span class="sxs-lookup"><span data-stu-id="70e95-105">Defines a combination box control (a combo box).</span></span> <span data-ttu-id="70e95-106">Un cuadro combinado consta de un cuadro de texto estático o un cuadro de edición combinado con un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="70e95-106">A combo box consists of either a static text box or an edit box combined with a list box.</span></span> <span data-ttu-id="70e95-107">El cuadro de lista se puede mostrar en todo momento o extraerlo el usuario.</span><span class="sxs-lookup"><span data-stu-id="70e95-107">The list box can be displayed at all times or pulled down by the user.</span></span> <span data-ttu-id="70e95-108">Si el cuadro combinado contiene un cuadro de texto estático, el cuadro de texto muestra siempre la selección (si existe) en la parte del cuadro de lista del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="70e95-108">If the combo box contains a static text box, the text box always displays the selection (if any) in the list box portion of the combo box.</span></span> <span data-ttu-id="70e95-109">Si usa un cuadro de edición, el usuario puede escribir la selección deseada; el cuadro de lista resalta el primer elemento (si existe) que coincida con lo que el usuario ha escrito en el cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="70e95-109">If it uses an edit box, the user can type in the desired selection; the list box highlights the first item (if any) that matches what the user has entered in the edit box.</span></span> <span data-ttu-id="70e95-110">A continuación, el usuario puede seleccionar el elemento resaltado en el cuadro de lista para completar la selección.</span><span class="sxs-lookup"><span data-stu-id="70e95-110">The user can then select the item highlighted in the list box to complete the choice.</span></span> <span data-ttu-id="70e95-111">Además, el cuadro combinado puede estar dibujado por el propietario y tener un alto fijo o variable.</span><span class="sxs-lookup"><span data-stu-id="70e95-111">In addition, the combo box can be owner-drawn and of fixed or variable height.</span></span>

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="70e95-112"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="70e95-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="70e95-113">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="70e95-113">Control styles.</span></span> <span data-ttu-id="70e95-114">Este valor puede ser una combinación de los estilos de clase COMBOBOX y cualquiera de los siguientes estilos **: \_ WS TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL** y **WS \_ deshabilitados**.</span><span class="sxs-lookup"><span data-stu-id="70e95-114">This value can be a combination of the COMBOBOX class styles and any of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="70e95-115">Si no especifica un estilo, el estilo predeterminado es `CBS_SIMPLE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="70e95-115">If you do not specify a style, the default style is `CBS_SIMPLE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="70e95-116">El parámetro *height* se aplica al alto de un cuadro combinado con una lista desplegable totalmente expandida.</span><span class="sxs-lookup"><span data-stu-id="70e95-116">The *height* parameter applies to the height of a combo box with a drop-down list fully expanded.</span></span>

<span data-ttu-id="70e95-117">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="70e95-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="70e95-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="70e95-118">Examples</span></span>

<span data-ttu-id="70e95-119">En este ejemplo se define un control de cuadro combinado con una barra de desplazamiento vertical:</span><span class="sxs-lookup"><span data-stu-id="70e95-119">This example defines a combo-box control with a vertical scroll bar:</span></span>

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a><span data-ttu-id="70e95-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="70e95-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e95-121">Cuadros combinados</span><span class="sxs-lookup"><span data-stu-id="70e95-121">Combo Boxes</span></span>](../controls/about-combo-boxes.md)
</dt> </dl>

 

 