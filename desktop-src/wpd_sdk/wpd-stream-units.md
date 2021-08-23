---
description: La enumeración WPD STREAM UNITS especifica los tipos de unidad que se \_ \_ usarán para las operaciones IPortableDeviceUnitsStream.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: WPD_STREAM_UNITS enumeración (PortableDeviceTypes.h)
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
ms.openlocfilehash: d2419453beac6b493ddd1bbbe1281b1596ce00456599074b3872fecb003550c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440765"
---
# <a name="wpd_stream_units-enumeration"></a>Enumeración \_ WPD STREAM \_ UNITS

La **enumeración \_ WPD STREAM \_ UNITS** especifica los tipos de unidad que se usarán para las [**operaciones IPortableDeviceUnitsStream.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**BYTES DE \_ UNIDADES DE \_ FLUJO WPD \_**
</dt> <dd>

Las unidades de flujo se especifican en bytes.

</dd> <dt>

<span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**MARCOS DE \_ UNIDADES \_ DE FLUJO WPD \_**
</dt> <dd>

Las unidades de flujo se especifican en fotogramas.

</dd> <dt>

<span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**FILAS DE \_ UNIDADES DE \_ FLUJO WPD \_**
</dt> <dd>

Las unidades de flujo se especifican en filas.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**UNIDADES \_ DE FLUJO \_ WPD \_ MILISEGUNDOS**
</dt> <dd>

Las unidades de flujo se especifican en milisegundos.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**\_MICROSEGUNDOS \_ DE UNIDADES DE \_ FLUJO WPD**
</dt> <dd>

Las unidades de flujo se especifican en microsegundos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                        |
| Header<br/>                   | <dl> <dt>PortableDeviceTypes.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[**IPortableDeviceUnitsStream::SeekInUnits**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




