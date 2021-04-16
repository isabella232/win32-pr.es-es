---
description: Este atributo especifica si el control especificado está habilitado o deshabilitado. La mayoría de los controles aparecen atenuados al deshabilitarlos.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Atributo de control habilitado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652532"
---
# <a name="enabled-control-attribute"></a><span data-ttu-id="b3121-104">Atributo de control habilitado</span><span class="sxs-lookup"><span data-stu-id="b3121-104">Enabled Control Attribute</span></span>

<span data-ttu-id="b3121-105">Este atributo especifica si el control especificado está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b3121-105">This attribute specifies if the given control is enabled or disabled.</span></span> <span data-ttu-id="b3121-106">La mayoría de los controles aparecen atenuados al deshabilitarlos.</span><span class="sxs-lookup"><span data-stu-id="b3121-106">Most controls appear gray when disabled.</span></span>

<span data-ttu-id="b3121-107">Si se establece este bit, el control se crea como habilitado.</span><span class="sxs-lookup"><span data-stu-id="b3121-107">If this bit is set, the control is created as enabled.</span></span>

<span data-ttu-id="b3121-108">Si no se establece este bit, el control se crea como deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b3121-108">If this bit is not set, the control is created as disabled.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="b3121-109">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="b3121-109">Valid Controls</span></span>

<span data-ttu-id="b3121-110">Todos los controles.</span><span class="sxs-lookup"><span data-stu-id="b3121-110">All controls.</span></span> <span data-ttu-id="b3121-111">La apariencia de algunos controles que no están asociados a una propiedad, como mapas de bits e iconos, no se ve afectada por el establecimiento de este atributo.</span><span class="sxs-lookup"><span data-stu-id="b3121-111">The appearance of some controls that are not associated with a property, such as Bitmaps and Icons, are unaffected by setting this attribute.</span></span>

## <a name="value"></a><span data-ttu-id="b3121-112">Value</span><span class="sxs-lookup"><span data-stu-id="b3121-112">Value</span></span>



| <span data-ttu-id="b3121-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="b3121-113">Decimal</span></span> | <span data-ttu-id="b3121-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="b3121-114">Hexadecimal</span></span> | <span data-ttu-id="b3121-115">Constante</span><span class="sxs-lookup"><span data-stu-id="b3121-115">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="b3121-116">2</span><span class="sxs-lookup"><span data-stu-id="b3121-116">2</span></span>       | <span data-ttu-id="b3121-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b3121-117">0x00000002</span></span>  | <span data-ttu-id="b3121-118">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="b3121-118">**msidbControlAttributesEnabled**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b3121-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3121-119">Remarks</span></span>

<span data-ttu-id="b3121-120">También puede usar la [tabla ControlCondition](controlcondition-table.md) para deshabilitar o habilitar un control según el valor de una propiedad o una instrucción condicional.</span><span class="sxs-lookup"><span data-stu-id="b3121-120">You can also use the [ControlCondition table](controlcondition-table.md) to disable or enable a control according to the value of a property or conditional statement.</span></span>

<span data-ttu-id="b3121-121">También puede habilitar o deshabilitar un control si suscribe el control a un [ControlEvent,](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="b3121-121">You can also enable or disable a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="b3121-122">Escriba el identificador del atributo en la columna atributo y el identificador del evento en la columna evento de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b3121-122">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="b3121-123">Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="b3121-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



