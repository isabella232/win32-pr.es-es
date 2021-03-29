---
description: El \_ \_ \_ tipo de enumeración recortes de valores de estado de WPD describe el estado de recorte de una imagen.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: Enumeración WPD_CROPPED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678933"
---
# <a name="wpd_cropped_status_values-enumeration"></a><span data-ttu-id="a7c52-103">\_ \_ Enumeración de valores de estado recortados de WPD \_</span><span class="sxs-lookup"><span data-stu-id="a7c52-103">WPD\_CROPPED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="a7c52-104">El tipo de enumeración **\_ recortes de \_ \_ valores de estado de WPD** describe el estado de recorte de una imagen.</span><span class="sxs-lookup"><span data-stu-id="a7c52-104">The **WPD\_CROPPED\_STATUS\_VALUES** enumeration type describes the cropping status of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c52-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7c52-105">Syntax</span></span>


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="a7c52-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a7c52-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a7c52-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_Estado recortado de WPD \_ \_ no \_ recortado**</span><span class="sxs-lookup"><span data-stu-id="a7c52-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**WPD\_CROPPED\_STATUS\_NOT\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="a7c52-108">La imagen no se ha recortado.</span><span class="sxs-lookup"><span data-stu-id="a7c52-108">The image has not been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="a7c52-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**\_Estado recortado de WPD recortado \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7c52-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**WPD\_CROPPED\_STATUS\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="a7c52-110">La imagen se ha recortado.</span><span class="sxs-lookup"><span data-stu-id="a7c52-110">The image has been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="a7c52-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**\_ \_ \_ \_ no \_ se debe \_ recortar el estado recortado de WPD**</span><span class="sxs-lookup"><span data-stu-id="a7c52-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**WPD\_CROPPED\_STATUS\_SHOULD\_NOT\_BE\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="a7c52-112">La imagen no ha sido y no debe recortarse.</span><span class="sxs-lookup"><span data-stu-id="a7c52-112">The image has not been, and should not be, cropped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7c52-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7c52-113">Remarks</span></span>

<span data-ttu-id="a7c52-114">Indica el estado recortado de una imagen.</span><span class="sxs-lookup"><span data-stu-id="a7c52-114">Indicates the cropped status of an image.</span></span> <span data-ttu-id="a7c52-115">Esta enumeración se usa en la propiedad [ \_ \_ \_ Estado recortado de imagen de WPD](image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="a7c52-115">This enumeration is used by the [WPD\_IMAGE\_CROPPED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7c52-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7c52-116">Requirements</span></span>



| <span data-ttu-id="a7c52-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7c52-117">Requirement</span></span> | <span data-ttu-id="a7c52-118">Value</span><span class="sxs-lookup"><span data-stu-id="a7c52-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c52-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7c52-119">Header</span></span><br/> | <dl> <span data-ttu-id="a7c52-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7c52-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7c52-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7c52-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c52-122">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="a7c52-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




