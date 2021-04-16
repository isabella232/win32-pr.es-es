---
title: Control LTEXT
description: Define un control de texto alineado a la izquierda.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menús de control de LTEXT y otros recursos
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105656355"
---
# <a name="ltext-control"></a><span data-ttu-id="0c326-104">Control LTEXT</span><span class="sxs-lookup"><span data-stu-id="0c326-104">LTEXT control</span></span>

<span data-ttu-id="0c326-105">Define un control de texto alineado a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="0c326-105">Defines a left-aligned text control.</span></span> <span data-ttu-id="0c326-106">El control es un rectángulo simple que muestra el texto especificado alineado a la izquierda en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="0c326-106">The control is a simple rectangle displaying the given text left-aligned in the rectangle.</span></span> <span data-ttu-id="0c326-107">Se aplica formato al texto antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="0c326-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="0c326-108">Las palabras que se extienden más allá del final de una línea se ajustan automáticamente al principio de la línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="0c326-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="0c326-109">Las palabras que superan el ancho del control se truncan.</span><span class="sxs-lookup"><span data-stu-id="0c326-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="0c326-110">La instrucción **LTEXT** , que solo se puede usar en una instrucción [**DIALOGEX**](dialogex-resource.md) , define el texto, el identificador, las dimensiones y los atributos del control.</span><span class="sxs-lookup"><span data-stu-id="0c326-110">The **LTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0c326-111"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="0c326-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0c326-112">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="0c326-112">Control styles.</span></span> <span data-ttu-id="0c326-113">Este valor puede ser cualquier combinación del estilo **de \_ RADIOBUTTON de BS** y los siguientes estilos **: SS \_ left**, **WS \_ TABSTOP** y **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="0c326-113">This value can be any combination of the **BS\_RADIOBUTTON** style and the following styles: **SS\_LEFT**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="0c326-114">Si no especifica un estilo, el estilo predeterminado es `SS_LEFT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="0c326-114">If you do not specify a style, the default style is `SS_LEFT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="0c326-115">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0c326-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0c326-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0c326-116">Examples</span></span>

<span data-ttu-id="0c326-117">En este ejemplo se define un control de texto alineado a la izquierda que tiene la etiqueta nombre de archivo:</span><span class="sxs-lookup"><span data-stu-id="0c326-117">This example defines a left-aligned text control that is labeled Filename:</span></span>

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="0c326-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c326-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c326-119">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="0c326-119">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="0c326-120">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="0c326-120">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="0c326-121">Controles de edición</span><span class="sxs-lookup"><span data-stu-id="0c326-121">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="0c326-122">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="0c326-122">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 