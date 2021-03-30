---
description: La \_ categoría de la categoría de la luz del sensor \_ contiene sensores que proporcionan información sobre las características de la luz.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907797"
---
# <a name="sensor_category_light"></a><span data-ttu-id="5462d-103">\_luz de categoría de sensor \_</span><span class="sxs-lookup"><span data-stu-id="5462d-103">SENSOR\_CATEGORY\_LIGHT</span></span>

<span data-ttu-id="5462d-104">La \_ categoría de la categoría de la luz del sensor \_ contiene sensores que proporcionan información sobre las características de la luz.</span><span class="sxs-lookup"><span data-stu-id="5462d-104">The SENSOR\_CATEGORY\_LIGHT category contains sensors that provide information about characteristics of light.</span></span>

<span data-ttu-id="5462d-105">**Tipos de sensores definidos por la plataforma**</span><span class="sxs-lookup"><span data-stu-id="5462d-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="5462d-106">Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="5462d-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="5462d-107">Tipo de sensor</span><span class="sxs-lookup"><span data-stu-id="5462d-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="5462d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5462d-108">Description</span></span>                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <span data-ttu-id="5462d-109"><dt>**Sensor \_ de Escriba \_ \_ luz ambiente**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span><span class="sxs-lookup"><span data-stu-id="5462d-109"><dt>**SENSOR\_TYPE\_AMBIENT\_LIGHT**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span></span> </dl> | <span data-ttu-id="5462d-110">Sensores de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="5462d-110">Ambient light sensors.</span></span><br/> |



<span data-ttu-id="5462d-111">**Campos de datos definidos por la plataforma**</span><span class="sxs-lookup"><span data-stu-id="5462d-111">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="5462d-112">Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ \_ \_ GUID Light:</span><span class="sxs-lookup"><span data-stu-id="5462d-112">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_LIGHT\_GUID:</span></span>

<span data-ttu-id="5462d-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span><span class="sxs-lookup"><span data-stu-id="5462d-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span></span>

<span data-ttu-id="5462d-114">Esta categoría incluye los siguientes campos de datos definidos por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="5462d-114">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="5462d-115">Nombre del campo de datos y PID</span><span class="sxs-lookup"><span data-stu-id="5462d-115">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="5462d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5462d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <span data-ttu-id="5462d-117"><dt> **Tipo de datos de sensor \_ \_ \_ Light \_ CHROMACITY**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="5462d-117"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_CHROMACITY** </dt> <dt> (PID = 4) </dt></span></span> </dl>                     | <span data-ttu-id="5462d-118">**VT \_ Vector \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="5462d-118">**VT\_VECTOR\|VT\_UI1**</span></span><br/> <span data-ttu-id="5462d-119">Cromaticidad como una matriz contada de valores float.</span><span class="sxs-lookup"><span data-stu-id="5462d-119">Chromaticity as a counted array of float values.</span></span><br/> <span data-ttu-id="5462d-120">Los datos de los tipos de vector siempre se serializan como **VT \_ UI1** (una matriz de caracteres sin signo de 1 byte).</span><span class="sxs-lookup"><span data-stu-id="5462d-120">Data for vector types is always serialized as **VT\_UI1** (an array of unsigned, 1-byte characters).</span></span> <span data-ttu-id="5462d-121">Este campo de datos contiene realmente cada valor como un valor real de 4 bytes de IEEE (**VT \_ R4**).</span><span class="sxs-lookup"><span data-stu-id="5462d-121">This data field actually contains each value as an IEEE 4-byte real value (**VT\_R4**).</span></span><br/> <span data-ttu-id="5462d-122">Para obtener información sobre cómo trabajar con matrices, vea [recuperar tipos de vectores](retrieving-vector-types.md).</span><span class="sxs-lookup"><span data-stu-id="5462d-122">For information about working with arrays, see [Retrieving Vector Types](retrieving-vector-types.md).</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <span data-ttu-id="5462d-123"><dt>**Sensor \_ de \_Nivel ligero de tipo de datos \_ \_ \_ Lux**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="5462d-123"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_LEVEL\_LUX**</dt> <dt> (PID = 2) </dt></span></span> </dl>                            | <span data-ttu-id="5462d-124">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="5462d-124">**VT\_R4**</span></span><br/> <span data-ttu-id="5462d-125">Nivel de luminancia, en Lux.</span><span class="sxs-lookup"><span data-stu-id="5462d-125">Illuminance level, in lux.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <span data-ttu-id="5462d-126"><dt>**Sensor \_ de \_Temperatura ligera de tipo de datos \_ \_ \_ Kelvin**</dt> <dt> (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="5462d-126"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_TEMPERATURE\_KELVIN**</dt> <dt> (PID = 3) </dt></span></span> </dl> | <span data-ttu-id="5462d-127">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="5462d-127">**VT\_R4**</span></span><br/> <span data-ttu-id="5462d-128">Temperatura de color, en grados Kelvin.</span><span class="sxs-lookup"><span data-stu-id="5462d-128">Color temperature, in degrees Kelvin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="5462d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5462d-129">Requirements</span></span>



| <span data-ttu-id="5462d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5462d-130">Requirement</span></span> | <span data-ttu-id="5462d-131">Value</span><span class="sxs-lookup"><span data-stu-id="5462d-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5462d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5462d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5462d-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5462d-133">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5462d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5462d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5462d-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5462d-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5462d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5462d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5462d-137"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="5462d-137"><dt>Sensors.h</dt></span></span> </dl> |



 

 




