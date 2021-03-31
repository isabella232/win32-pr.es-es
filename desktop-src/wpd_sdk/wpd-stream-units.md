---
description: La \_ enumeración de unidades de streaming WPD \_ especifica los tipos de unidad que se van a usar para las operaciones IPortableDeviceUnitsStream.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: Enumeración WPD_STREAM_UNITS (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STREAM_UNITS
api_type:
- HeaderDef
api_location:
- PortableDeviceTypes.h
ms.openlocfilehash: 8e70455402a49673b574a0c696b6dda30cc6a884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816806"
---
# <a name="wpd_stream_units-enumeration"></a><span data-ttu-id="cfe71-103">\_Enumeración de unidades de streaming WPD \_</span><span class="sxs-lookup"><span data-stu-id="cfe71-103">WPD\_STREAM\_UNITS enumeration</span></span>

<span data-ttu-id="cfe71-104">La enumeración de **\_ \_ unidades de streaming WPD** especifica los tipos de unidad que se van a usar para las operaciones [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) .</span><span class="sxs-lookup"><span data-stu-id="cfe71-104">The **WPD\_STREAM\_UNITS** enumeration specifies the unit types to be used for [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe71-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfe71-105">Syntax</span></span>


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a><span data-ttu-id="cfe71-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="cfe71-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cfe71-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**\_ \_ bytes de unidades de STREAMing WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cfe71-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD\_STREAM\_UNITS\_BYTES**</span></span>
</dt> <dd>

<span data-ttu-id="cfe71-108">Las unidades de streaming se especifican en bytes.</span><span class="sxs-lookup"><span data-stu-id="cfe71-108">The stream units are specified in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cfe71-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**\_ \_ tramas de unidades de STREAMing WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cfe71-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD\_STREAM\_UNITS\_FRAMES**</span></span>
</dt> <dd>

<span data-ttu-id="cfe71-110">Las unidades de streaming se especifican en fotogramas.</span><span class="sxs-lookup"><span data-stu-id="cfe71-110">The stream units are specified in frames.</span></span>

</dd> <dt>

<span data-ttu-id="cfe71-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**\_filas de unidades de streaming de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cfe71-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**WPD\_STREAM\_UNITS\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="cfe71-112">Las unidades de streaming se especifican en filas.</span><span class="sxs-lookup"><span data-stu-id="cfe71-112">The stream units are specified in rows.</span></span>

</dd> <dt>

<span data-ttu-id="cfe71-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**unidades de streaming de WPD en \_ \_ \_ milisegundos**</span><span class="sxs-lookup"><span data-stu-id="cfe71-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD\_STREAM\_UNITS\_MILLISECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="cfe71-114">Las unidades de streaming se especifican en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="cfe71-114">The stream units are specified in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="cfe71-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**unidades de streaming de WPD en \_ \_ \_ microsegundos**</span><span class="sxs-lookup"><span data-stu-id="cfe71-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD\_STREAM\_UNITS\_MICROSECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="cfe71-116">Las unidades de streaming se especifican en microsegundos.</span><span class="sxs-lookup"><span data-stu-id="cfe71-116">The stream units are specified in microseconds.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfe71-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfe71-117">Requirements</span></span>



| <span data-ttu-id="cfe71-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe71-118">Requirement</span></span> | <span data-ttu-id="cfe71-119">Value</span><span class="sxs-lookup"><span data-stu-id="cfe71-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe71-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfe71-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe71-121">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfe71-121">Windows 8 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cfe71-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfe71-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe71-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cfe71-123">None supported</span></span><br/>                                                                        |
| <span data-ttu-id="cfe71-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfe71-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfe71-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe71-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe71-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfe71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe71-127">**IPortableDeviceUnitsStream**</span><span class="sxs-lookup"><span data-stu-id="cfe71-127">**IPortableDeviceUnitsStream**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[<span data-ttu-id="cfe71-128">**IPortableDeviceUnitsStream::SeekInUnits**</span><span class="sxs-lookup"><span data-stu-id="cfe71-128">**IPortableDeviceUnitsStream::SeekInUnits**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




