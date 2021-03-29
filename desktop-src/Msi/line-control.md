---
description: El control de línea es una línea horizontal.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Line (control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba3b7374574e2a0087e7dae8d0ffa9f097be9f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812865"
---
# <a name="line-control"></a><span data-ttu-id="83443-103">Line (control)</span><span class="sxs-lookup"><span data-stu-id="83443-103">Line Control</span></span>

<span data-ttu-id="83443-104">El control de línea es una línea horizontal.</span><span class="sxs-lookup"><span data-stu-id="83443-104">The Line control is a horizontal line.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="83443-105">Atributos de control</span><span class="sxs-lookup"><span data-stu-id="83443-105">Control Attributes</span></span>

<span data-ttu-id="83443-106">Puede usar los siguientes atributos con este control.</span><span class="sxs-lookup"><span data-stu-id="83443-106">You can use the following attributes with this control.</span></span> <span data-ttu-id="83443-107">Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos.</span><span class="sxs-lookup"><span data-stu-id="83443-107">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="83443-108">Escriba el identificador de ControlEvent, en la columna evento.</span><span class="sxs-lookup"><span data-stu-id="83443-108">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="83443-109">Identificador de atributo</span><span class="sxs-lookup"><span data-stu-id="83443-109">Attribute identifier</span></span>                       | <span data-ttu-id="83443-110">Bit hexadecimal</span><span class="sxs-lookup"><span data-stu-id="83443-110">Hexadecimal bit</span></span>                  | <span data-ttu-id="83443-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="83443-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83443-112">Position</span><span class="sxs-lookup"><span data-stu-id="83443-112">Position</span></span>](position-control-attribute.md) |                                  | <span data-ttu-id="83443-113">Posición del control en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="83443-113">Position of the control in the dialog box.</span></span> <span data-ttu-id="83443-114">Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="83443-114">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="83443-115">Use [unidades de instalador](installer-units.md) para longitud y distancia.</span><span class="sxs-lookup"><span data-stu-id="83443-115">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                         |
| [<span data-ttu-id="83443-116">Visible</span><span class="sxs-lookup"><span data-stu-id="83443-116">Visible</span></span>](visible-control-attribute.md)   | <span data-ttu-id="83443-117">0x00000000 0x00000001</span><span class="sxs-lookup"><span data-stu-id="83443-117">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="83443-118">Control oculto.</span><span class="sxs-lookup"><span data-stu-id="83443-118">Hidden control.</span></span> <span data-ttu-id="83443-119">Control visible.</span><span class="sxs-lookup"><span data-stu-id="83443-119">Visible control.</span></span><br/> <span data-ttu-id="83443-120">Incluya este bit en la palabra de bits de la columna Attributes de la tabla de [control](control-table.md) o la [tabla BBControl](bbcontrol-table.md) para que el control esté visible u oculto en su creación.</span><span class="sxs-lookup"><span data-stu-id="83443-120">Include this bit in the bit word of the Attributes column in the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="83443-121">También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).</span><span class="sxs-lookup"><span data-stu-id="83443-121">You can also hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="83443-122">Sunken</span><span class="sxs-lookup"><span data-stu-id="83443-122">Sunken</span></span>](sunken-control-attribute.md)     | <span data-ttu-id="83443-123">0x00000000 0x00000004</span><span class="sxs-lookup"><span data-stu-id="83443-123">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="83443-124">Muestra el estilo visual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="83443-124">Displays the default visual style.</span></span> <span data-ttu-id="83443-125">Muestra el control con una apariencia en relieve y 3D.</span><span class="sxs-lookup"><span data-stu-id="83443-125">Displays the control with a sunken, 3-D look.</span></span><br/> <span data-ttu-id="83443-126">Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="83443-126">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="83443-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83443-127">Remarks</span></span>

<span data-ttu-id="83443-128">Este control se puede crear a partir de la clase estática mediante la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="83443-128">This control can be created from the STATIC class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="83443-129">Tiene los estilos **SS \_ ETCHEDHORZ** y **SS \_ SUNKEN** .</span><span class="sxs-lookup"><span data-stu-id="83443-129">It has the **SS\_ETCHEDHORZ** and **SS\_SUNKEN** styles.</span></span>

 

 
