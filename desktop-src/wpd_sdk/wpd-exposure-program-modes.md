---
description: El \_ tipo de \_ enumeración modos del programa de exposición de WPD \_ describe un modo de exposición que se usa al capturar imágenes con un dispositivo.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Enumeración WPD_EXPOSURE_PROGRAM_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680386"
---
# <a name="wpd_exposure_program_modes-enumeration"></a><span data-ttu-id="7bdfc-103">\_ \_ Enumeración de modos de programa de exposición de WPD \_</span><span class="sxs-lookup"><span data-stu-id="7bdfc-103">WPD\_EXPOSURE\_PROGRAM\_MODES enumeration</span></span>

<span data-ttu-id="7bdfc-104">El tipo de enumeración modos del programa de exposición de WPD describe un modo de exposición que se usa al capturar imágenes con un dispositivo. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-104">The **WPD\_EXPOSURE\_PROGRAM\_MODES** enumeration type describes an exposure mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bdfc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bdfc-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="7bdfc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7bdfc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7bdfc-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**modo de programa de exposición de WPD \_ \_ \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="7bdfc-108">No se ha especificado el modo de exposición.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-108">The exposure mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="7bdfc-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_manual del \_ modo de programa de exposición de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="7bdfc-110">La aplicación debe especificar toda la configuración de exposición.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-110">The application should specify all exposure settings.</span></span>

</dd> <dt>

<span data-ttu-id="7bdfc-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**modo de programa de exposición de WPD \_ \_ \_ \_ auto**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="7bdfc-112">Use un modo de exposición automática definido por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-112">Use a device-defined automatic exposure mode.</span></span>

</dd> <dt>

<span data-ttu-id="7bdfc-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**\_prioridad de \_ abertura del modo de programa de exposición de \_ \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_APERTURE\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="7bdfc-114">Un modo de exposición automatizada que indica que el valor de apertura de la lente debe permanecer fijo, pero el dispositivo debe determinar la velocidad del obturador.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-114">An automated exposure mode that indicates that the lens aperture value should remain fixed, but shutter speed should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="7bdfc-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_prioridad de \_ \_ \_ obturador del \_ modo de exposición de WPD**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_SHUTTER\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="7bdfc-116">Un modo de exposición automatizada que indica que la velocidad del obturador debe permanecer fija, pero el dispositivo debe determinar la abertura del objetivo.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-116">An automated exposure mode that indicates that the shutter speed should remain fixed, but that lens aperture should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="7bdfc-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_creatividad del \_ modo de programa de exposición de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_CREATIVE**</span></span>
</dt> <dd>

<span data-ttu-id="7bdfc-118">Modo de exposición automatizada que intenta maximizar la profundidad del campo.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-118">An automated exposure mode that tries to maximize the depth of field.</span></span>

</dd> <dt>

<span data-ttu-id="7bdfc-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_acción del \_ modo de programa de exposición de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_ACTION**</span></span>
</dt> <dd>

<span data-ttu-id="7bdfc-120">Modo de exposición automatizada que intenta maximizar la velocidad del obturador.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-120">An automated exposure mode that tries to maximize the shutter speed.</span></span>

</dd> <dt>

<span data-ttu-id="7bdfc-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**modo de programa de exposición de WPD \_ \_ \_ \_ vertical**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_PORTRAIT**</span></span>
</dt> <dd>

<span data-ttu-id="7bdfc-122">Modo de exposición automatizada que especifica una profundidad relativamente superficial de campo.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-122">An automated exposure mode that specifies a relatively shallow depth of field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bdfc-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bdfc-123">Remarks</span></span>

<span data-ttu-id="7bdfc-124">Indica el modo del programa de exposición del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-124">Indicates the exposure program mode of the device.</span></span> <span data-ttu-id="7bdfc-125">Esta enumeración se usa en la propiedad del [modo de programa de \_ \_ exposición de imagen \_ \_ \_ estática de WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="7bdfc-125">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_PROGRAM\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bdfc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bdfc-126">Requirements</span></span>



| <span data-ttu-id="7bdfc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bdfc-127">Requirement</span></span> | <span data-ttu-id="7bdfc-128">Value</span><span class="sxs-lookup"><span data-stu-id="7bdfc-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bdfc-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bdfc-129">Header</span></span><br/> | <dl> <span data-ttu-id="7bdfc-130"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bdfc-130"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bdfc-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bdfc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bdfc-132">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="7bdfc-132">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




