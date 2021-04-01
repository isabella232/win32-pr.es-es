---
description: La categoría de SENSOR \_ \_ otra categoría contiene sensores que admiten la clase personalizada en el controlador de clase HID.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082056"
---
# <a name="sensor_category_other"></a><span data-ttu-id="6e98a-103">Categoría de SENSOR \_ \_ diferente</span><span class="sxs-lookup"><span data-stu-id="6e98a-103">SENSOR\_CATEGORY\_OTHER</span></span>

<span data-ttu-id="6e98a-104">La categoría de SENSOR \_ \_ otra categoría contiene sensores que admiten la clase personalizada en el controlador de clase HID.</span><span class="sxs-lookup"><span data-stu-id="6e98a-104">The SENSOR\_CATEGORY\_OTHER category contains sensors that support the Custom class in the HID Class driver.</span></span>

<dl> <dt>

<span data-ttu-id="6e98a-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**tipo de SENSOR \_ \_ personalizado**</span><span class="sxs-lookup"><span data-stu-id="6e98a-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**SENSOR\_TYPE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e98a-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span><span class="sxs-lookup"><span data-stu-id="6e98a-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span></span>
</dt> <dt>



<span data-ttu-id="6e98a-107">Sensor personalizado que admite la clase personalizada en el controlador de clase de HID.</span><span class="sxs-lookup"><span data-stu-id="6e98a-107">Custom sensor that supports the Custom class in the HID Class driver.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="6e98a-108">**Campos de datos definidos por la plataforma**</span><span class="sxs-lookup"><span data-stu-id="6e98a-108">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="6e98a-109">Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ \_ \_ GUID personalizado:</span><span class="sxs-lookup"><span data-stu-id="6e98a-109">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_CUSTOM\_GUID:</span></span>

<span data-ttu-id="6e98a-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span><span class="sxs-lookup"><span data-stu-id="6e98a-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span></span>

<span data-ttu-id="6e98a-111">Esta categoría incluye los siguientes campos de datos definidos por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="6e98a-111">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="6e98a-112">Nombre del campo de datos y PID</span><span class="sxs-lookup"><span data-stu-id="6e98a-112">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="6e98a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e98a-113">Description</span></span>                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <span data-ttu-id="6e98a-114"><dt>**Sensor \_ de \_ \_ \_ Uso personalizado de tipo de datos**</dt> <dt> (PID = 5)</dt></span><span class="sxs-lookup"><span data-stu-id="6e98a-114"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_USAGE**</dt> <dt> (PID = 5) </dt></span></span> </dl>                          | <span data-ttu-id="6e98a-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="6e98a-115">**VT\_UI4**</span></span><br/> <span data-ttu-id="6e98a-116">Un uso de HID que se puede usar para distinguir varios sensores personalizados.</span><span class="sxs-lookup"><span data-stu-id="6e98a-116">A HID usage which can be used to distinguish multiple, custom sensors.</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <span data-ttu-id="6e98a-117"><dt>**Sensor \_ de \_ \_ \_ \_ Matriz booleana personalizada de tipo de datos**</dt> <dt> (PID = 6)</dt></span><span class="sxs-lookup"><span data-stu-id="6e98a-117"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_BOOLEAN\_ARRAY**</dt> <dt> (PID = 6) </dt></span></span> </dl> | <span data-ttu-id="6e98a-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="6e98a-118">**VT\_UI4**</span></span><br/> <span data-ttu-id="6e98a-119">Matriz de valores booleanos para un sensor personalizado determinado.</span><span class="sxs-lookup"><span data-stu-id="6e98a-119">An array of Boolean values for a given custom sensor.</span></span><br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <span data-ttu-id="6e98a-120"><dt>**Sensor \_ de Tipo de datos \_ \_ Custom \_ VALUE1**</dt> <dt> (PID = 7)</dt></span><span class="sxs-lookup"><span data-stu-id="6e98a-120"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE1**</dt> <dt> (PID = 7) </dt></span></span> </dl>                       | <span data-ttu-id="6e98a-121">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6e98a-121">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6e98a-122">Uno de los seis valores disponibles para un sensor personalizado determinado.</span><span class="sxs-lookup"><span data-stu-id="6e98a-122">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <span data-ttu-id="6e98a-123"><dt>**Sensor \_ de Tipo de datos \_ \_ personalizado \_ VALUE2**</dt> <dt> (PID = 8)</dt></span><span class="sxs-lookup"><span data-stu-id="6e98a-123"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE2**</dt> <dt> (PID = 8) </dt></span></span> </dl>                       | <span data-ttu-id="6e98a-124">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6e98a-124">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6e98a-125">Uno de los seis valores disponibles para un sensor personalizado determinado.</span><span class="sxs-lookup"><span data-stu-id="6e98a-125">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <span data-ttu-id="6e98a-126"><dt>**Sensor \_ de \_Tipo de \_ datos \_ VALUE3 personalizado**</dt> <dt> (PID = 9)</dt></span><span class="sxs-lookup"><span data-stu-id="6e98a-126"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE3**</dt> <dt> (PID = 9) </dt></span></span> </dl>                       | <span data-ttu-id="6e98a-127">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6e98a-127">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6e98a-128">Uno de los seis valores disponibles para un sensor personalizado determinado.</span><span class="sxs-lookup"><span data-stu-id="6e98a-128">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <span data-ttu-id="6e98a-129"><dt>**Sensor \_ de \_Tipo de \_ datos \_ VALUE4 personalizado**</dt> <dt> (PID = 10)</dt></span><span class="sxs-lookup"><span data-stu-id="6e98a-129"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE4**</dt> <dt> (PID = 10) </dt></span></span> </dl>                      | <span data-ttu-id="6e98a-130">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6e98a-130">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6e98a-131">Uno de los seis valores disponibles para un sensor personalizado determinado.</span><span class="sxs-lookup"><span data-stu-id="6e98a-131">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <span data-ttu-id="6e98a-132"><dt>**Sensor \_ de \_Tipo de \_ datos \_ VALUE5 personalizado**</dt> <dt> (PID = 11)</dt></span><span class="sxs-lookup"><span data-stu-id="6e98a-132"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE5**</dt> <dt> (PID = 11) </dt></span></span> </dl>                      | <span data-ttu-id="6e98a-133">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6e98a-133">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6e98a-134">Uno de los seis valores disponibles para un sensor personalizado determinado.</span><span class="sxs-lookup"><span data-stu-id="6e98a-134">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <span data-ttu-id="6e98a-135"><dt>**Sensor \_ de \_Tipo de \_ datos \_ VALUE6 personalizado**</dt> <dt> (PID = 12)</dt></span><span class="sxs-lookup"><span data-stu-id="6e98a-135"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE6**</dt> <dt> (PID = 12) </dt></span></span> </dl>                      | <span data-ttu-id="6e98a-136">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6e98a-136">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6e98a-137">Uno de los seis valores disponibles para un sensor personalizado determinado.</span><span class="sxs-lookup"><span data-stu-id="6e98a-137">One of six available values for a given custom sensor.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="6e98a-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e98a-138">Remarks</span></span>

<span data-ttu-id="6e98a-139">Un sensor que admita la clase genérica en el controlador de clase HID se asignará a una de las otras categorías definidas (biométrico, eléctrico, entorno, etc.).</span><span class="sxs-lookup"><span data-stu-id="6e98a-139">A sensor that supports the Generic class in the HID class driver will map to one of the other defined categories (biometric, electrical, environmental, and so on).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e98a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e98a-140">Requirements</span></span>



| <span data-ttu-id="6e98a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e98a-141">Requirement</span></span> | <span data-ttu-id="6e98a-142">Value</span><span class="sxs-lookup"><span data-stu-id="6e98a-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e98a-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e98a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6e98a-144">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e98a-144">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6e98a-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e98a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6e98a-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6e98a-146">None supported</span></span><br/>                                                            |
| <span data-ttu-id="6e98a-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e98a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e98a-148"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e98a-148"><dt>Sensors.h</dt></span></span> </dl> |



 

 




