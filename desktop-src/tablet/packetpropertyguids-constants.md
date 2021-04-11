---
description: Define valores que especifican las propiedades del paquete.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Constantes PacketPropertyGuids (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279165"
---
# <a name="packetpropertyguids-constants"></a><span data-ttu-id="8c159-103">Constantes de PacketPropertyGuids</span><span class="sxs-lookup"><span data-stu-id="8c159-103">PacketPropertyGuids Constants</span></span>

<span data-ttu-id="8c159-104">Define valores que especifican las propiedades del paquete.</span><span class="sxs-lookup"><span data-stu-id="8c159-104">Defines values that specify the packet properties.</span></span> <span data-ttu-id="8c159-105">Tablet PCAPI usa identificadores únicos globales (GUID) para identificar las propiedades de los paquetes, que en COM son cadenas constantes.</span><span class="sxs-lookup"><span data-stu-id="8c159-105">The Tablet PCAPI uses globally unique identifiers (GUIDs) to identify packet properties, which in COM are constant strings.</span></span>

<span data-ttu-id="8c159-106">En C++, puede tener acceso a estas constantes en el archivo de encabezado Msinkaut. h, que se encuentra en <systemdrive> el \\ Directorio: archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ include Si instaló el SDK en la ubicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8c159-106">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span> <span data-ttu-id="8c159-107">En C++, estas constantes son WCHARs, no BSTR.</span><span class="sxs-lookup"><span data-stu-id="8c159-107">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="8c159-108">Conviértalos en BSTR antes de usarlo.</span><span class="sxs-lookup"><span data-stu-id="8c159-108">Convert them into BSTRs before use.</span></span> <span data-ttu-id="8c159-109">Para obtener más información sobre el tipo de datos BSTR, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="8c159-109">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

<span data-ttu-id="8c159-110">En la tabla siguiente se enumeran los campos de identificador único global (GUID) de la propiedad de paquete disponible.</span><span class="sxs-lookup"><span data-stu-id="8c159-110">The following table lists the available packet property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="8c159-111">Utilice estos GUID para especificar las propiedades que contiene el paquete al crear el contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8c159-111">Use these GUIDs to specify which properties the packet contains when you create the tablet context.</span></span> <span data-ttu-id="8c159-112">Para determinar el intervalo y la resolución de una propiedad, llame al método [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) .</span><span class="sxs-lookup"><span data-stu-id="8c159-112">To determine the range and resolution of a property, call the [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) method.</span></span> <span data-ttu-id="8c159-113">Las constantes de la tabla siguiente a partir de "STR \_ " son representaciones de cadena de las constantes binarias correspondientes que se muestran en la misma celda de tabla.</span><span class="sxs-lookup"><span data-stu-id="8c159-113">The constants in the table below beginning with "STR\_" are string representations of the corresponding binary constants shown in the same table cell.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8c159-114">Constante</span><span class="sxs-lookup"><span data-stu-id="8c159-114">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8c159-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c159-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <span data-ttu-id="8c159-116"><dt><strong>STR_GUID_X o GUID_PACKETPROPERTY_GUID_X</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-116"><dt><strong>STR_GUID_X or GUID_PACKETPROPERTY_GUID_X</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-117">Coordenada x del espacio de coordenadas de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8c159-117">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="8c159-118">Cada paquete contiene esta propiedad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8c159-118">Each packet contains this property by default.</span></span> <span data-ttu-id="8c159-119">El origen (0,0) de la tableta es la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="8c159-119">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="8c159-120"><dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-120"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-121">Coordenada y del espacio de coordenadas de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8c159-121">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="8c159-122">Cada paquete contiene esta propiedad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8c159-122">Each packet contains this property by default.</span></span> <span data-ttu-id="8c159-123">El origen (0,0) de la tableta es la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="8c159-123">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="8c159-124"><dt><strong>STR_GUID_Y o GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-124"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-125">Coordenada y del espacio de coordenadas de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8c159-125">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="8c159-126">Cada paquete contiene esta propiedad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8c159-126">Each packet contains this property by default.</span></span> <span data-ttu-id="8c159-127">El origen (0,0) de la tableta es la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="8c159-127">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <span data-ttu-id="8c159-128"><dt><strong>STR_GUID_Z o GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-128"><dt><strong>STR_GUID_Z or GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-129">La coordenada z o la distancia de la punta del lápiz desde la superficie de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8c159-129">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="8c159-130">El tipo de enumeración <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> determina la unidad de medida para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8c159-130">The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> enumeration type determines the unit of measurement for this property.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <span data-ttu-id="8c159-131"><dt><strong>STR_GUID_PAKETSTATUS o GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-131"><dt><strong>STR_GUID_PAKETSTATUS or GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-132">Contiene uno o varios de los siguientes valores de marca:</span><span class="sxs-lookup"><span data-stu-id="8c159-132">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="8c159-133">El cursor toca la superficie de dibujo (valor = 1).</span><span class="sxs-lookup"><span data-stu-id="8c159-133">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="8c159-134">El cursor se invierte.</span><span class="sxs-lookup"><span data-stu-id="8c159-134">The cursor is inverted.</span></span> <span data-ttu-id="8c159-135">Por ejemplo, el extremo del borrador del lápiz apunta hacia la superficie (valor = 2).</span><span class="sxs-lookup"><span data-stu-id="8c159-135">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="8c159-136">No se usa (valor = 4).</span><span class="sxs-lookup"><span data-stu-id="8c159-136">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="8c159-137">Se presiona el botón de barril (valor = 8).</span><span class="sxs-lookup"><span data-stu-id="8c159-137">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="8c159-138"><dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-138"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-139">La hora a la que se generó el paquete.</span><span class="sxs-lookup"><span data-stu-id="8c159-139">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="8c159-140"><dt><strong>STR_GUID_TIMERTICK o GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-140"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-141">La hora a la que se generó el paquete.</span><span class="sxs-lookup"><span data-stu-id="8c159-141">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <span data-ttu-id="8c159-142"><dt><strong>STR_GUID_SERIALNUMBER o GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-142"><dt><strong>STR_GUID_SERIALNUMBER or GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-143">La propiedad de paquete para identificar el paquete.</span><span class="sxs-lookup"><span data-stu-id="8c159-143">The packet property for identifying the packet.</span></span><br/> <span data-ttu-id="8c159-144">Este es el mismo valor que se usa para recuperar el paquete de la cola de paquetes.</span><span class="sxs-lookup"><span data-stu-id="8c159-144">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <span data-ttu-id="8c159-145"><dt><strong>STR_GUID_NORMALPRESSURE o GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-145"><dt><strong>STR_GUID_NORMALPRESSURE or GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-146">Presión de la punta del lápiz perpendicular a la superficie de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8c159-146">The pressure of the pen tip perpendicular to the tablet surface.</span></span><br/> <span data-ttu-id="8c159-147">Cuanto mayor sea la presión de la punta del lápiz, mayor será la tinta dibujada.</span><span class="sxs-lookup"><span data-stu-id="8c159-147">The greater the pressure on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <span data-ttu-id="8c159-148"><dt><strong>STR_GUID_TANGENTPRESSURE o GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-148"><dt><strong>STR_GUID_TANGENTPRESSURE or GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-149">Presión de la punta del lápiz a lo largo del plano de la superficie de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8c159-149">The pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <span data-ttu-id="8c159-150"><dt><strong>STR_GUID_BUTTONPRESSURE o GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-150"><dt><strong>STR_GUID_BUTTONPRESSURE or GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-151">Presión sobre un botón sensible a la presión.</span><span class="sxs-lookup"><span data-stu-id="8c159-151">The pressure on a pressure sensitive button.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <span data-ttu-id="8c159-152"><dt><strong>STR_GUID_XTILTORIENTATION o GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-152"><dt><strong>STR_GUID_XTILTORIENTATION or GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-153">Ángulo entre el plano y, z y el lápiz y el plano del eje y.</span><span class="sxs-lookup"><span data-stu-id="8c159-153">The angle between the y,z-plane and the pen and y-axis plane.</span></span><br/> <span data-ttu-id="8c159-154">Se aplica a un cursor de lápiz.</span><span class="sxs-lookup"><span data-stu-id="8c159-154">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="8c159-155">El valor es 0 cuando el lápiz es perpendicular a la superficie de dibujo y es positivo cuando el lápiz está a la derecha de la perpendicular.</span><span class="sxs-lookup"><span data-stu-id="8c159-155">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <span data-ttu-id="8c159-156"><dt><strong>STR_GUID_YTILTORIENTATION o GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-156"><dt><strong>STR_GUID_YTILTORIENTATION or GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-157">Ángulo entre el plano x, z y el lápiz y el plano del eje x.</span><span class="sxs-lookup"><span data-stu-id="8c159-157">The angle between the x,z-plane and the pen and x-axis plane.</span></span><br/> <span data-ttu-id="8c159-158">Se aplica a un cursor de lápiz.</span><span class="sxs-lookup"><span data-stu-id="8c159-158">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="8c159-159">El valor es 0 cuando el lápiz es perpendicular a la superficie de dibujo y es positivo cuando el lápiz está hacia arriba o fuera del usuario.</span><span class="sxs-lookup"><span data-stu-id="8c159-159">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <span data-ttu-id="8c159-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION o GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION or GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-161">Rotación en el sentido de las agujas del reloj del cursor sobre el eje z a través de un intervalo circular completo.</span><span class="sxs-lookup"><span data-stu-id="8c159-161">The clockwise rotation of the cursor about the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <span data-ttu-id="8c159-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION o GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION or GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-163">Ángulo entre el eje del lápiz y la superficie de la tableta.</span><span class="sxs-lookup"><span data-stu-id="8c159-163">The angle between the axis of the pen and the surface of the tablet.</span></span><br/> <span data-ttu-id="8c159-164">El valor es 0 cuando el lápiz es paralelo a la superficie y 90 cuando el lápiz es perpendicular a la superficie.</span><span class="sxs-lookup"><span data-stu-id="8c159-164">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span><br/> <span data-ttu-id="8c159-165">Los valores son negativos cuando se invierte el lápiz.</span><span class="sxs-lookup"><span data-stu-id="8c159-165">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <span data-ttu-id="8c159-166"><dt><strong>STR_GUID_TWISTORIENTATION o GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-166"><dt><strong>STR_GUID_TWISTORIENTATION or GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-167">Rotación en el sentido de las agujas del reloj del cursor sobre su propio eje.</span><span class="sxs-lookup"><span data-stu-id="8c159-167">The clockwise rotation of the cursor about its own axis.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <span data-ttu-id="8c159-168"><dt><strong>STR_GUID_PITCHROTATION o GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-168"><dt><strong>STR_GUID_PITCHROTATION or GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-169">La propiedad de paquete que indica si la punta está por encima o por debajo de una línea horizontal que es perpendicular a la superficie de escritura.</span><span class="sxs-lookup"><span data-stu-id="8c159-169">The packet property that indicates whether the tip is above or below a horizontal line that is perpendicular to the writing surface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8c159-170">Esto requiere un digitalizador 3D.</span><span class="sxs-lookup"><span data-stu-id="8c159-170">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="8c159-171">El valor es positivo si la punta está por encima de la línea y es negativo si está por debajo de la línea.</span><span class="sxs-lookup"><span data-stu-id="8c159-171">The value is positive if the tip is above the line and negative if it is below the line.</span></span> <span data-ttu-id="8c159-172">Por ejemplo, si mantiene el lápiz delante de usted y escribe en una pared imaginaria, el paso es positivo si la punta está por encima de una línea que se extiende desde usted a la pared.</span><span class="sxs-lookup"><span data-stu-id="8c159-172">For example, if you hold the pen in front of you and write on an imaginary wall, the pitch is positive if the tip is above a line extending from you to the wall.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <span data-ttu-id="8c159-173"><dt><strong>STR_GUID_ROLLROTATION o GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-173"><dt><strong>STR_GUID_ROLLROTATION or GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-174">Rotación en el sentido de las agujas del reloj del lápiz alrededor de su propio eje.</span><span class="sxs-lookup"><span data-stu-id="8c159-174">The clockwise rotation of the pen around its own axis.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8c159-175">Esto requiere un digitalizador 3D.</span><span class="sxs-lookup"><span data-stu-id="8c159-175">This requires a 3D digitizer.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="8c159-176"><dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-176"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-177">Ángulo del lápiz situado a la izquierda o a la derecha alrededor del centro de su eje horizontal cuando el lápiz es horizontal.</span><span class="sxs-lookup"><span data-stu-id="8c159-177">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8c159-178">Esto requiere un digitalizador 3D.</span><span class="sxs-lookup"><span data-stu-id="8c159-178">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="8c159-179">Si mantiene el lápiz delante y lo escribe en un muro imaginario, el valor de guiñada cero indica que el lápiz es perpendicular a la pared.</span><span class="sxs-lookup"><span data-stu-id="8c159-179">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="8c159-180">El valor es negativo si la punta está a la izquierda de la perpendicular y positiva si la punta está a la derecha de la perpendicular.</span><span class="sxs-lookup"><span data-stu-id="8c159-180">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="8c159-181"><dt><strong>STR_GUID_YAWROTATION o GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-181"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-182">Ángulo del lápiz situado a la izquierda o a la derecha alrededor del centro de su eje horizontal cuando el lápiz es horizontal.</span><span class="sxs-lookup"><span data-stu-id="8c159-182">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8c159-183">Esto requiere un digitalizador 3D.</span><span class="sxs-lookup"><span data-stu-id="8c159-183">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="8c159-184">Si mantiene el lápiz delante y lo escribe en un muro imaginario, el valor de guiñada cero indica que el lápiz es perpendicular a la pared.</span><span class="sxs-lookup"><span data-stu-id="8c159-184">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="8c159-185">El valor es negativo si la punta está a la izquierda de la perpendicular y positiva si la punta está a la derecha de la perpendicular.</span><span class="sxs-lookup"><span data-stu-id="8c159-185">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <span data-ttu-id="8c159-186"><dt><strong>STR_GUID_WIDTH o GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-186"><dt><strong>STR_GUID_WIDTH or GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-187">Ancho del área de contacto en un digitalizador táctil.</span><span class="sxs-lookup"><span data-stu-id="8c159-187">The width of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <span data-ttu-id="8c159-188"><dt><strong>STR_GUID_HEIGHT o GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-188"><dt><strong>STR_GUID_HEIGHT or GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-189">Alto del área de contacto en un digitalizador táctil.</span><span class="sxs-lookup"><span data-stu-id="8c159-189">The height of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <span data-ttu-id="8c159-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE o GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE or GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-191">El nivel de confianza en el que había contacto con el dedo en un digitalizador táctil.</span><span class="sxs-lookup"><span data-stu-id="8c159-191">The level of confidence that there was finger contact on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <span data-ttu-id="8c159-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID o GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8c159-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID or GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="8c159-193">Identificador de contacto del dispositivo para un paquete.</span><span class="sxs-lookup"><span data-stu-id="8c159-193">The device contact identifier for a packet.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="8c159-194">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c159-194">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c159-195">Todos los valores de paquetes procedentes del hardware de Tablet PC son enteros de tamaño de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8c159-195">All packet values coming from the tablet hardware are 32-bit size integers.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c159-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c159-196">Requirements</span></span>



| <span data-ttu-id="8c159-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c159-197">Requirement</span></span> | <span data-ttu-id="8c159-198">Value</span><span class="sxs-lookup"><span data-stu-id="8c159-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c159-199">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c159-199">Minimum supported client</span></span><br/> | <span data-ttu-id="8c159-200">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8c159-200">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8c159-201">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c159-201">Minimum supported server</span></span><br/> | <span data-ttu-id="8c159-202">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8c159-202">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8c159-203">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c159-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c159-204"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8c159-204"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c159-205">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c159-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c159-206">**Método IsPacketPropertySupported**</span><span class="sxs-lookup"><span data-stu-id="8c159-206">**IsPacketPropertySupported Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[<span data-ttu-id="8c159-207">**Método GetPropertyMetrics**</span><span class="sxs-lookup"><span data-stu-id="8c159-207">**GetPropertyMetrics Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[<span data-ttu-id="8c159-208">**Interfaz IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="8c159-208">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




