---
description: En la tabla siguiente se enumeran los GUID de propiedades de paquete utilizados por la estructura de propiedades de paquetes \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID de PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913546"
---
# <a name="packetproperty-guids"></a><span data-ttu-id="8e09a-103">GUID de PacketProperty</span><span class="sxs-lookup"><span data-stu-id="8e09a-103">PacketProperty GUIDs</span></span>

<span data-ttu-id="8e09a-104">En la tabla siguiente se enumeran los GUID de propiedades de paquete utilizados por la estructura de [**\_ propiedades de paquetes**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .</span><span class="sxs-lookup"><span data-stu-id="8e09a-104">The following table lists packet property GUIDs used by the [**PACKET\_PROPERTY**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e09a-105">GUID</span><span class="sxs-lookup"><span data-stu-id="8e09a-105">GUID</span></span></th>
<th><span data-ttu-id="8e09a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e09a-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e09a-107">GUID_ALTITUDE_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="8e09a-107">GUID_ALTITUDE_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="8e09a-108">Ángulo entre el eje del lápiz y la superficie de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8e09a-108">Angle between the axis of the pen and the surface of the tablet.</span></span> <span data-ttu-id="8e09a-109">El valor es 0 cuando el lápiz es paralelo a la superficie y 90 cuando el lápiz es perpendicular a la superficie.</span><span class="sxs-lookup"><span data-stu-id="8e09a-109">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span> <span data-ttu-id="8e09a-110">Los valores son negativos cuando se invierte el lápiz.</span><span class="sxs-lookup"><span data-stu-id="8e09a-110">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e09a-111">GUID_AZIMUTH_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="8e09a-111">GUID_AZIMUTH_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="8e09a-112">Rotación en el sentido de las agujas del reloj del cursor alrededor del eje z a través de un intervalo circular completo.</span><span class="sxs-lookup"><span data-stu-id="8e09a-112">Clockwise rotation of the cursor around the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e09a-113">GUID_BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="8e09a-113">GUID_BOXNUMBER</span></span><br/></td>
<td><span data-ttu-id="8e09a-114">GUID que se usa para recuperar el número de cuadro de una alternativa de reconocimiento de tinta cuando el reconocedor está funcionando en modo de cuadro.</span><span class="sxs-lookup"><span data-stu-id="8e09a-114">The GUID that is used to retrieve the box number for an ink recognition alternate when the recognizer is operating in box mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e09a-115">GUID_BUTTON_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="8e09a-115">GUID_BUTTON_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="8e09a-116">Presión sobre un botón sensible a la presión.</span><span class="sxs-lookup"><span data-stu-id="8e09a-116">Pressure on a pressure-sensitive button.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e09a-117">GUID_NORMAL_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="8e09a-117">GUID_NORMAL_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="8e09a-118">El GUID para el objeto PacketProperty que representa la presión de la punta del lápiz perpendicular a la superficie de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8e09a-118">The GUID for the PacketProperty object that represents pressure of the pen tip perpendicular to the tablet surface.</span></span> <span data-ttu-id="8e09a-119">Cuanto mayor sea la presión de la punta del lápiz, más tinta se dibujará.</span><span class="sxs-lookup"><span data-stu-id="8e09a-119">The greater the pressure put on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e09a-120">GUID_PACKET_STATUS</span><span class="sxs-lookup"><span data-stu-id="8e09a-120">GUID_PACKET_STATUS</span></span><br/></td>
<td><span data-ttu-id="8e09a-121">Contiene uno o varios de los siguientes valores de marca:</span><span class="sxs-lookup"><span data-stu-id="8e09a-121">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="8e09a-122">El cursor toca la superficie de dibujo (valor = 1).</span><span class="sxs-lookup"><span data-stu-id="8e09a-122">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="8e09a-123">El cursor se invierte.</span><span class="sxs-lookup"><span data-stu-id="8e09a-123">The cursor is inverted.</span></span> <span data-ttu-id="8e09a-124">Por ejemplo, el extremo del borrador del lápiz apunta hacia la superficie (valor = 2).</span><span class="sxs-lookup"><span data-stu-id="8e09a-124">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="8e09a-125">No se usa (valor = 4).</span><span class="sxs-lookup"><span data-stu-id="8e09a-125">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="8e09a-126">Se presiona el botón de barril (valor = 8).</span><span class="sxs-lookup"><span data-stu-id="8e09a-126">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e09a-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span><span class="sxs-lookup"><span data-stu-id="8e09a-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span></span><br/></td>
<td><span data-ttu-id="8e09a-128">Identificador de contacto del dispositivo para un paquete.</span><span class="sxs-lookup"><span data-stu-id="8e09a-128">The device contact identifier for a packet.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e09a-129">GUID_SERIAL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="8e09a-129">GUID_SERIAL_NUMBER</span></span><br/></td>
<td><span data-ttu-id="8e09a-130">Identifica el paquete.</span><span class="sxs-lookup"><span data-stu-id="8e09a-130">Identifies the packet.</span></span> <span data-ttu-id="8e09a-131">Este es el mismo valor que se usa para recuperar el paquete de la cola de paquetes.</span><span class="sxs-lookup"><span data-stu-id="8e09a-131">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e09a-132">GUID_TANGENT_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="8e09a-132">GUID_TANGENT_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="8e09a-133">El GUID para el objeto PacketProperty que representa la presión de la punta del lápiz a lo largo del plano de la superficie de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="8e09a-133">The GUID for the PacketProperty object that represents pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e09a-134">GUID_TIMER_TICK</span><span class="sxs-lookup"><span data-stu-id="8e09a-134">GUID_TIMER_TICK</span></span><br/></td>
<td><span data-ttu-id="8e09a-135">Hora a la que se generó el paquete.</span><span class="sxs-lookup"><span data-stu-id="8e09a-135">Time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e09a-136">GUID_TWIST_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="8e09a-136">GUID_TWIST_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="8e09a-137">Rotación en el sentido de las agujas del reloj del cursor alrededor de su propio eje.</span><span class="sxs-lookup"><span data-stu-id="8e09a-137">Clockwise rotation of the cursor around its own axis.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e09a-138">GUID_X</span><span class="sxs-lookup"><span data-stu-id="8e09a-138">GUID_X</span></span><br/></td>
<td><span data-ttu-id="8e09a-139">Coordenada x del espacio de coordenadas de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8e09a-139">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="8e09a-140">Cada paquete contiene esta propiedad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8e09a-140">Each packet contains this property by default.</span></span> <span data-ttu-id="8e09a-141">El origen (0,0) de la tableta es la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="8e09a-141">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e09a-142">GUID_X_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="8e09a-142">GUID_X_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="8e09a-143">En el caso de un cursor de lápiz, la orientación de la inclinación x es el ángulo entre el plano y, z y el plano del eje y y el lápiz.</span><span class="sxs-lookup"><span data-stu-id="8e09a-143">For a pen cursor, the x-tilt orientation is the angle between the y,z-plane and the pen and y-axis plane.</span></span> <span data-ttu-id="8e09a-144">El valor es 0 cuando el lápiz es perpendicular a la superficie de dibujo y es positivo cuando el lápiz está a la derecha de la perpendicular.</span><span class="sxs-lookup"><span data-stu-id="8e09a-144">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e09a-145">GUID_Y</span><span class="sxs-lookup"><span data-stu-id="8e09a-145">GUID_Y</span></span><br/></td>
<td><span data-ttu-id="8e09a-146">Coordenada y del espacio de coordenadas de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8e09a-146">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="8e09a-147">Cada paquete contiene esta propiedad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8e09a-147">Each packet contains this property by default.</span></span> <span data-ttu-id="8e09a-148">El origen (0,0) de la tableta es la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="8e09a-148">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e09a-149">GUID_Y_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="8e09a-149">GUID_Y_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="8e09a-150">Para un cursor de lápiz, la orientación de inclinación y es el ángulo entre el plano x, z y el lápiz y el plano del eje x.</span><span class="sxs-lookup"><span data-stu-id="8e09a-150">For a pen cursor, the y-tilt orientation is the angle between the x,z-plane and the pen and x-axis plane.</span></span> <span data-ttu-id="8e09a-151">El valor es 0 cuando el lápiz es perpendicular a la superficie de dibujo y es positivo cuando el lápiz está hacia arriba o fuera del usuario.</span><span class="sxs-lookup"><span data-stu-id="8e09a-151">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward, or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e09a-152">GUID_Z</span><span class="sxs-lookup"><span data-stu-id="8e09a-152">GUID_Z</span></span><br/></td>
<td><span data-ttu-id="8e09a-153">La coordenada z o la distancia de la punta del lápiz desde la superficie de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8e09a-153">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="8e09a-154">El tipo de enumeración <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> determina la unidad de medida para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8e09a-154">The <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> enumeration type determines the unit of measurement for this property.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="8e09a-155">El campo TangentPressure representa la presión a lo largo del plano de la superficie de la tableta. el campo NormalPressure representa la presión perpendicular al plano de la superficie de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="8e09a-155">The TangentPressure field represents pressure along the plane of the tablet surface; the NormalPressure field represents pressure perpendicular to the plane of the tablet surface.</span></span>

 

 

 




