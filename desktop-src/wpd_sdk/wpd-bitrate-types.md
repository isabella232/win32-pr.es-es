---
description: El \_ tipo de enumeración de tipos de velocidad de bits de WPD \_ describe un tipo de compresión de archivos de audio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Enumeración WPD_BITRATE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718939"
---
# <a name="wpd_bitrate_types-enumeration"></a><span data-ttu-id="853bf-103">\_Enumeración de tipos de velocidad de bits de WPD \_</span><span class="sxs-lookup"><span data-stu-id="853bf-103">WPD\_BITRATE\_TYPES enumeration</span></span>

<span data-ttu-id="853bf-104">El tipo de enumeración de **\_ \_ tipos de velocidad de bits de WPD** describe el tipo de compresión de un archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="853bf-104">The **WPD\_BITRATE\_TYPES** enumeration type describes an audio file's compression type.</span></span>

## <a name="syntax"></a><span data-ttu-id="853bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="853bf-105">Syntax</span></span>


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="853bf-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="853bf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="853bf-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**tipo de velocidad de bits de WPD \_ \_ \_ sin usar**</span><span class="sxs-lookup"><span data-stu-id="853bf-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**WPD\_BITRATE\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="853bf-108">No se ha especificado este valor.</span><span class="sxs-lookup"><span data-stu-id="853bf-108">This value has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="853bf-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_ \_ tipo discreto de velocidad de bits de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="853bf-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD\_BITRATE\_TYPE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="853bf-110">Compresión de velocidad de bits constante.</span><span class="sxs-lookup"><span data-stu-id="853bf-110">Constant bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="853bf-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**VARIABLE de tipo de velocidad de bits de WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="853bf-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD\_BITRATE\_TYPE\_VARIABLE**</span></span>
</dt> <dd>

<span data-ttu-id="853bf-112">Compresión de velocidad de bits variable.</span><span class="sxs-lookup"><span data-stu-id="853bf-112">Variable bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="853bf-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**tipo de velocidad de bits de WPD \_ \_ \_ gratis**</span><span class="sxs-lookup"><span data-stu-id="853bf-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD\_BITRATE\_TYPE\_FREE**</span></span>
</dt> <dd>

<span data-ttu-id="853bf-114">Velocidad de bits de formato libre.</span><span class="sxs-lookup"><span data-stu-id="853bf-114">Free format bit rate.</span></span> <span data-ttu-id="853bf-115">Se trata de una velocidad de bits constante inferior a la velocidad de bits máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="853bf-115">This is a constant bit rate that is lower than the maximum allowed bit rate.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="853bf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="853bf-116">Requirements</span></span>



| <span data-ttu-id="853bf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="853bf-117">Requirement</span></span> | <span data-ttu-id="853bf-118">Value</span><span class="sxs-lookup"><span data-stu-id="853bf-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="853bf-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="853bf-119">Header</span></span><br/> | <dl> <span data-ttu-id="853bf-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="853bf-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="853bf-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="853bf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="853bf-122">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="853bf-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




