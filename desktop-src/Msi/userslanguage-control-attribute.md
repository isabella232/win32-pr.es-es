---
description: Si se establece esta marca de bits, las fuentes se crean mediante la página de códigos predeterminada de la interfaz de usuario del usuario. Si no se establece la marca de bits, las fuentes se crean mediante la página de códigos de la base de datos.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Atributo de control UsersLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677687"
---
# <a name="userslanguage-control-attribute"></a><span data-ttu-id="1632b-104">Atributo de control UsersLanguage</span><span class="sxs-lookup"><span data-stu-id="1632b-104">UsersLanguage Control Attribute</span></span>

<span data-ttu-id="1632b-105">Si se establece esta marca de bits, las fuentes se crean mediante la página de códigos predeterminada de la interfaz de usuario del usuario.</span><span class="sxs-lookup"><span data-stu-id="1632b-105">If this bit flag is set, fonts are created using the user's default UI code page.</span></span> <span data-ttu-id="1632b-106">Si no se establece la marca de bits, las fuentes se crean mediante la página de códigos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1632b-106">If the bit flag is not set, fonts are created using the database code page.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="1632b-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="1632b-107">Valid Controls</span></span>

[<span data-ttu-id="1632b-108">Texto</span><span class="sxs-lookup"><span data-stu-id="1632b-108">Text</span></span>](text-control.md)

 

[<span data-ttu-id="1632b-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="1632b-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="1632b-110">ComboBox</span><span class="sxs-lookup"><span data-stu-id="1632b-110">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="1632b-111">Value</span><span class="sxs-lookup"><span data-stu-id="1632b-111">Value</span></span>



| <span data-ttu-id="1632b-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="1632b-112">Decimal</span></span> | <span data-ttu-id="1632b-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1632b-113">Hexadecimal</span></span> | <span data-ttu-id="1632b-114">Constante</span><span class="sxs-lookup"><span data-stu-id="1632b-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="1632b-115">1 048 576</span><span class="sxs-lookup"><span data-stu-id="1632b-115">1048576</span></span> | <span data-ttu-id="1632b-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="1632b-116">0x00100000</span></span>  | <span data-ttu-id="1632b-117">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="1632b-117">**msidbControlAttributesUsersLanguage**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1632b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1632b-118">Remarks</span></span>

<span data-ttu-id="1632b-119">Este atributo de control se puede usar para mostrar el texto que el usuario ha escrito en un control [Edit](edit-control.md) o [PathEdit](pathedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="1632b-119">This control attribute can be used to display text that the user has entered into an [Edit](edit-control.md) or [PathEdit](pathedit-control.md) control.</span></span>

<span data-ttu-id="1632b-120">El control Edit, control PathEdit, control [DirectoryList](directorylist-control.md) y [DirectoryCombo](directorycombo-control.md) siempre usan las fuentes creadas en la página de códigos de la interfaz de usuario predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="1632b-120">The Edit control, PathEdit control, [DirectoryList control](directorylist-control.md) and [DirectoryCombo control](directorycombo-control.md) always use the fonts created in the user's default UI code page.</span></span> <span data-ttu-id="1632b-121">Esto puede producir problemas si se han instalado idiomas adicionales en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1632b-121">This can cause problems if additional languages have been installed on the operating system.</span></span> <span data-ttu-id="1632b-122">En este caso, es posible que las fuentes del equipo no representen todos los caracteres de los idiomas agregados.</span><span class="sxs-lookup"><span data-stu-id="1632b-122">In this case, the fonts on the computer may not be able to represent all the characters in the added languages.</span></span> <span data-ttu-id="1632b-123">Para determinar qué fuentes se pueden usar, busca los valores en **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ FontLink \\ SystemLink**.</span><span class="sxs-lookup"><span data-stu-id="1632b-123">To determine what fonts can be used, look up the values in **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\FontLink\\SystemLink**.</span></span>

<span data-ttu-id="1632b-124">Para obtener más información, vea [controles](controls.md)y [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="1632b-124">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



