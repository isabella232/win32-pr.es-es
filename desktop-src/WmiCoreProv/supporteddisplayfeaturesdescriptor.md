---
description: Representa las características de visualización admitidas del monitor.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: SupportedDisplayFeaturesDescriptor (clase)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073105"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>SupportedDisplayFeaturesDescriptor (clase)

**SupportedDisplayFeaturesDescriptor representa** las características de visualización admitidas del monitor. La información de esta clase corresponde a los datos del estándar E-EDID (Definición de entrada de vídeo) del estándar Enhanced Extended Display Identification Data (E-EDID) de Video Electronics Standard Association (VESA).

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

## <a name="members"></a>Members

La **clase SupportedDisplayFeaturesDescriptor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SupportedDisplayFeaturesDescriptor** tiene estas propiedades.

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Compatibilidad con apagado activo y muy baja potencia. La pantalla consume menos energía cuando recibe una señal de tiempo que está fuera del intervalo operativo activo declarado. La pantalla volverá al funcionamiento normal si la señal de tiempo vuelve al intervalo de funcionamiento normal. Los ejemplos de señales de tiempo fuera del intervalo de funcionamiento normal son ninguna señal de sincronización o ninguna señal DE.

</dd> <dt>

**Displaytype**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de presentación del monitor. En la tabla siguiente se enumeran los valores posibles.



| Value                                                                              | Significado                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Pantalla monocromática/escala de grises<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | Presentación de color RGB<br/>            |
| <dl> <dt>2 (0x2)</dt> </dl> | Pantalla de color no RGB<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla tiene compatibilidad con GTF. Si **es True,** la pantalla admite intervalos basados en el estándar GTF mediante los valores de parámetro GTF predeterminados.

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla tiene un modo de tiempo preferido. Si **es True**, el primer bloque de control de tiempo detallado contiene el modo de control de tiempo preferido del monitor. EDID v.1.3 y posteriores requieren el uso del modo de tiempo preferido.

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True,** la pantalla admite sRGB.

</dd> <dt>

**StandbySupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla admite el modo de espera de vesa display power management signaling (DPMS). Si **es True,** se admite el modo en espera de DPMS.

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla admite la suspensión de la señalización de administración de energía de visualización (DPMS) de VESA. Si **es True,** se admite la suspensión de DPMS.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




