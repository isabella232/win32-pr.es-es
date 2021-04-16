---
description: El \_ tipo de enumeración de valores de equilibrio de blanco de WPD \_ \_ describe cómo un dispositivo de vídeo o imagen pondera los canales de color para lograr un equilibrio de blanco adecuado.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Enumeración WPD_WHITE_BALANCE_SETTINGS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649731"
---
# <a name="wpd_white_balance_settings-enumeration"></a><span data-ttu-id="7608e-103">\_ \_ Enumeración de valores de equilibrio de blanco de WPD \_</span><span class="sxs-lookup"><span data-stu-id="7608e-103">WPD\_WHITE\_BALANCE\_SETTINGS enumeration</span></span>

<span data-ttu-id="7608e-104">El tipo de enumeración de valores de equilibrio de blanco de WPD describe cómo un dispositivo de vídeo o imagen pondera los canales de color para lograr un equilibrio de blanco adecuado. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7608e-104">The **WPD\_WHITE\_BALANCE\_SETTINGS** enumeration type describes how a video or image device weights color channels to achieve a proper white balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="7608e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7608e-105">Syntax</span></span>


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="7608e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7608e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7608e-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_balance blanco de WPD \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="7608e-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD\_WHITE\_BALANCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="7608e-108">Este valor no se ha definido.</span><span class="sxs-lookup"><span data-stu-id="7608e-108">This value has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="7608e-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_manual de \_ balance \_ blanco de WPD**</span><span class="sxs-lookup"><span data-stu-id="7608e-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD\_WHITE\_BALANCE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="7608e-110">El balance de blanco se establece explícitamente mediante la propiedad de [ \_ \_ ganancia de imagen \_ RGB \_ ](still-image-properties.md) de la imagen de carga continua de WPD y no cambiará.</span><span class="sxs-lookup"><span data-stu-id="7608e-110">The white balance is set explicitly by using the [WPD\_STILL\_IMAGE\_RGB\_GAIN](still-image-properties.md) property and will not change by itself.</span></span>

</dd> <dt>

<span data-ttu-id="7608e-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_balance blanco de WPD \_ \_ automático**</span><span class="sxs-lookup"><span data-stu-id="7608e-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD\_WHITE\_BALANCE\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="7608e-112">El dispositivo establecerá el balance de blanco.</span><span class="sxs-lookup"><span data-stu-id="7608e-112">The device will set the white balance.</span></span>

</dd> <dt>

<span data-ttu-id="7608e-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**equilibrio de blanco de WPD \_ en \_ \_ una \_ instalación \_ automática**</span><span class="sxs-lookup"><span data-stu-id="7608e-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD\_WHITE\_BALANCE\_ONE\_PUSH\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="7608e-114">El dispositivo establecerá el balance de blanco, pero solo cuando el usuario inserte el botón de captura del dispositivo mientras dirige el dispositivo a un campo en blanco.</span><span class="sxs-lookup"><span data-stu-id="7608e-114">The device will set the white balance, but only when the user pushes the device's capture button while aiming the device at a white field.</span></span>

</dd> <dt>

<span data-ttu-id="7608e-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**\_verano de \_ balance \_ blanco de WPD**</span><span class="sxs-lookup"><span data-stu-id="7608e-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD\_WHITE\_BALANCE\_DAYLIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="7608e-116">El dispositivo usará los números de balance de blanco adecuados para su uso en la mayoría de los valores de horario de verano.</span><span class="sxs-lookup"><span data-stu-id="7608e-116">The device will use white balance numbers appropriate for use in most daylight settings.</span></span>

</dd> <dt>

<span data-ttu-id="7608e-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**\_Tungsten de \_ equilibrio de blanco de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="7608e-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD\_WHITE\_BALANCE\_TUNGSTEN**</span></span>
</dt> <dd>

<span data-ttu-id="7608e-118">El dispositivo usará los números de balance de blanco adecuados para su uso en la mayoría de los valores de iluminación de la luz de los interiores.</span><span class="sxs-lookup"><span data-stu-id="7608e-118">The device will use white balance numbers appropriate for use in most indoor, incandescent lighting settings.</span></span>

</dd> <dt>

<span data-ttu-id="7608e-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**BALANCE de blanco de WPD \_ en \_ \_ Flash**</span><span class="sxs-lookup"><span data-stu-id="7608e-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD\_WHITE\_BALANCE\_FLASH**</span></span>
</dt> <dd>

<span data-ttu-id="7608e-120">El dispositivo usará los números de balance de blanco adecuados para su uso con un flash.</span><span class="sxs-lookup"><span data-stu-id="7608e-120">The device will use white balance numbers appropriate for use with a flash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7608e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7608e-121">Remarks</span></span>

<span data-ttu-id="7608e-122">Esta enumeración se usa en la propiedad de equilibrio de blancos de la imagen de la [ \_ \_ imagen \_ \_ ](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="7608e-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_WHITE\_BALANCE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7608e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7608e-123">Requirements</span></span>



| <span data-ttu-id="7608e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7608e-124">Requirement</span></span> | <span data-ttu-id="7608e-125">Value</span><span class="sxs-lookup"><span data-stu-id="7608e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7608e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7608e-126">Header</span></span><br/> | <dl> <span data-ttu-id="7608e-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7608e-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7608e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7608e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7608e-129">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="7608e-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




