---
description: El \_ tipo de \_ enumeración modos de medición de exposición \_ de WPD describe el modo de medición que se va a usar al estimar la exposición de una captura de imagen continuada por un dispositivo.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: Enumeración WPD_EXPOSURE_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680388"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a><span data-ttu-id="3fd42-103">\_ \_ Enumeración de modos de medición de exposición de WPD \_</span><span class="sxs-lookup"><span data-stu-id="3fd42-103">WPD\_EXPOSURE\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="3fd42-104">El tipo de enumeración modos de medición de exposición de WPD describe el modo de medición que se va a usar al estimar la exposición de una captura de imagen continuada por un dispositivo. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3fd42-104">The **WPD\_EXPOSURE\_METERING\_MODES** enumeration type describes the metering mode to use when estimating exposure for still image capture by a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fd42-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="3fd42-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3fd42-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3fd42-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**modo de disponibilidad de exposición de WPD \_ \_ \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="3fd42-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD\_EXPOSURE\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="3fd42-108">El modo de disponibilidad no está definido.</span><span class="sxs-lookup"><span data-stu-id="3fd42-108">The metering mode is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="3fd42-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_promedio del \_ modo de medición de exposición de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3fd42-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="3fd42-110">Usar la exposición mediada en toda la imagen.</span><span class="sxs-lookup"><span data-stu-id="3fd42-110">Use averaged exposure across the full image.</span></span>

</dd> <dt>

<span data-ttu-id="3fd42-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**\_ \_ \_ \_ \_ media ponderada del centro del modo de medición de exposición \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="3fd42-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_WEIGHTED\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="3fd42-112">Use una exposición media, con el centro de la imagen dado más peso.</span><span class="sxs-lookup"><span data-stu-id="3fd42-112">Use an averaged exposure, with the center of the image given more weight.</span></span>

</dd> <dt>

<span data-ttu-id="3fd42-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**el modo de disponibilidad de exposición de WPD es \_ \_ multi- \_ \_ \_ Spot**</span><span class="sxs-lookup"><span data-stu-id="3fd42-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="3fd42-114">Usar una técnica de promedio de varias zonas.</span><span class="sxs-lookup"><span data-stu-id="3fd42-114">Use a multi-spot averaging technique.</span></span>

</dd> <dt>

<span data-ttu-id="3fd42-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**\_zona del \_ centro del \_ modo \_ de \_ medición de exposición de WPD**</span><span class="sxs-lookup"><span data-stu-id="3fd42-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="3fd42-116">Usar una técnica de promedio de punto central.</span><span class="sxs-lookup"><span data-stu-id="3fd42-116">Use a center-spot averaging technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fd42-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fd42-117">Remarks</span></span>

<span data-ttu-id="3fd42-118">Indica el modo de medición del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3fd42-118">Indicates the metering mode of the device.</span></span> <span data-ttu-id="3fd42-119">Esta enumeración se usa en la propiedad de [modo de medición de \_ \_ \_ exposición de \_ \_ imagen de WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd42-119">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd42-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fd42-120">Requirements</span></span>



| <span data-ttu-id="3fd42-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd42-121">Requirement</span></span> | <span data-ttu-id="3fd42-122">Value</span><span class="sxs-lookup"><span data-stu-id="3fd42-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd42-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fd42-123">Header</span></span><br/> | <dl> <span data-ttu-id="3fd42-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd42-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd42-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fd42-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd42-126">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="3fd42-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




