---
description: El \_ \_ tipo de enumeración de modos de captura de WPD describe el modo de control de tiempo de captura de una captura de imagen fija.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Enumeración WPD_CAPTURE_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718707"
---
# <a name="wpd_capture_modes-enumeration"></a><span data-ttu-id="748bf-103">\_Enumeración de modos de captura de WPD \_</span><span class="sxs-lookup"><span data-stu-id="748bf-103">WPD\_CAPTURE\_MODES enumeration</span></span>

<span data-ttu-id="748bf-104">El tipo de enumeración de **\_ \_ modos de captura de WPD** describe el modo de control de tiempo de captura de una captura de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="748bf-104">The **WPD\_CAPTURE\_MODES** enumeration type describes the capture timing mode of a still image capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="748bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="748bf-105">Syntax</span></span>


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="748bf-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="748bf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="748bf-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**modo de captura de WPD \_ \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="748bf-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD\_CAPTURE\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="748bf-108">No se ha definido el modo de captura.</span><span class="sxs-lookup"><span data-stu-id="748bf-108">The capture mode has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="748bf-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**modo de captura de WPD \_ \_ \_ normal**</span><span class="sxs-lookup"><span data-stu-id="748bf-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD\_CAPTURE\_MODE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="748bf-110">No se debe usar ningún retraso ni modo de ráfaga.</span><span class="sxs-lookup"><span data-stu-id="748bf-110">No delay or burst mode should be used.</span></span>

</dd> <dt>

<span data-ttu-id="748bf-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**ráfaga en el modo de captura de WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="748bf-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD\_CAPTURE\_MODE\_BURST**</span></span>
</dt> <dd>

<span data-ttu-id="748bf-112">Especifica que se debe capturar un número definido de imágenes con un intervalo definido entre ellas.</span><span class="sxs-lookup"><span data-stu-id="748bf-112">Specifies that a defined number of images should be captured with a defined interval between them.</span></span> <span data-ttu-id="748bf-113">El número de imágenes que se van a capturar y el tiempo de retardo entre ellas se especifican mediante las propiedades de número de ráfaga de imagen de la [ \_ \_ \_ \_ imagen de WPD](still-image-properties.md) y de [ \_ \_ \_ \_ intervalo de ráfaga de imagen](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="748bf-113">The number of images to capture and time delay between them are specified by the [WPD\_STILL\_IMAGE\_BURST\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_BURST\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="748bf-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**modo de captura de WPD \_ \_ \_ TIMELAPSE**</span><span class="sxs-lookup"><span data-stu-id="748bf-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD\_CAPTURE\_MODE\_TIMELAPSE**</span></span>
</dt> <dd>

<span data-ttu-id="748bf-115">La captura de imagen debe usar la fotografía de lapso de tiempo.</span><span class="sxs-lookup"><span data-stu-id="748bf-115">Image capture should use time lapse photography.</span></span> <span data-ttu-id="748bf-116">El número de imágenes y el intervalo entre ellas se describen en las propiedades del intervalo [ \_ \_ \_ TIMELAPSE \_ ](still-image-properties.md) y de la imagen estática de WPD y de la [ \_ imagen de \_ \_ TIMELAPSE \_ ](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="748bf-116">The number of images and interval between them are described by the [WPD\_STILL\_IMAGE\_TIMELAPSE\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_TIMELAPSE\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="748bf-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="748bf-117">Remarks</span></span>

<span data-ttu-id="748bf-118">Esta enumeración se usa en la propiedad de modo de captura de imagen de la [ \_ \_ imagen \_ \_ de WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="748bf-118">This enumeration is used by the [WPD\_STILL\_IMAGE\_CAPTURE\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="748bf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="748bf-119">Requirements</span></span>



| <span data-ttu-id="748bf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="748bf-120">Requirement</span></span> | <span data-ttu-id="748bf-121">Value</span><span class="sxs-lookup"><span data-stu-id="748bf-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="748bf-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="748bf-122">Header</span></span><br/> | <dl> <span data-ttu-id="748bf-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="748bf-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="748bf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="748bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="748bf-125">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="748bf-125">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="748bf-126">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="748bf-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




