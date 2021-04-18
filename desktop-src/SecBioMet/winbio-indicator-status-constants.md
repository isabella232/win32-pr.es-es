---
title: Constantes de WINBIO_INDICATOR_STATUS (Winbio \_ Types. h)
description: Establecer una luz del indicador.
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7693fbd2b9b37067738774d172f4bb482edb06e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686246"
---
# <a name="winbio_indicator_status-constants"></a><span data-ttu-id="a9024-103">Constantes de estado de \_ indicador de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="a9024-103">WINBIO\_INDICATOR\_STATUS Constants</span></span>

<span data-ttu-id="a9024-104">Los valores siguientes se pueden usar para establecer una luz del indicador.</span><span class="sxs-lookup"><span data-stu-id="a9024-104">The following values can be used to set an indicator light.</span></span> <span data-ttu-id="a9024-105">De forma predeterminada, los sensores no tendrán una luz encendida, pero las aplicaciones pueden usar estos valores para habilitar o deshabilitar las luces de indicador.</span><span class="sxs-lookup"><span data-stu-id="a9024-105">By default, sensors will not have a light on, but applications can use these values to enable or disable indicator lights.</span></span> <span data-ttu-id="a9024-106">El valor de **\_ \_ Estado del sensor de WINBIO** proporciona más detalles sobre el estado de una luz del indicador activada.</span><span class="sxs-lookup"><span data-stu-id="a9024-106">The **WINBIO\_SENSOR\_STATUS** value provides more detail about the status of an indicator light that is on.</span></span> <span data-ttu-id="a9024-107">Para obtener más información, vea las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="a9024-107">For more information, see the following functions:</span></span>

-   [<span data-ttu-id="a9024-108">**SensorAdapterSetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="a9024-108">**SensorAdapterSetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [<span data-ttu-id="a9024-109">**SensorAdapterGetIndicatorStatus**</span><span class="sxs-lookup"><span data-stu-id="a9024-109">**SensorAdapterGetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [<span data-ttu-id="a9024-110">**SensorAdapterQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="a9024-110">**SensorAdapterQueryStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| <span data-ttu-id="a9024-111">Constante</span><span class="sxs-lookup"><span data-stu-id="a9024-111">Constant</span></span>                                                                                                                                                                            | <span data-ttu-id="a9024-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9024-112">Description</span></span>                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <span data-ttu-id="a9024-113"><dt>**\_indicador \_ de WINBIO en**</dt></span><span class="sxs-lookup"><span data-stu-id="a9024-113"><dt>**WINBIO\_INDICATOR\_ON**</dt></span></span> </dl>    | <span data-ttu-id="a9024-114">La luz del indicador del sensor está activada.</span><span class="sxs-lookup"><span data-stu-id="a9024-114">The sensor indicator light is on.</span></span><br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <span data-ttu-id="a9024-115"><dt>**indicador de WINBIO \_ \_ desactivado**</dt></span><span class="sxs-lookup"><span data-stu-id="a9024-115"><dt>**WINBIO\_INDICATOR\_OFF**</dt></span></span> </dl> | <span data-ttu-id="a9024-116">La luz del indicador del sensor está desactivada.</span><span class="sxs-lookup"><span data-stu-id="a9024-116">The sensor indicator light is off.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a9024-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9024-117">Requirements</span></span>



| <span data-ttu-id="a9024-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9024-118">Requirement</span></span> | <span data-ttu-id="a9024-119">Value</span><span class="sxs-lookup"><span data-stu-id="a9024-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9024-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9024-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a9024-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9024-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="a9024-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9024-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a9024-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9024-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a9024-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9024-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9024-125"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9024-125"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9024-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9024-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9024-127">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="a9024-127">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





