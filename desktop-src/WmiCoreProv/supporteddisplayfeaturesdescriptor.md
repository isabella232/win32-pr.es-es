---
description: Representa las características de presentación admitidas del monitor.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: Clase SupportedDisplayFeaturesDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705883"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>Clase SupportedDisplayFeaturesDescriptor

**SupportedDisplayFeaturesDescriptor** representa las características de presentación admitidas del monitor. La información de esta clase se corresponde con los datos de la definición de entrada de vídeo de la estándar de identificación de vídeo electrónica (VESA) de la asociación mejorada de visualización de datos (E-EDID).

## <a name="syntax"></a>Sintaxis

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a>Miembros

La clase **SupportedDisplayFeaturesDescriptor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SupportedDisplayFeaturesDescriptor** tiene estas propiedades.

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Compatibilidad con la energía activa y muy baja. La pantalla consume menos energía cuando recibe una señal de tiempo que está fuera del intervalo operativo activo declarado. La pantalla volverá al funcionamiento normal si la señal de temporización vuelve al intervalo operativo normal. Algunos ejemplos de señales de control de tiempo fuera del intervalo operativo normal son las señales de sincronización o la ausencia DE señal.

</dd> <dt>

**TipoDePresentación**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de pantalla para el monitor. En la tabla siguiente se enumeran los valores posibles.



| Value                                                                              | Significado                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0X0)</dt> </dl> | Pantalla monocroma/escala de grises<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | Presentación de color RGB<br/>            |
| <dl> <dt>2 (0X2)</dt> </dl> | Pantalla multicolor no RGB<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla tiene compatibilidad con GTF. Si **es true**, la pantalla admite los tiempos basados en el estándar GTF con los valores de parámetro GTF predeterminados.

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla tiene un modo de control de tiempo preferido. Si **es true**, el primer bloque de tiempo detallado contiene el modo de control de tiempo preferido del monitor. El uso del modo de control de tiempo preferido es necesario para EDID v. 1.3 y versiones posteriores.

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, la pantalla admite sRGB.

</dd> <dt>

**StandbySupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla es compatible con el modo de espera de la señal de administración de energía (DPMS) de pantalla VESA. Si es **true**, se admite el modo de espera de DPMS.

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla admite la suspensión de la señal de administración de energía (DPMS) de pantalla VESA. Si **es true**, se admite la suspensión de DPMS.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




