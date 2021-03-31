---
description: La categoría de \_ BIOmétrica de categoría de sensor \_ contiene sensores que proporcionan información sobre los seres vivo.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154060"
---
# <a name="sensor_category_biometric"></a><span data-ttu-id="c3675-103">biométrica de categoría de SENSOR \_ \_</span><span class="sxs-lookup"><span data-stu-id="c3675-103">SENSOR\_CATEGORY\_BIOMETRIC</span></span>

<span data-ttu-id="c3675-104">La categoría de \_ BIOmétrica de categoría de sensor \_ contiene sensores que proporcionan información sobre los seres vivo.</span><span class="sxs-lookup"><span data-stu-id="c3675-104">The SENSOR\_CATEGORY\_BIOMETRIC category contains sensors that provide information about living beings.</span></span>

<span data-ttu-id="c3675-105">**Tipos de sensores definidos por la plataforma**</span><span class="sxs-lookup"><span data-stu-id="c3675-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="c3675-106">Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c3675-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="c3675-107">Tipo de sensor</span><span class="sxs-lookup"><span data-stu-id="c3675-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="c3675-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3675-108">Description</span></span>                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <span data-ttu-id="c3675-109"><dt>**Sensor \_ de ESCRIBIR \_ \_ presencia humana**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt></span><span class="sxs-lookup"><span data-stu-id="c3675-109"><dt>**SENSOR\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt></span></span> </dl>    | <span data-ttu-id="c3675-110">Sensores que detectan la presencia humana.</span><span class="sxs-lookup"><span data-stu-id="c3675-110">Sensors that detect human presence.</span></span><br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <span data-ttu-id="c3675-111"><dt>**Sensor \_ de Escriba \_ \_ proximidad humana**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span><span class="sxs-lookup"><span data-stu-id="c3675-111"><dt>**SENSOR\_TYPE\_HUMAN\_PROXIMITY**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span></span> </dl> | <span data-ttu-id="c3675-112">Sensores que detectan proximidad humana.</span><span class="sxs-lookup"><span data-stu-id="c3675-112">Sensors that detect human proximity.</span></span><br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <span data-ttu-id="c3675-113"><dt>**Sensor \_ de Escriba \_ Touch**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span><span class="sxs-lookup"><span data-stu-id="c3675-113"><dt>**SENSOR\_TYPE\_TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span></span> </dl>                                | <span data-ttu-id="c3675-114">Sensores táctiles.</span><span class="sxs-lookup"><span data-stu-id="c3675-114">Touch sensors.</span></span><br/>                       |



<span data-ttu-id="c3675-115">**Campos de datos definidos por la plataforma**</span><span class="sxs-lookup"><span data-stu-id="c3675-115">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="c3675-116">Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ \_ GUID biométrico \_ :</span><span class="sxs-lookup"><span data-stu-id="c3675-116">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_BIOMETRIC\_GUID:</span></span>

<span data-ttu-id="c3675-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span><span class="sxs-lookup"><span data-stu-id="c3675-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span></span>

<span data-ttu-id="c3675-118">Esta categoría incluye los siguientes campos de datos definidos por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c3675-118">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="c3675-119">Nombre del campo de datos y PID</span><span class="sxs-lookup"><span data-stu-id="c3675-119">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="c3675-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3675-120">Description</span></span>                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <span data-ttu-id="c3675-121"><dt>**Sensor \_ de \_ \_ \_ Presencia humana de tipo de datos**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="c3675-121"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>(PID = 2) </dt></span></span> </dl>                          | <span data-ttu-id="c3675-122">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c3675-122">**VT\_BOOL**</span></span><br/> <span data-ttu-id="c3675-123">**True** cuando un usuario usa el equipo.</span><span class="sxs-lookup"><span data-stu-id="c3675-123">**TRUE** when a human is using the computer.</span></span><br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <span data-ttu-id="c3675-124"><dt>**Sensor \_ de \_Medidor de \_ \_ proximidad humana \_ de tipo de datos**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="c3675-124"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PROXIMITY\_METERS**</dt> <dt>(PID = 3) </dt></span></span> </dl> | <span data-ttu-id="c3675-125">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="c3675-125">**VT\_R4**</span></span><br/> <span data-ttu-id="c3675-126">Distancia entre un usuario y el equipo, en metros.</span><span class="sxs-lookup"><span data-stu-id="c3675-126">Distance between a human and the computer, in meters.</span></span><br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <span data-ttu-id="c3675-127"><dt>**Sensor \_ de \_ \_ \_ Estado de tipo de datos táctil**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="c3675-127"><dt>**SENSOR\_DATA\_TYPE\_TOUCH\_STATE**</dt> <dt>(PID = 4) </dt></span></span> </dl>                                   | <span data-ttu-id="c3675-128">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c3675-128">**VT\_BOOL**</span></span><br/> <span data-ttu-id="c3675-129">**True** cuando se toca el sensor táctil; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c3675-129">**TRUE** when the touch sensor is being touched; otherwise, **FALSE**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c3675-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3675-130">Requirements</span></span>



| <span data-ttu-id="c3675-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3675-131">Requirement</span></span> | <span data-ttu-id="c3675-132">Value</span><span class="sxs-lookup"><span data-stu-id="c3675-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3675-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3675-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c3675-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3675-134">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c3675-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3675-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c3675-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c3675-136">None supported</span></span><br/>                                                            |
| <span data-ttu-id="c3675-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3675-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3675-138"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3675-138"><dt>Sensors.h</dt></span></span> </dl> |



 

 




