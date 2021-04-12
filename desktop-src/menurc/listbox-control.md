---
title: LISTBOX (control) (menús y otros recursos)
description: Define controles de uso frecuente para un cuadro de diálogo o una ventana. El control es un rectángulo que contiene una lista de cadenas (como nombres de archivo) desde las que el usuario puede seleccionar.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menús de control LISTBOX y otros recursos
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149257"
---
# <a name="listbox-control"></a><span data-ttu-id="05d8f-105">LISTBOX (control)</span><span class="sxs-lookup"><span data-stu-id="05d8f-105">LISTBOX control</span></span>

<span data-ttu-id="05d8f-106">Define controles de uso frecuente para un cuadro de diálogo o una ventana.</span><span class="sxs-lookup"><span data-stu-id="05d8f-106">Defines commonly used controls for a dialog box or window.</span></span> <span data-ttu-id="05d8f-107">El control es un rectángulo que contiene una lista de cadenas (como nombres de archivo) desde las que el usuario puede seleccionar.</span><span class="sxs-lookup"><span data-stu-id="05d8f-107">The control is a rectangle containing a list of strings (such as filenames) from which the user can select.</span></span>

<span data-ttu-id="05d8f-108">La instrucción **ListBox** , que solo se puede utilizar en una instrucción [**DIALOGEX**](dialogex-resource.md) o **Window** , define el identificador, las dimensiones y los atributos de una ventana de control.</span><span class="sxs-lookup"><span data-stu-id="05d8f-108">The **LISTBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) or **WINDOW** statement, defines the identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="05d8f-109"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="05d8f-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="05d8f-110">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="05d8f-110">Control styles.</span></span> <span data-ttu-id="05d8f-111">Este valor puede ser una combinación de los estilos de clase de cuadro de lista y cualquiera de los siguientes estilos: **WS \_ Border** y **WS \_ VSCROLL**.</span><span class="sxs-lookup"><span data-stu-id="05d8f-111">This value can be a combination of the list-box class styles and any of the following styles: **WS\_BORDER** and **WS\_VSCROLL**.</span></span>

<span data-ttu-id="05d8f-112">Si no especifica un estilo, el estilo predeterminado es `LBS_NOTIFY | WS_BORDER` .</span><span class="sxs-lookup"><span data-stu-id="05d8f-112">If you do not specify a style, the default style is `LBS_NOTIFY | WS_BORDER`.</span></span>

</dd> </dl>

<span data-ttu-id="05d8f-113">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="05d8f-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="05d8f-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="05d8f-114">Examples</span></span>

<span data-ttu-id="05d8f-115">En este ejemplo se define un control de cuadro de lista cuyo identificador es 101:</span><span class="sxs-lookup"><span data-stu-id="05d8f-115">This example defines a list-box control whose identifier is 101:</span></span>

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="05d8f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="05d8f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d8f-117">**COMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="05d8f-117">**COMBOBOX**</span></span>](combobox-control.md)
</dt> <dt>

[<span data-ttu-id="05d8f-118">Cuadros de lista</span><span class="sxs-lookup"><span data-stu-id="05d8f-118">List Boxes</span></span>](../controls/about-list-boxes.md)
</dt> </dl>

 

 