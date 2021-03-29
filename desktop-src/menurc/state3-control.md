---
title: Control STATE3
description: Define un control de casilla de tres Estados. El control es idéntico al de una casilla, con la excepción de que tiene tres Estados activado, desactivado y deshabilitado (atenuado).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menús de control de STATE3 y otros recursos
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783665"
---
# <a name="state3-control"></a><span data-ttu-id="770c2-105">Control STATE3</span><span class="sxs-lookup"><span data-stu-id="770c2-105">STATE3 control</span></span>

<span data-ttu-id="770c2-106">Define un control de casilla de tres Estados.</span><span class="sxs-lookup"><span data-stu-id="770c2-106">Defines a three-state check box control.</span></span> <span data-ttu-id="770c2-107">El control es idéntico a una [**casilla**](checkbox-control.md), excepto en que tiene tres Estados: checked, unchecked y Disabled (atenuado).</span><span class="sxs-lookup"><span data-stu-id="770c2-107">The control is identical to a [**CHECKBOX**](checkbox-control.md), except that it has three states: checked, unchecked, and disabled (grayed).</span></span>

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="770c2-108"><span id="text"></span><span id="TEXT"></span>*negrita*</span><span class="sxs-lookup"><span data-stu-id="770c2-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="770c2-109">Texto que se va a mostrar a la derecha del control.</span><span class="sxs-lookup"><span data-stu-id="770c2-109">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="770c2-110"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="770c2-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="770c2-111">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="770c2-111">Control styles.</span></span> <span data-ttu-id="770c2-112">Este valor puede ser una combinación del estilo de clase de botón **BS \_ 3STATE** y los estilos de **WS \_ TABSTOP** y de **\_ Grupo WS** .</span><span class="sxs-lookup"><span data-stu-id="770c2-112">This value can be a combination of the button class style **BS\_3STATE** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="770c2-113">Si no especifica un estilo, el estilo predeterminado es `BS_3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="770c2-113">If you do not specify a style, the default style is `BS_3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="770c2-114">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="770c2-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="770c2-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="770c2-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="770c2-116">**Autocheckbox**</span><span class="sxs-lookup"><span data-stu-id="770c2-116">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="770c2-117">Casillas</span><span class="sxs-lookup"><span data-stu-id="770c2-117">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="770c2-118">**CASILLA**</span><span class="sxs-lookup"><span data-stu-id="770c2-118">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="770c2-119">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="770c2-119">**CONTROL**</span></span>](control-control.md)
</dt> </dl>

 

 




