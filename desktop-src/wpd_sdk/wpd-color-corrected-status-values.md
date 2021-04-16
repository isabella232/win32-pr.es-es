---
description: El \_ \_ \_ \_ tipo de enumeración valores de estado corregidos en color de WPD describe el estado de corrección del color de un archivo de imagen o vídeo.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: Enumeración WPD_COLOR_CORRECTED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718897"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a><span data-ttu-id="d6c9b-103">\_ \_ \_ Enumeración de valores de estado corregidos en color de WPD \_</span><span class="sxs-lookup"><span data-stu-id="d6c9b-103">WPD\_COLOR\_CORRECTED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="d6c9b-104">El tipo de enumeración **\_ \_ \_ \_ valores de estado corregidos en color de WPD** describe el estado de corrección del color de un archivo de imagen o vídeo.</span><span class="sxs-lookup"><span data-stu-id="d6c9b-104">The **WPD\_COLOR\_CORRECTED\_STATUS\_VALUES** enumeration type describes the color correction status of an image or video file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c9b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6c9b-105">Syntax</span></span>


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="d6c9b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d6c9b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d6c9b-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_Estado corregido de color de WPD \_ \_ \_ no \_ corregido**</span><span class="sxs-lookup"><span data-stu-id="d6c9b-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_NOT\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="d6c9b-108">No se ha corregido el color de la imagen.</span><span class="sxs-lookup"><span data-stu-id="d6c9b-108">The image has not been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="d6c9b-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**se \_ \_ corrigió el \_ Estado corregido de color de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="d6c9b-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="d6c9b-110">Se corrigió el color de la imagen.</span><span class="sxs-lookup"><span data-stu-id="d6c9b-110">The image has been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="d6c9b-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**el \_ Estado corrección del color de WPD \_ \_ \_ \_ no debe \_ \_ corregirse**</span><span class="sxs-lookup"><span data-stu-id="d6c9b-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_SHOULD\_NOT\_BE\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="d6c9b-112">La imagen no ha sido, y no debe ser, se ha corregido el color.</span><span class="sxs-lookup"><span data-stu-id="d6c9b-112">The image has not been, and should not be, color corrected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6c9b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6c9b-113">Remarks</span></span>

<span data-ttu-id="d6c9b-114">Indica el estado de corrección del color de una imagen.</span><span class="sxs-lookup"><span data-stu-id="d6c9b-114">Indicates the color corrected status of an image.</span></span> <span data-ttu-id="d6c9b-115">Esta enumeración se usa en la propiedad de [ \_ \_ \_ \_ Estado corrección de color de imagen de WPD](image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c9b-115">This enumeration is used by the [WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c9b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6c9b-116">Requirements</span></span>



| <span data-ttu-id="d6c9b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c9b-117">Requirement</span></span> | <span data-ttu-id="d6c9b-118">Value</span><span class="sxs-lookup"><span data-stu-id="d6c9b-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c9b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6c9b-119">Header</span></span><br/> | <dl> <span data-ttu-id="d6c9b-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c9b-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6c9b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6c9b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c9b-122">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="d6c9b-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




