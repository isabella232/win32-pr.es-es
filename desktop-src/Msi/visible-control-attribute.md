---
description: Si se establece el bit de control visible, el control está visible en el cuadro de diálogo. Si no se establece este bit, el control se oculta en el cuadro de diálogo. Un evento de control puede cambiar posteriormente el estado oculto o visible del atributo de control visible.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Atributo de control visible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677351"
---
# <a name="visible-control-attribute"></a><span data-ttu-id="f6fc8-105">Atributo de control visible</span><span class="sxs-lookup"><span data-stu-id="f6fc8-105">Visible Control Attribute</span></span>

<span data-ttu-id="f6fc8-106">Si se establece el bit de control visible, el control está visible en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-106">If the Visible Control bit is set, the control is visible on the dialog box.</span></span> <span data-ttu-id="f6fc8-107">Si no se establece este bit, el control se oculta en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-107">If this bit is not set, the control is hidden on the dialog box.</span></span> <span data-ttu-id="f6fc8-108">Un [evento de control](control-events.md)puede cambiar posteriormente el estado oculto o visible del atributo de control visible.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-108">The visible or hidden state of the Visible control attribute can be later changed by a [Control Event](control-events.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="f6fc8-109">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="f6fc8-109">Valid Controls</span></span>

<span data-ttu-id="f6fc8-110">Todos los controles.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="f6fc8-111">Value</span><span class="sxs-lookup"><span data-stu-id="f6fc8-111">Value</span></span>



| <span data-ttu-id="f6fc8-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="f6fc8-112">Decimal</span></span> | <span data-ttu-id="f6fc8-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="f6fc8-113">Hexadecimal</span></span> | <span data-ttu-id="f6fc8-114">Constante</span><span class="sxs-lookup"><span data-stu-id="f6fc8-114">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="f6fc8-115">1</span><span class="sxs-lookup"><span data-stu-id="f6fc8-115">1</span></span>       | <span data-ttu-id="f6fc8-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f6fc8-116">0x00000001</span></span>  | <span data-ttu-id="f6fc8-117">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="f6fc8-117">**msidbControlAttributesVisible**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f6fc8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6fc8-118">Remarks</span></span>

<span data-ttu-id="f6fc8-119">Puede usar la [tabla ControlCondition](controlcondition-table.md) para mostrar u ocultar un control según el valor de una propiedad o una instrucción condicional.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-119">You can use the [ControlCondition table](controlcondition-table.md) to show or hide a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="f6fc8-120">También puede mostrar u ocultar un control si suscribe el control a un [ControlEvent,](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="f6fc8-120">You can also show or hide a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="f6fc8-121">Escriba el identificador del atributo en la columna atributo y el identificador del evento en la columna evento de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6fc8-121">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="f6fc8-122">Vea [controles y](controls.md) [atributos de control](control-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="f6fc8-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



