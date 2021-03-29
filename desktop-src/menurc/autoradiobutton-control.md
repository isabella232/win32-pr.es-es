---
title: Control autoradiobutton
description: Define un control de botón de radio automático. Este control realiza automáticamente la exclusión mutua con los demás controles autoradiobutton del mismo grupo. Cuando se elige el botón, se notifica a la aplicación con el BN en el que se \_ hace clic.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menús de control autoradiobutton y otros recursos
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783887"
---
# <a name="autoradiobutton-control"></a><span data-ttu-id="3591e-106">Control autoradiobutton</span><span class="sxs-lookup"><span data-stu-id="3591e-106">AUTORADIOBUTTON control</span></span>

<span data-ttu-id="3591e-107">Define un control de botón de radio automático.</span><span class="sxs-lookup"><span data-stu-id="3591e-107">Defines an automatic radio button control.</span></span> <span data-ttu-id="3591e-108">Este control realiza automáticamente la exclusión mutua con los demás controles **AUTOradiobutton** del mismo grupo.</span><span class="sxs-lookup"><span data-stu-id="3591e-108">This control automatically performs mutual exclusion with the other **AUTORADIOBUTTON** controls in the same group.</span></span> <span data-ttu-id="3591e-109">Cuando se elige el botón, se notifica a la aplicación con el BN en el que se **\_ hace clic**.</span><span class="sxs-lookup"><span data-stu-id="3591e-109">When the button is chosen, the application is notified with **BN\_CLICKED**.</span></span>

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="3591e-110"><span id="text"></span><span id="TEXT"></span>*negrita*</span><span class="sxs-lookup"><span data-stu-id="3591e-110"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="3591e-111">Texto que aparecerá junto al botón de radio.</span><span class="sxs-lookup"><span data-stu-id="3591e-111">Text that will appear next to the radio button.</span></span>

</dd> <dt>

<span data-ttu-id="3591e-112"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="3591e-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="3591e-113">Estilos para el botón de radio automático, que puede ser una combinación de estilos de clase de botón y los estilos siguientes: **WS \_ TABSTOP**, **WS \_ Disabled** y **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="3591e-113">Styles for the automatic radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="3591e-114">Si no especifica un estilo, el estilo predeterminado es `BS_AUTORADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="3591e-114">If you do not specify a style, the default style is `BS_AUTORADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="3591e-115">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3591e-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3591e-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="3591e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3591e-117">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="3591e-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="3591e-118">Botones de radio</span><span class="sxs-lookup"><span data-stu-id="3591e-118">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[<span data-ttu-id="3591e-119">**ÍNDICES**</span><span class="sxs-lookup"><span data-stu-id="3591e-119">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




