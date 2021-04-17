---
description: Si el bit de control ComboList se establece en un cuadro combinado, el campo de edición se reemplaza por un campo de texto estático. Esto evita que un usuario escriba un nuevo valor y requiere que el usuario elija solo uno de los valores predefinidos.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Atributo de control ComboList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668075"
---
# <a name="combolist-control-attribute"></a><span data-ttu-id="4cacb-104">Atributo de control ComboList</span><span class="sxs-lookup"><span data-stu-id="4cacb-104">ComboList Control Attribute</span></span>

<span data-ttu-id="4cacb-105">Si el bit de control ComboList se establece en un cuadro combinado, el campo de edición se reemplaza por un campo de texto estático.</span><span class="sxs-lookup"><span data-stu-id="4cacb-105">If the ComboList Control bit is set on a combo box, the edit field is replaced by a static text field.</span></span> <span data-ttu-id="4cacb-106">Esto evita que un usuario escriba un nuevo valor y requiere que el usuario elija solo uno de los valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="4cacb-106">This prevents a user from entering a new value and requires the user to choose only one of the predefined values.</span></span>

<span data-ttu-id="4cacb-107">Si no se establece este bit, el cuadro combinado tiene un campo de edición.</span><span class="sxs-lookup"><span data-stu-id="4cacb-107">If this bit is not set, the combo box has an edit field.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="4cacb-108">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="4cacb-108">Valid Controls</span></span>

[<span data-ttu-id="4cacb-109">ComboBox</span><span class="sxs-lookup"><span data-stu-id="4cacb-109">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="4cacb-110">Value</span><span class="sxs-lookup"><span data-stu-id="4cacb-110">Value</span></span>



| <span data-ttu-id="4cacb-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="4cacb-111">Decimal</span></span> | <span data-ttu-id="4cacb-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="4cacb-112">Hexadecimal</span></span> | <span data-ttu-id="4cacb-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cacb-113">Description</span></span>                     |
|---------|-------------|---------------------------------|
| <span data-ttu-id="4cacb-114">131 072</span><span class="sxs-lookup"><span data-stu-id="4cacb-114">131072</span></span>  | <span data-ttu-id="4cacb-115">0x00020000</span><span class="sxs-lookup"><span data-stu-id="4cacb-115">0x00020000</span></span>  | <span data-ttu-id="4cacb-116">msidbControlAttributesComboList</span><span class="sxs-lookup"><span data-stu-id="4cacb-116">msidbControlAttributesComboList</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4cacb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cacb-117">Remarks</span></span>

<span data-ttu-id="4cacb-118">Para establecer este atributo en un control, incluya el bit ComboList en la columna Attributes del registro del control en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="4cacb-118">To set this attribute on a control, include the ComboList bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="4cacb-119">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="4cacb-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



