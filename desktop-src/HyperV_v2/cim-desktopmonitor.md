---
description: Representa un monitor de escritorio de CRT.
ms.assetid: 26a06320-9fd9-434e-87c8-486e9ca4945c
title: CIM_DesktopMonitor (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab152fc10f3fd404744c293d2368039ffcfdb291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666697"
---
# <a name="cim_desktopmonitor-class-hyper-v-management"></a>CIM_DesktopMonitor (clase, administración de Hyper-V)

Representa un monitor de escritorio de CRT.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices")]
class CIM_DesktopMonitor : CIM_Display
{
  uint16 DisplayType;
  uint32 Bandwidth;
  uint32 ScreenHeight;
  uint32 ScreenWidth;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ DesktopMonitor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ DesktopMonitor** tiene estas propiedades.

<dl> <dt>

**Ancho de banda**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahercios"), **punitivo** ("hercios \* 10 ^ 6")
</dt> </dl>

Ancho de banda de la pantalla, en MHertz. "0" indica desconocido.

</dd> <dt>

**TipoDePresentación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de tipo de presentación del monitor de CRT. Por ejemplo, color Multiscan o monocromo.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

**Color de Multiscan** (2)


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

**Monocromo Multiscan** (3)


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

**Color de frecuencia fijo** (4)


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

**Monocromática de frecuencia fija** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ScreenHeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Alto lógico de la pantalla, en coordenadas de la pantalla.

</dd> <dt>

**ScreenWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho lógico de la pantalla, en coordenadas de la pantalla.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Presentación de CIM \_**](cim-display.md)
</dt> </dl>

 

