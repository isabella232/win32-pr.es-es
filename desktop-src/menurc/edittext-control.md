---
title: EDITTEXT (control)
description: Define un control de edición que pertenece a la clase EDIT.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Menús de control EDITTEXT y otros recursos
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790558"
---
# <a name="edittext-control"></a><span data-ttu-id="35058-104">EDITTEXT (control)</span><span class="sxs-lookup"><span data-stu-id="35058-104">EDITTEXT control</span></span>

<span data-ttu-id="35058-105">Define un control de edición que pertenece a la clase EDIT.</span><span class="sxs-lookup"><span data-stu-id="35058-105">Defines an edit control belonging to the EDIT class.</span></span> <span data-ttu-id="35058-106">Crea una región rectangular en la que el usuario puede escribir y editar texto.</span><span class="sxs-lookup"><span data-stu-id="35058-106">It creates a rectangular region in which the user can type and edit text.</span></span> <span data-ttu-id="35058-107">El control muestra un cursor cuando el usuario hace clic en él.</span><span class="sxs-lookup"><span data-stu-id="35058-107">The control displays a cursor when the user clicks the mouse in it.</span></span> <span data-ttu-id="35058-108">El usuario puede usar el teclado para escribir texto o editar el texto existente.</span><span class="sxs-lookup"><span data-stu-id="35058-108">The user can then use the keyboard to enter text or edit the existing text.</span></span> <span data-ttu-id="35058-109">La edición de claves incluye las teclas retroceso y eliminar.</span><span class="sxs-lookup"><span data-stu-id="35058-109">Editing keys include the BACKSPACE and DELETE keys.</span></span> <span data-ttu-id="35058-110">El usuario también puede usar el mouse para seleccionar los caracteres que se van a eliminar o seleccionar el lugar donde se van a insertar nuevos caracteres.</span><span class="sxs-lookup"><span data-stu-id="35058-110">The user can also use the mouse to select characters to be deleted or to select the place to insert new characters.</span></span>

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="35058-111"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="35058-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="35058-112">Estilos de control.</span><span class="sxs-lookup"><span data-stu-id="35058-112">Control styles.</span></span> <span data-ttu-id="35058-113">Este valor puede ser una combinación de los estilos de clase de edición y los siguientes estilos: **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL**, **WS \_ HSCROLL** y **WS \_ deshabilitados**.</span><span class="sxs-lookup"><span data-stu-id="35058-113">This value can be a combination of the edit class styles and the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, **WS\_HSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="35058-114">Si no especifica un estilo, el estilo predeterminado es `ES_LEFT | WS_BORDER | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="35058-114">If you do not specify a style, the default style is `ES_LEFT | WS_BORDER | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="35058-115">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="35058-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="35058-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="35058-116">Examples</span></span>

<span data-ttu-id="35058-117">En el ejemplo siguiente se muestra el uso de la instrucción **EDITTEXT** :</span><span class="sxs-lookup"><span data-stu-id="35058-117">The following example demonstrates the use of the **EDITTEXT** statement:</span></span>

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="35058-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="35058-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35058-119">Controles de edición</span><span class="sxs-lookup"><span data-stu-id="35058-119">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> </dl>

 

 