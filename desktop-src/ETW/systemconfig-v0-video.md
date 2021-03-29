---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de vídeo.
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: SystemConfig_V0_Video (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: b840e3c06e74f8acbd1e43550559385e78c9a638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985098"
---
# <a name="systemconfig_v0_video-class"></a>\_Clase de \_ vídeo SystemConfig v0

Esta clase es la clase de tipo de evento para los eventos de configuración de vídeo.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a>Miembros

La clase de **\_ \_ vídeo SystemConfig V0** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ \_ vídeo SystemConfig V0** tiene estas propiedades.

<dl> <dt>

**AdapterString**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8), **máx** . (256)
</dt> </dl>

Nombre o Descripción del adaptador.

</dd> <dt>

**BiosString**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9), **Max** (256)
</dt> </dl>

Nombre del BIOS del adaptador.

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4)
</dt> </dl>

Número de bits usados para mostrar cada píxel.

</dd> <dt>

**ChipType**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6), **Max** (256)
</dt> </dl>

Nombre del chip del adaptador.

</dd> <dt>

**DACType**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7), **Max** (256)
</dt> </dl>

Nombre del chip del convertidor digital a analógico (DAC) del adaptador.

</dd> <dt>

**DeviceId**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10), **Max** (256)
</dt> </dl>

Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.

</dd> <dt>

**MemorySize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1)
</dt> </dl>

Cantidad máxima de memoria admitida, en bytes.

</dd> <dt>

**StateFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11)
</dt> </dl>

Marcas de estado de dispositivo. Puede ser cualquier combinación razonable de lo siguiente.



| Value                                                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**Mostrar \_ DISPOSITIVO \_ conectado \_ al \_ escritorio**</dt> <dt>1 (0x1)</dt> </dl> | El dispositivo es parte del escritorio.<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**Mostrar \_ \_ \_ Controlador de creación de reflejo de dispositivos**</dt> <dt>8 (0x8)</dt> </dl>           | Representa un pseudo dispositivo que se usa para reflejar el dibujo de la aplicación para conectarse a un equipo remoto o a otros fines. Un pseudo monitor invisible está asociado a este dispositivo. Por ejemplo, NetMeeting lo usa.<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**Mostrar \_ DISPOSITIVO \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | El dispositivo tiene más modos de visualización que los dispositivos de salida que admiten.<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**Mostrar \_ Dispositivo \_ primario \_ de dispositivo**</dt> <dt>4 (0x4)</dt> </dl>                 | El escritorio principal está en el dispositivo. Para un sistema con una sola tarjeta de presentación, siempre se establece. Para un sistema con varias tarjetas de presentación, solo un dispositivo puede tener este conjunto.<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**Mostrar \_ DISPOSITIVO \_ extraíble**</dt> <dt>32 (0x20)</dt> </dl>                               | El dispositivo es extraíble; no puede ser la pantalla principal.<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**Mostrar \_ DISPOSITIVO \_ VGA \_ compatible**</dt> <dt>16 (0x10)</dt> </dl>               | El dispositivo es compatible con VGA.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

**VRefresh**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Frecuencia de actualización actual, en hercios.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Número actual de píxeles horizontales.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Número actual de píxeles verticales.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




