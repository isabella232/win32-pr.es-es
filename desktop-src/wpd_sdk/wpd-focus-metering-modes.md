---
description: El \_ tipo de enumeración de modos de medición de foco de WPD describe el modo en que \_ \_ un dispositivo debe decidir qué parte de un marco se va a usar para establecer el foco.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Enumeración WPD_FOCUS_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671012"
---
# <a name="wpd_focus_metering_modes-enumeration"></a><span data-ttu-id="367e9-103">\_ \_ Enumeración de modos de medición de foco de WPD \_</span><span class="sxs-lookup"><span data-stu-id="367e9-103">WPD\_FOCUS\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="367e9-104">El tipo de enumeración de modos de medición de foco de WPD describe el modo en que un dispositivo debe decidir qué parte de un marco se va a usar para establecer el foco. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="367e9-104">The **WPD\_FOCUS\_METERING\_MODES** enumeration type describes how a device should decide what part of a frame to use to set focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="367e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="367e9-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="367e9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="367e9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="367e9-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**modo de medición de foco de WPD \_ \_ \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="367e9-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD\_FOCUS\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="367e9-108">Indica que no se ha especificado ningún modo de enfoque.</span><span class="sxs-lookup"><span data-stu-id="367e9-108">Indicates that no focusing mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="367e9-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_zona del \_ centro del \_ modo \_ de \_ medición de foco de WPD**</span><span class="sxs-lookup"><span data-stu-id="367e9-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="367e9-110">Se centra en el centro del área de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="367e9-110">Focuses on the center of the framed area.</span></span>

</dd> <dt>

<span data-ttu-id="367e9-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**modo de medición de foco de WPD \_ \_ \_ \_ \_ multispot**</span><span class="sxs-lookup"><span data-stu-id="367e9-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="367e9-112">Determine el foco analizando varias partes del área de marco.</span><span class="sxs-lookup"><span data-stu-id="367e9-112">Determine focus by analyzing multiple parts of the framed area.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="367e9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="367e9-113">Remarks</span></span>

<span data-ttu-id="367e9-114">Esta enumeración se especifica mediante la propiedad del [modo de medición de \_ \_ \_ foco de \_ \_ imagen de WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="367e9-114">This enumeration is specified by the [WPD\_STILL\_IMAGE\_FOCUS\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="367e9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="367e9-115">Requirements</span></span>



| <span data-ttu-id="367e9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="367e9-116">Requirement</span></span> | <span data-ttu-id="367e9-117">Value</span><span class="sxs-lookup"><span data-stu-id="367e9-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="367e9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="367e9-118">Header</span></span><br/> | <dl> <span data-ttu-id="367e9-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="367e9-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="367e9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="367e9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="367e9-121">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="367e9-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




