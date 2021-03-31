---
title: Constantes de WINBIO_SENSOR_MODE (Winbio \_ Types. h)
description: Establezca el modo de adaptador de sensor.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803902"
---
# <a name="winbio_sensor_mode-constants"></a><span data-ttu-id="4f186-103">Constantes de modo de \_ sensor de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="4f186-103">WINBIO\_SENSOR\_MODE Constants</span></span>

<span data-ttu-id="4f186-104">Los valores siguientes se usan en la función [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) para establecer el modo de adaptador de sensor.</span><span class="sxs-lookup"><span data-stu-id="4f186-104">The following values are used in the [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) function to set the sensor adapter mode.</span></span>



| <span data-ttu-id="4f186-105">Constante</span><span class="sxs-lookup"><span data-stu-id="4f186-105">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="4f186-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f186-106">Description</span></span>                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <span data-ttu-id="4f186-107"><dt>**\_modo desconocido del sensor de WINBIO \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f186-107"><dt>**WINBIO\_SENSOR\_UNKNOWN\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="4f186-108">No se conoce el modo operativo.</span><span class="sxs-lookup"><span data-stu-id="4f186-108">The operating mode is not known.</span></span><br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <span data-ttu-id="4f186-109"><dt>**\_modo básico del sensor de WINBIO \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f186-109"><dt>**WINBIO\_SENSOR\_BASIC\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="4f186-110">Use el sensor en modo básico.</span><span class="sxs-lookup"><span data-stu-id="4f186-110">Operate the sensor in basic mode.</span></span> <span data-ttu-id="4f186-111">El sensor actúa únicamente como un dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="4f186-111">The sensor acts only as a capture device.</span></span> <span data-ttu-id="4f186-112">No se utiliza ninguna funcionalidad de almacenamiento o procesamiento incorporado que exista.</span><span class="sxs-lookup"><span data-stu-id="4f186-112">Any onboard processing or storage capabilities that exist are not used.</span></span><br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <span data-ttu-id="4f186-113"><dt>**\_modo avanzado del sensor de WINBIO \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f186-113"><dt>**WINBIO\_SENSOR\_ADVANCED\_MODE**</dt></span></span> </dl>       | <span data-ttu-id="4f186-114">Use el sensor en modo avanzado.</span><span class="sxs-lookup"><span data-stu-id="4f186-114">Operate the sensor in advanced mode.</span></span> <span data-ttu-id="4f186-115">El sensor puede capturar ejemplos y realizar funciones de almacenamiento y búsqueda de coincidencias.</span><span class="sxs-lookup"><span data-stu-id="4f186-115">The sensor can capture samples and perform matching and storage functions.</span></span><br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <span data-ttu-id="4f186-116"><dt>**\_modo de \_ navegación del sensor de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f186-116"><dt>**WINBIO\_SENSOR\_NAVIGATION\_MODE**</dt></span></span> </dl> | <span data-ttu-id="4f186-117">Use el sensor como almohadilla del mouse.</span><span class="sxs-lookup"><span data-stu-id="4f186-117">Operate the sensor as a mouse pad.</span></span> <span data-ttu-id="4f186-118">Actualmente no se admite.</span><span class="sxs-lookup"><span data-stu-id="4f186-118">This is not currently supported.</span></span><br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <span data-ttu-id="4f186-119"><dt>**\_modo de \_ suspensión del sensor de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4f186-119"><dt>**WINBIO\_SENSOR\_SLEEP\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="4f186-120">Use el sensor en modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="4f186-120">Operate the sensor in sleep mode.</span></span><br/>                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="4f186-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f186-121">Requirements</span></span>



| <span data-ttu-id="4f186-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f186-122">Requirement</span></span> | <span data-ttu-id="4f186-123">Value</span><span class="sxs-lookup"><span data-stu-id="4f186-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f186-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f186-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4f186-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f186-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="4f186-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f186-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4f186-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f186-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4f186-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f186-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f186-129"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f186-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f186-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f186-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f186-131">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="4f186-131">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





