---
title: Control GROUPBOX (menús y otros recursos)
description: Define un control de cuadro de grupo. El control es un rectángulo que agrupa otros controles. Los controles se agrupan dibujando un borde alrededor de ellos y mostrando el texto determinado en la esquina superior izquierda.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menús de control GROUPBOX y otros recursos
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104077061"
---
# <a name="groupbox-control"></a><span data-ttu-id="a41d5-106">GROUPBOX (control)</span><span class="sxs-lookup"><span data-stu-id="a41d5-106">GROUPBOX control</span></span>

<span data-ttu-id="a41d5-107">Define un control de cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="a41d5-107">Defines a group box control.</span></span> <span data-ttu-id="a41d5-108">El control es un rectángulo que agrupa otros controles.</span><span class="sxs-lookup"><span data-stu-id="a41d5-108">The control is a rectangle that groups other controls together.</span></span> <span data-ttu-id="a41d5-109">Los controles se agrupan dibujando un borde alrededor de ellos y mostrando el texto determinado en la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="a41d5-109">The controls are grouped by drawing a border around them and displaying the given text in the upper-left corner.</span></span>

<span data-ttu-id="a41d5-110">La instrucción **GROUPBOX** , que solo se puede usar en una instrucción [**DIALOGEX**](dialogex-resource.md) , define el texto, el identificador, las dimensiones y los atributos de una ventana de control.</span><span class="sxs-lookup"><span data-stu-id="a41d5-110">The **GROUPBOX** statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="a41d5-111"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="a41d5-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="a41d5-112">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="a41d5-112">Control styles.</span></span> <span data-ttu-id="a41d5-113">Este valor puede ser una combinación del estilo de clase de botón **BS \_ GROUPBOX** y los estilos de **WS \_ TABSTOP** y **WS \_ deshabilitados** .</span><span class="sxs-lookup"><span data-stu-id="a41d5-113">This value can be a combination of the button class style **BS\_GROUPBOX** and the **WS\_TABSTOP** and **WS\_DISABLED** styles.</span></span>

<span data-ttu-id="a41d5-114">Si no especifica un estilo, el estilo predeterminado es **BS \_ GROUPBOX**.</span><span class="sxs-lookup"><span data-stu-id="a41d5-114">If you do not specify a style, the default style is **BS\_GROUPBOX**.</span></span>

</dd> </dl>

<span data-ttu-id="a41d5-115">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a41d5-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a41d5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a41d5-116">Remarks</span></span>

<span data-ttu-id="a41d5-117">Cuando el estilo contiene **WS \_ TABSTOP** o el texto especifica un acelerador, el tabulador o la tecla de aceleración mueve el foco al primer control del grupo.</span><span class="sxs-lookup"><span data-stu-id="a41d5-117">When the style contains **WS\_TABSTOP** or the text specifies an accelerator, tabbing or pressing the accelerator key moves the focus to the first control within the group.</span></span>

## <a name="examples"></a><span data-ttu-id="a41d5-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a41d5-118">Examples</span></span>

<span data-ttu-id="a41d5-119">En este ejemplo se define un control de cuadro de grupo que tiene la etiqueta opciones:</span><span class="sxs-lookup"><span data-stu-id="a41d5-119">This example defines a group-box control that is labeled Options:</span></span>

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="a41d5-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a41d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41d5-121">Cuadros de grupo</span><span class="sxs-lookup"><span data-stu-id="a41d5-121">Group Boxes</span></span>](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




