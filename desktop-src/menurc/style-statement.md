---
title: STYLE (instrucción)
description: Define el estilo de ventana del cuadro de diálogo. El estilo de ventana especifica si el cuadro es una ventana emergente o secundaria.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Menús de instrucciones de estilo y otros recursos
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420653"
---
# <a name="style-statement"></a><span data-ttu-id="12675-105">STYLE (instrucción)</span><span class="sxs-lookup"><span data-stu-id="12675-105">STYLE statement</span></span>

<span data-ttu-id="12675-106">Define el estilo de ventana del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="12675-106">Defines the window style of the dialog box.</span></span> <span data-ttu-id="12675-107">El estilo de ventana especifica si el cuadro es una ventana emergente o secundaria.</span><span class="sxs-lookup"><span data-stu-id="12675-107">The window style specifies whether the box is a pop-up or a child window.</span></span>

``` syntax
STYLE style
```

<dl> <dt>

<span data-ttu-id="12675-108"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="12675-108"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="12675-109">Nombre del estilo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="12675-109">The window style.</span></span> <span data-ttu-id="12675-110">Este parámetro puede ser un valor entero o una combinación de valores de estilo de ventana (como **WS \_ Caption** y **WS \_ SYSMENU**) y valores de estilo de cuadro de diálogo (como el **\_ centro de DS**).</span><span class="sxs-lookup"><span data-stu-id="12675-110">This parameter can be an integer value or a combination of window style values (such as **WS\_CAPTION** and **WS\_SYSMENU**) and dialog box style values (such as **DS\_CENTER**).</span></span>

</dd> </dl>

<span data-ttu-id="12675-111">Para obtener una lista de estilos de ventana, vea [estilos de ventana](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="12675-111">For a list of window styles, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span> <span data-ttu-id="12675-112">Para obtener una lista de estilos de cuadro de diálogo, vea [estilos de plantilla de cuadro de diálogo](../dlgbox/about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="12675-112">For a list of dialog box styles, see [Dialog Box Template Styles](../dlgbox/about-dialog-boxes.md).</span></span> <span data-ttu-id="12675-113">Si utiliza los valores de estilo de ventana o de cuadro de diálogo, debe incluir Windows. h.</span><span class="sxs-lookup"><span data-stu-id="12675-113">If you use the window or dialog box style values, you must include Windows.h.</span></span>

 

 