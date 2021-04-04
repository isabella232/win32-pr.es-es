---
description: El control de la cartelera muestra los controles que se usan con frecuencia y que se agregan y se quitan del cuadro de diálogo ControlEvents.
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: Control de cartelera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e056a764ec4a71c3ce6785acf331b4bc1ff95ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909066"
---
# <a name="billboard-control"></a><span data-ttu-id="41c00-103">Control de cartelera</span><span class="sxs-lookup"><span data-stu-id="41c00-103">Billboard Control</span></span>

<span data-ttu-id="41c00-104">El control de la cartelera muestra los controles que se usan con frecuencia y que se agregan y se quitan del cuadro de diálogo ControlEvents.</span><span class="sxs-lookup"><span data-stu-id="41c00-104">The Billboard control displays commonly used controls that are added and removed from the dialog box by ControlEvents.</span></span> <span data-ttu-id="41c00-105">Solo los controles que no están asociados a una propiedad, como [texto](text-control.md), [mapa de bits](bitmap-control.md), [icono](icon-control.md)o controles personalizados, se pueden colocar en una cartelera.</span><span class="sxs-lookup"><span data-stu-id="41c00-105">Only controls that are not associated with a property, such as [Text](text-control.md), [Bitmap](bitmap-control.md), or [Icon](icon-control.md), or custom controls can be placed on a billboard.</span></span> <span data-ttu-id="41c00-106">Los controles de la cartelera suelen mostrar mensajes de progreso.</span><span class="sxs-lookup"><span data-stu-id="41c00-106">Billboard controls most typically display progress messages.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="41c00-107">Atributos de control</span><span class="sxs-lookup"><span data-stu-id="41c00-107">Control Attributes</span></span>

<span data-ttu-id="41c00-108">Puede usar los siguientes atributos con el control de la cartelera.</span><span class="sxs-lookup"><span data-stu-id="41c00-108">You can use the following attributes with the Billboard control.</span></span> <span data-ttu-id="41c00-109">Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos.</span><span class="sxs-lookup"><span data-stu-id="41c00-109">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="41c00-110">Escriba el identificador de ControlEvent, en la columna evento.</span><span class="sxs-lookup"><span data-stu-id="41c00-110">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="41c00-111">Identificador de atributo</span><span class="sxs-lookup"><span data-stu-id="41c00-111">Attribute identifier</span></span>                                 | <span data-ttu-id="41c00-112">Bit hexadecimal</span><span class="sxs-lookup"><span data-stu-id="41c00-112">Hexadecimal bit</span></span>                  | <span data-ttu-id="41c00-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="41c00-113">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41c00-114">BillboardName</span><span class="sxs-lookup"><span data-stu-id="41c00-114">BillboardName</span></span>](billboardname-control-attribute.md) |                                  | <span data-ttu-id="41c00-115">Nombre de la cartelera actual.</span><span class="sxs-lookup"><span data-stu-id="41c00-115">Name of the current billboard.</span></span> <span data-ttu-id="41c00-116">Escriba el identificador de la cartelera en la columna cartelera de la [tabla BBControl](bbcontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="41c00-116">Enter the billboard's identifier in the Billboard column of the [BBControl table](bbcontrol-table.md).</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="41c00-117">Position</span><span class="sxs-lookup"><span data-stu-id="41c00-117">Position</span></span>](position-control-attribute.md)           |                                  | <span data-ttu-id="41c00-118">Posición del control en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="41c00-118">Position of control in the dialog box.</span></span> <span data-ttu-id="41c00-119">Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la [tabla BBControl](bbcontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="41c00-119">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="41c00-120">Use [unidades de instalador](installer-units.md) para longitud y distancia.</span><span class="sxs-lookup"><span data-stu-id="41c00-120">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                |
| [<span data-ttu-id="41c00-121">Visible</span><span class="sxs-lookup"><span data-stu-id="41c00-121">Visible</span></span>](visible-control-attribute.md)             | <span data-ttu-id="41c00-122">0x00000000 0x00000001</span><span class="sxs-lookup"><span data-stu-id="41c00-122">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="41c00-123">Control oculto.</span><span class="sxs-lookup"><span data-stu-id="41c00-123">Hidden control.</span></span> <span data-ttu-id="41c00-124">Control visible.</span><span class="sxs-lookup"><span data-stu-id="41c00-124">Visible control.</span></span><br/> <span data-ttu-id="41c00-125">Incluya este bit en la palabra de bit de la columna Attributes de la [tabla BBControl](bbcontrol-table.md) para que el control esté visible u oculto en su creación.</span><span class="sxs-lookup"><span data-stu-id="41c00-125">Include this bit in the bit word of the Attributes column in the [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="41c00-126">Ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).</span><span class="sxs-lookup"><span data-stu-id="41c00-126">Hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="41c00-127">Sunken</span><span class="sxs-lookup"><span data-stu-id="41c00-127">Sunken</span></span>](sunken-control-attribute.md)               | <span data-ttu-id="41c00-128">0x00000000 0x00000004</span><span class="sxs-lookup"><span data-stu-id="41c00-128">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="41c00-129">Muestra el estilo visual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="41c00-129">Displays the default visual style.</span></span> <span data-ttu-id="41c00-130">Muestra el control con un aspecto hundido, 3D.</span><span class="sxs-lookup"><span data-stu-id="41c00-130">Displays the control with a sunken, 3-D, look.</span></span><br/> <span data-ttu-id="41c00-131">Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="41c00-131">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="41c00-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41c00-132">Remarks</span></span>

<span data-ttu-id="41c00-133">Este control no tiene ninguna ventana propia.</span><span class="sxs-lookup"><span data-stu-id="41c00-133">This control has no window of its own.</span></span>

<span data-ttu-id="41c00-134">Los controles de la cartelera que aparecen en la interfaz de usuario completa se enumeran en la tabla de la [cartelera](billboard-table.md).</span><span class="sxs-lookup"><span data-stu-id="41c00-134">Billboard controls that appear in the full user interface are listed in the [Billboard table](billboard-table.md).</span></span>

<span data-ttu-id="41c00-135">Los controles que se encuentran en una cartelera deben aparecer en la [tabla BBControl](bbcontrol-table.md) en lugar de en la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="41c00-135">Controls that are located on a billboard must be listed in the [BBControl table](bbcontrol-table.md) rather than the [Control table](control-table.md).</span></span>

 

 




