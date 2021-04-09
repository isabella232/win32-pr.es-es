---
title: Control CTEXT
description: Define un control de texto centrado.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menús de control de CTEXT y otros recursos
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149230"
---
# <a name="ctext-control"></a><span data-ttu-id="2ad75-104">Control CTEXT</span><span class="sxs-lookup"><span data-stu-id="2ad75-104">CTEXT control</span></span>

<span data-ttu-id="2ad75-105">Define un control de texto centrado.</span><span class="sxs-lookup"><span data-stu-id="2ad75-105">Defines a centered-text control.</span></span> <span data-ttu-id="2ad75-106">El control es un rectángulo simple que muestra el texto especificado centrado en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="2ad75-106">The control is a simple rectangle displaying the given text centered in the rectangle.</span></span> <span data-ttu-id="2ad75-107">Se aplica formato al texto antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="2ad75-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="2ad75-108">Las palabras que se extienden más allá del final de una línea se ajustan automáticamente al principio de la línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="2ad75-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="2ad75-109">Las palabras que superan el ancho del control se truncan.</span><span class="sxs-lookup"><span data-stu-id="2ad75-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="2ad75-110">La instrucción [**LTEXT**](ltext-control.md) , que solo se puede usar en una instrucción REP, define el texto, el identificador, las dimensiones y los atributos del control.</span><span class="sxs-lookup"><span data-stu-id="2ad75-110">The [**LTEXT**](ltext-control.md) statement, which can be used only in a rep statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="2ad75-111"><span id="text"></span><span id="TEXT"></span>*negrita*</span><span class="sxs-lookup"><span data-stu-id="2ad75-111"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="2ad75-112">Texto que se va a centrar en el área rectangular del control.</span><span class="sxs-lookup"><span data-stu-id="2ad75-112">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2ad75-113"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="2ad75-113"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="2ad75-114">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="2ad75-114">Control styles.</span></span> <span data-ttu-id="2ad75-115">Este valor puede ser cualquier combinación de los siguientes estilos: **SS \_ Center**, **WS \_ TABSTOP** y **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="2ad75-115">This value can be any combination of the following styles: **SS\_CENTER**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="2ad75-116">Si no especifica un estilo, el estilo predeterminado es `SS_CENTER | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="2ad75-116">If you do not specify a style, the default style is `SS_CENTER | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="2ad75-117">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2ad75-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2ad75-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2ad75-118">Examples</span></span>

<span data-ttu-id="2ad75-119">En este ejemplo se define un control de texto centrado con la etiqueta nombre de archivo:</span><span class="sxs-lookup"><span data-stu-id="2ad75-119">This example defines a centered-text control that is labeled Filename:</span></span>

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a><span data-ttu-id="2ad75-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ad75-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad75-121">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="2ad75-121">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="2ad75-122">Controles de edición</span><span class="sxs-lookup"><span data-stu-id="2ad75-122">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="2ad75-123">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="2ad75-123">**LTEXT**</span></span>](ltext-control.md)
</dt> <dt>

[<span data-ttu-id="2ad75-124">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="2ad75-124">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 