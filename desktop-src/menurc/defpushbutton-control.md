---
title: Control DEFPUSHBUTTON
description: Define un control de botón de complemento predeterminado.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Menús de control de DEFPUSHBUTTON y otros recursos
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676333"
---
# <a name="defpushbutton-control"></a><span data-ttu-id="2f9ab-104">Control DEFPUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="2f9ab-104">DEFPUSHBUTTON control</span></span>

<span data-ttu-id="2f9ab-105">Define un control de botón de complemento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2f9ab-105">Defines a default push-button control.</span></span> <span data-ttu-id="2f9ab-106">El control es un pequeño rectángulo con un contorno en negrita que representa la respuesta predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="2f9ab-106">The control is a small rectangle with a bold outline that represents the default response for the user.</span></span> <span data-ttu-id="2f9ab-107">El texto especificado se muestra dentro del botón.</span><span class="sxs-lookup"><span data-stu-id="2f9ab-107">The given text is displayed inside the button.</span></span> <span data-ttu-id="2f9ab-108">El control resalta el botón de la manera habitual cuando el usuario hace clic con el mouse en él y envía un mensaje a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="2f9ab-108">The control highlights the button in the usual way when the user clicks the mouse in it and sends a message to its parent window.</span></span>

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="2f9ab-109"><span id="text"></span><span id="TEXT"></span>*negrita*</span><span class="sxs-lookup"><span data-stu-id="2f9ab-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="2f9ab-110">Texto que se va a centrar en el área rectangular del control.</span><span class="sxs-lookup"><span data-stu-id="2f9ab-110">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2f9ab-111"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="2f9ab-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="2f9ab-112">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="2f9ab-112">Control styles.</span></span> <span data-ttu-id="2f9ab-113">Este valor puede ser una combinación de los siguientes estilos: **BS \_ DEFPUSHBUTTON**, **WS \_ TABSTOP**, **WS \_ Group** y **WS \_ deshabilitados**.</span><span class="sxs-lookup"><span data-stu-id="2f9ab-113">This value can be a combination of the following styles: **BS\_DEFPUSHBUTTON**, **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="2f9ab-114">Si no especifica un estilo, el estilo predeterminado es `BS_DEFPUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="2f9ab-114">If you do not specify a style, the default style is `BS_DEFPUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="2f9ab-115">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2f9ab-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2f9ab-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2f9ab-116">Examples</span></span>

<span data-ttu-id="2f9ab-117">En este ejemplo se define un control de botón de opción predeterminado con la etiqueta cancelar:</span><span class="sxs-lookup"><span data-stu-id="2f9ab-117">This example defines a default push-button control that is labeled Cancel:</span></span>

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a><span data-ttu-id="2f9ab-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f9ab-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f9ab-119">Botones de reenvío</span><span class="sxs-lookup"><span data-stu-id="2f9ab-119">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="2f9ab-120">**BOTONES**</span><span class="sxs-lookup"><span data-stu-id="2f9ab-120">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> <dt>

[<span data-ttu-id="2f9ab-121">**ÍNDICES**</span><span class="sxs-lookup"><span data-stu-id="2f9ab-121">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




