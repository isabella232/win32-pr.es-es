---
description: El \_ tipo de enumeración de modos de efecto de WPD \_ describe varios efectos visuales que se pueden aplicar a una imagen.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Enumeración WPD_EFFECT_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698525"
---
# <a name="wpd_effect_modes-enumeration"></a><span data-ttu-id="29ede-103">\_Enumeración de modos de efecto de WPD \_</span><span class="sxs-lookup"><span data-stu-id="29ede-103">WPD\_EFFECT\_MODES enumeration</span></span>

<span data-ttu-id="29ede-104">El tipo de enumeración de **\_ \_ modos de efecto de WPD** describe varios efectos visuales que se pueden aplicar a una imagen.</span><span class="sxs-lookup"><span data-stu-id="29ede-104">The **WPD\_EFFECT\_MODES** enumeration type describes various visual effects that can be applied to an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="29ede-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29ede-105">Syntax</span></span>


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="29ede-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="29ede-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="29ede-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**modo de efecto de WPD \_ \_ \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="29ede-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**WPD\_EFFECT\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="29ede-108">No se ha especificado ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="29ede-108">No effect has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="29ede-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_color del \_ modo de efecto de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="29ede-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD\_EFFECT\_MODE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="29ede-110">La imagen debe ser de color.</span><span class="sxs-lookup"><span data-stu-id="29ede-110">The image should be color.</span></span>

</dd> <dt>

<span data-ttu-id="29ede-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_ \_ modo de efecto \_ \_ de WPD \_ en blanco y negro**</span><span class="sxs-lookup"><span data-stu-id="29ede-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD\_EFFECT\_MODE\_BLACK\_AND\_WHITE**</span></span>
</dt> <dd>

<span data-ttu-id="29ede-112">La imagen debe estar en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="29ede-112">The image should be black and white.</span></span>

</dd> <dt>

<span data-ttu-id="29ede-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**modo de efecto de WPD \_ \_ \_ sepia**</span><span class="sxs-lookup"><span data-stu-id="29ede-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD\_EFFECT\_MODE\_SEPIA**</span></span>
</dt> <dd>

<span data-ttu-id="29ede-114">La imagen debe ser sepia.</span><span class="sxs-lookup"><span data-stu-id="29ede-114">The image should be sepia.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29ede-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29ede-115">Remarks</span></span>

<span data-ttu-id="29ede-116">Esta enumeración la usa la propiedad de [ \_ modo de \_ \_ efecto \_ de imagen de WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="29ede-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_EFFECT\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="29ede-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29ede-117">Requirements</span></span>



| <span data-ttu-id="29ede-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="29ede-118">Requirement</span></span> | <span data-ttu-id="29ede-119">Value</span><span class="sxs-lookup"><span data-stu-id="29ede-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="29ede-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29ede-120">Header</span></span><br/> | <dl> <span data-ttu-id="29ede-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ede-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ede-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="29ede-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ede-123">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="29ede-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




