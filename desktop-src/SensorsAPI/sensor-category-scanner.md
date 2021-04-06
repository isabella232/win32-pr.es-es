---
description: La \_ categoría de analizador categoría de sensor \_ contiene sensores que proporcionan información obtenida mediante el análisis.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001034"
---
# <a name="sensor_category_scanner"></a><span data-ttu-id="b3852-103">\_escáner de categoría de sensor \_</span><span class="sxs-lookup"><span data-stu-id="b3852-103">SENSOR\_CATEGORY\_SCANNER</span></span>

<span data-ttu-id="b3852-104">La \_ categoría de analizador categoría de sensor \_ contiene sensores que proporcionan información obtenida mediante el análisis.</span><span class="sxs-lookup"><span data-stu-id="b3852-104">The SENSOR\_CATEGORY\_SCANNER category contains sensors that provide information that is obtained by scanning.</span></span>

<span data-ttu-id="b3852-105">**Tipos de sensores definidos por la plataforma**</span><span class="sxs-lookup"><span data-stu-id="b3852-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="b3852-106">Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="b3852-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="b3852-107">Tipo de sensor</span><span class="sxs-lookup"><span data-stu-id="b3852-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="b3852-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3852-108">Description</span></span>                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <span data-ttu-id="b3852-109"><dt>**Sensor \_ de ESCRIBIR \_ \_ escáner de código de barras**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span><span class="sxs-lookup"><span data-stu-id="b3852-109"><dt>**SENSOR\_TYPE\_BARCODE\_SCANNER**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span></span> </dl> | <span data-ttu-id="b3852-110">Sensores que usan el examen óptico para leer códigos de barras.</span><span class="sxs-lookup"><span data-stu-id="b3852-110">Sensors that use optical scanning to read bar codes.</span></span><br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <span data-ttu-id="b3852-111"><dt>**Sensor \_ de ESCRIBIR \_ \_ escáner RFID**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span><span class="sxs-lookup"><span data-stu-id="b3852-111"><dt>**SENSOR\_TYPE\_RFID\_SCANNER**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span></span> </dl>          | <span data-ttu-id="b3852-112">Sensores de detección de ID. de radio.</span><span class="sxs-lookup"><span data-stu-id="b3852-112">Radio-frequency ID scanning sensors.</span></span><br/>                 |



<span data-ttu-id="b3852-113">**Campos de datos definidos por la plataforma**</span><span class="sxs-lookup"><span data-stu-id="b3852-113">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="b3852-114">Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ GUID del \_ analizador \_ :</span><span class="sxs-lookup"><span data-stu-id="b3852-114">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_SCANNER\_GUID:</span></span>

<span data-ttu-id="b3852-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span><span class="sxs-lookup"><span data-stu-id="b3852-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span></span>

<span data-ttu-id="b3852-116">Esta categoría incluye los siguientes campos de datos definidos por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="b3852-116">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="b3852-117">Nombre del campo de datos y PID</span><span class="sxs-lookup"><span data-stu-id="b3852-117">Data field name and PID</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="b3852-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3852-118">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <span data-ttu-id="b3852-119"><dt>**Sensor \_ de Tipo de datos de \_ \_ \_ etiqueta RFID \_ 40 \_ bits**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="b3852-119"><dt>**SENSOR\_DATA\_TYPE\_RFID\_TAG\_40\_BIT**</dt> <dt>(PID = 2) </dt></span></span> </dl> | <span data-ttu-id="b3852-120">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="b3852-120">**VT\_UI8**</span></span><br/> <span data-ttu-id="b3852-121">valor de etiqueta de identificador de frecuencia de radio de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="b3852-121">40-bit radio frequency ID tag value.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b3852-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3852-122">Requirements</span></span>



| <span data-ttu-id="b3852-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3852-123">Requirement</span></span> | <span data-ttu-id="b3852-124">Value</span><span class="sxs-lookup"><span data-stu-id="b3852-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b3852-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3852-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b3852-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3852-126">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b3852-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3852-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b3852-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b3852-128">None supported</span></span><br/>                                                            |
| <span data-ttu-id="b3852-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3852-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3852-130"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3852-130"><dt>Sensors.h</dt></span></span> </dl> |



 

 




