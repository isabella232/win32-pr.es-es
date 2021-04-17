---
description: El \_ tipo de \_ enumeración de modos Flash de WPD describe un modo flash que se usa al capturar imágenes con un dispositivo.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Enumeración WPD_FLASH_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671013"
---
# <a name="wpd_flash_modes-enumeration"></a><span data-ttu-id="d5baa-103">\_Enumeración de modos de Flash de WPD \_</span><span class="sxs-lookup"><span data-stu-id="d5baa-103">WPD\_FLASH\_MODES enumeration</span></span>

<span data-ttu-id="d5baa-104">El tipo de enumeración de **\_ \_ modos Flash de WPD** describe un modo flash que se usa al capturar imágenes con un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5baa-104">The **WPD\_FLASH\_MODES** enumeration type describes a flash mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5baa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5baa-105">Syntax</span></span>


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="d5baa-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d5baa-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d5baa-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_modo Flash de WPD \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="d5baa-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD\_FLASH\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="d5baa-108">No se ha especificado ningún modo flash.</span><span class="sxs-lookup"><span data-stu-id="d5baa-108">No flash mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="d5baa-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**modo de Flash de WPD \_ \_ \_ auto**</span><span class="sxs-lookup"><span data-stu-id="d5baa-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD\_FLASH\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="d5baa-110">Especifica que el flash debe usarse en el modo automático, según lo especificado por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5baa-110">Specifies that the flash should be used in the automatic mode, as specified by the device.</span></span>

</dd> <dt>

<span data-ttu-id="d5baa-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_modo Flash de WPD \_ \_ desactivado**</span><span class="sxs-lookup"><span data-stu-id="d5baa-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD\_FLASH\_MODE\_OFF**</span></span>
</dt> <dd>

<span data-ttu-id="d5baa-112">Especifica que no debe usarse Flash.</span><span class="sxs-lookup"><span data-stu-id="d5baa-112">Specifies that no flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d5baa-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_relleno en \_ modo \_ Flash de WPD**</span><span class="sxs-lookup"><span data-stu-id="d5baa-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD\_FLASH\_MODE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="d5baa-114">Especifica un destello de tipo de relleno.</span><span class="sxs-lookup"><span data-stu-id="d5baa-114">Specifies a fill-type flash.</span></span>

</dd> <dt>

<span data-ttu-id="d5baa-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_modo Flash de la \_ \_ vista en color rojo \_ \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="d5baa-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="d5baa-116">Especifica que debe usarse el Flash de reducción de ojos rojos.</span><span class="sxs-lookup"><span data-stu-id="d5baa-116">Specifies that the red eye reduction flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d5baa-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_color de \_ \_ ojos rojos \_ del modo Flash de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d5baa-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="d5baa-118">Especifica que debe usarse el parpadeo de relleno de ojos rojos.</span><span class="sxs-lookup"><span data-stu-id="d5baa-118">Specifies that the red eye fill flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d5baa-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ sincronización externa en modo flash \_ de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="d5baa-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**WPD\_FLASH\_MODE\_EXTERNAL\_SYNC**</span></span>
</dt> <dd>

<span data-ttu-id="d5baa-120">Especifica que el flash se debe sincronizar con otros dispositivos flash externos.</span><span class="sxs-lookup"><span data-stu-id="d5baa-120">Specifies that the flash should be synchronized with other external flash devices.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5baa-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5baa-121">Remarks</span></span>

<span data-ttu-id="d5baa-122">Esta enumeración se usa en la propiedad de [ \_ \_ \_ \_ modo flash](still-image-properties.md) de la imagen de WPD.</span><span class="sxs-lookup"><span data-stu-id="d5baa-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_FLASH\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5baa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5baa-123">Requirements</span></span>



| <span data-ttu-id="d5baa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5baa-124">Requirement</span></span> | <span data-ttu-id="d5baa-125">Value</span><span class="sxs-lookup"><span data-stu-id="d5baa-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5baa-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5baa-126">Header</span></span><br/> | <dl> <span data-ttu-id="d5baa-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5baa-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5baa-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5baa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5baa-129">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="d5baa-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




