---
description: Representa un encabezado de un \_ objeto DisplayController de CIM.
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: CIM_VideoHead (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22f8176c9bdbeae460dfa22ca395e7ed8dd8351e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687345"
---
# <a name="cim_videohead-class"></a>\_Clase de Videopartida CIM

Representa un encabezado de un [**objeto \_ DisplayController de CIM**](cim-displaycontroller.md) .

## <a name="syntax"></a>Sintaxis

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a>Miembros

La clase de **\_ videopartida CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ videopartida CIM** tiene estas propiedades.

<dl> <dt>

**CurrentBitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,12 "), **punitivo** (" bit ")
</dt> </dl>

Número de bits usados para mostrar cada píxel.

</dd> <dt>

**CurrentHorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,11 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. HorizontalResolution "), **punitivo** (" píxel ")
</dt> </dl>

Número actual de píxeles horizontales.

</dd> <dt>

**CurrentNumberOfColors**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VideoHeadResolution. NumberOfColors")
</dt> </dl>

El número de colores admitidos en la resolución actual.

</dd> <dt>

**CurrentNumberOfColumns**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 004,14 ")
</dt> </dl>

Si está en modo de carácter, el número de columnas del controlador de pantalla; de lo contrario, "0".

</dd> <dt>

**CurrentNumberOfRows**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 004,13 ")
</dt> </dl>

Si está en modo de carácter, el número de filas del controlador de pantalla; de lo contrario, "0".

</dd> <dt>

**CurrentRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hercios"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,15 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution.), **punitivo** ("hercios")
</dt> </dl>

Frecuencia de actualización actual del controlador de pantalla, en hercios.

</dd> <dt>

**CurrentScanMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ videohead**.**OtherCurrentScanMode**, CIM \_ VideoHeadResolution. ScanMode ")
</dt> </dl>

El modo de exploración actual del controlador de pantalla.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**No compatible** (2)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

**Operación no entrelazada** (3)


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

**Operación entrelazada** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**CurrentVerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,10 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. VerticalResolution "), **punitivo** (" píxel ")
</dt> </dl>

Número actual de píxeles verticales.

</dd> <dt>

**MaxRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hercios"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MaxRefreshRate "), **punitivo** (" hercios ")
</dt> </dl>

La frecuencia máxima de actualización del controlador de pantalla, en hercios.

</dd> <dt>

**MinRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hercios"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MinRefreshRate "), **punitivo** (" hercios ")
</dt> </dl>

La frecuencia de actualización mínima del controlador de pantalla, en hercios.

</dd> <dt>

**OtherCurrentScanMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ videohead**.**CurrentScanMode**, CIM \_ VideoHeadResolution. OtherScanMode ")
</dt> </dl>

Descripción del modo de examen actual cuando la propiedad **CurrentScanMode** es "1" (otra).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDevice de CIM \_**](cim-logicaldevice.md)
</dt> </dl>

 

