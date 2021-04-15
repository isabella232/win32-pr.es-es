---
description: El \_ tipo de \_ enumeración fuentes de alimentación de WPD describe la fuente de alimentación que usa un dispositivo.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: Enumeración WPD_POWER_SOURCES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649602"
---
# <a name="wpd_power_sources-enumeration"></a><span data-ttu-id="e786d-103">\_Enumeración de fuentes de alimentación de WPD \_</span><span class="sxs-lookup"><span data-stu-id="e786d-103">WPD\_POWER\_SOURCES enumeration</span></span>

<span data-ttu-id="e786d-104">El tipo de enumeración **\_ \_ fuentes de alimentación de WPD** describe la fuente de alimentación que usa un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e786d-104">The **WPD\_POWER\_SOURCES** enumeration type describes the power source that a device is using.</span></span>

## <a name="syntax"></a><span data-ttu-id="e786d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e786d-105">Syntax</span></span>


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="e786d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e786d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e786d-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_batería de \_ fuente de alimentación de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e786d-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**WPD\_POWER\_SOURCE\_BATTERY**</span></span>
</dt> <dd>

<span data-ttu-id="e786d-108">La fuente de alimentación del dispositivo es una batería.</span><span class="sxs-lookup"><span data-stu-id="e786d-108">The device power source is a battery.</span></span>

</dd> <dt>

<span data-ttu-id="e786d-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**fuente de alimentación de WPD \_ \_ \_ externa**</span><span class="sxs-lookup"><span data-stu-id="e786d-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD\_POWER\_SOURCE\_EXTERNAL**</span></span>
</dt> <dd>

<span data-ttu-id="e786d-110">El dispositivo usa una fuente de alimentación externa.</span><span class="sxs-lookup"><span data-stu-id="e786d-110">The device uses an external power source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e786d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e786d-111">Remarks</span></span>

<span data-ttu-id="e786d-112">Esta enumeración la usa la [propiedad \_ \_ \_ origen de energía del dispositivo WPD](device-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="e786d-112">This enumeration is used by the [WPD\_DEVICE\_POWER\_SOURCE](device-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e786d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e786d-113">Requirements</span></span>



| <span data-ttu-id="e786d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e786d-114">Requirement</span></span> | <span data-ttu-id="e786d-115">Value</span><span class="sxs-lookup"><span data-stu-id="e786d-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e786d-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e786d-116">Header</span></span><br/> | <dl> <span data-ttu-id="e786d-117"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="e786d-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e786d-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e786d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e786d-119">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="e786d-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




