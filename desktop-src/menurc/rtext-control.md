---
title: Control RTEXT
description: Define un control de texto alineado a la derecha.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menús de control de RTEXT y otros recursos
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487710"
---
# <a name="rtext-control"></a><span data-ttu-id="10bb8-104">Control RTEXT</span><span class="sxs-lookup"><span data-stu-id="10bb8-104">RTEXT control</span></span>

<span data-ttu-id="10bb8-105">Define un control de texto alineado a la derecha.</span><span class="sxs-lookup"><span data-stu-id="10bb8-105">Defines a right-aligned text control.</span></span> <span data-ttu-id="10bb8-106">El control es un rectángulo simple que muestra el texto especificado alineado a la derecha en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="10bb8-106">The control is a simple rectangle displaying the given text right-aligned in the rectangle.</span></span> <span data-ttu-id="10bb8-107">Se aplica formato al texto antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="10bb8-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="10bb8-108">Las palabras que se extienden más allá del final de una línea se ajustan automáticamente al principio de la línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="10bb8-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="10bb8-109">Las palabras que superan el ancho del control se truncan.</span><span class="sxs-lookup"><span data-stu-id="10bb8-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="10bb8-110">La instrucción **RText** , que solo se puede usar en una instrucción [**DIALOGEX**](dialogex-resource.md) , define el texto, el identificador, las dimensiones y los atributos del control.</span><span class="sxs-lookup"><span data-stu-id="10bb8-110">The **RTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="10bb8-111"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="10bb8-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="10bb8-112">Estilos para el control de texto, que puede ser cualquier combinación de los siguientes: **WS \_ TABSTOP** y **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="10bb8-112">Styles for the text control, which can be any combination of the following: **WS\_TABSTOP** and **WS\_GROUP**.</span></span>

<span data-ttu-id="10bb8-113">Si no especifica un estilo, el estilo predeterminado es `SS_RIGHT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="10bb8-113">If you do not specify a style, the default style is `SS_RIGHT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="10bb8-114">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="10bb8-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="10bb8-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="10bb8-115">Examples</span></span>

<span data-ttu-id="10bb8-116">En el ejemplo siguiente se muestra el uso de la instrucción **RText** :</span><span class="sxs-lookup"><span data-stu-id="10bb8-116">The following example demonstrates the use of the **RTEXT** statement:</span></span>

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="10bb8-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="10bb8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10bb8-118">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="10bb8-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="10bb8-119">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="10bb8-119">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="10bb8-120">Controles de edición</span><span class="sxs-lookup"><span data-stu-id="10bb8-120">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="10bb8-121">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="10bb8-121">**LTEXT**</span></span>](ltext-control.md)
</dt> </dl>

 

 