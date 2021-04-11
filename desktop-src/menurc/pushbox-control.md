---
title: Control PUSHBOX
description: Define un control de cuadro de la tecla de control, que es idéntico a un botón de PULSAción, con la excepción de que no muestra una esfera o un fotograma; solo aparece el texto.
ms.assetid: b4e9d3f5-fcc4-40e1-90af-53d14e4638bf
keywords:
- Menús de control de PUSHBOX y otros recursos
topic_type:
- apiref
api_name:
- PUSHBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3e81e11c7d9a87c4f5501b114ef77cdb88b07
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148913"
---
# <a name="pushbox-control"></a><span data-ttu-id="f4659-104">Control PUSHBOX</span><span class="sxs-lookup"><span data-stu-id="f4659-104">PUSHBOX control</span></span>

<span data-ttu-id="f4659-105">Define un control de cuadro de la tecla de control, que es idéntico a un botón de [**pulsación**](pushbutton-control.md), con la excepción de que no muestra una esfera o un fotograma; solo aparece el texto.</span><span class="sxs-lookup"><span data-stu-id="f4659-105">Defines a push-box control, which is identical to a [**PUSHBUTTON**](pushbutton-control.md), except that it does not display a button face or frame; only the text appears.</span></span>

``` syntax
PUSHBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="f4659-106"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="f4659-106"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="f4659-107">Estilos de pushbox, que pueden ser una combinación del estilo **BS \_ pushbox** y los estilos siguientes: **WS \_ TABSTOP**, **WS \_ Disabled** y **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="f4659-107">Styles for the pushbox, which can be a combination of the **BS\_PUSHBOX** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="f4659-108">Si no especifica un estilo, el estilo predeterminado es `BS_PUSHBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="f4659-108">If you do not specify a style, the default style is `BS_PUSHBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="f4659-109">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f4659-109">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f4659-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4659-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4659-111">Botones de reenvío</span><span class="sxs-lookup"><span data-stu-id="f4659-111">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="f4659-112">**BOTONES**</span><span class="sxs-lookup"><span data-stu-id="f4659-112">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> </dl>

 

 




